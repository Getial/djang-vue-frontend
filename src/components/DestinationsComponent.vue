<template>
    <section class="third-section w-100 d-flex flex-column align-items-center justify-content-evenly">
        <h2  class="fs-1 fw-bolder">Exclusive <span class="text-danger">deals & discounts</span></h2>
        <p class="text-secondary text-center">
            Discover our fantastic early booking discounts
            <br>
            & start planning your journey
        </p>
        <div class="carrusel d-flex mb-3 justify-content-evenly">

            <div class="bg-white rounded position-relative" v-for="destination in destinations" :key="destination.id" @mouseover="$event => {upHere = true, toggleHover(destination.id)}" @mouseleave="$event => {upHere = false, toggleHover(destination.id)}" >
                <img :src="destination.image" class="w-100" alt="...">
                <div class="mt-2 p-1 card-info">
                    <div class="d-flex justify-content-between align-items-bottom">
                        <h4 class="card-title">{{ destination.place }}</h4>
                        <p class="text-secondary">⭐ {{ destination.score }}</p>
                    </div>
                    <div class="d-flex justify-content-between">
                        <p class="text-secondary d-flex">
                            <img src="../assets/icon-ubication.png" class="h-75 img-fluid me-2" alt="">
                            {{  destination.country }}
                        </p>
                        <p class="text-decoration-line-through text-secondary">${{ destination.price }} <span class="badge bg-danger">${{ destination.priceWithDiscount }}</span></p>
                    </div>
                </div>
                <button :id="destination.id" class="position-absolute inactive top-50 bg-danger btn btn-sm text-white fs-6">Book Now</button>
            </div>


        </div>
        <div class="w-100 d-flex justify-content-center"> <!--buttons-->
            <button class="arrow-left-btn me-5 border text-secondary border-dark-subtle">➔</button>
            <button class="arrow-right-btn bg-danger text-white fs-4">➔</button>
        </div>
    </section>
</template>

<script>
    import axios from 'axios'

    export default ({
        name: 'DestinationsComponent',

        data() {
            return {
                destinations: [],
                upHere: false
            }
        },

        mounted() {
            axios.get('http://127.0.0.1:8000/api/destinations/')
            .then(response => {
                this.destinations = response.data
            })
            .catch(error => {
                console.log(error);
            })
        },

        methods: {
            toggleHover(id) {
                const btn = document.getElementById(id)
                if(this.upHere === true) {
                    btn.classList.remove('inactive')
                }
                else if(this.upHere === false) {
                    btn.classList.add('inactive')
                }
            }
        }
    })
</script>

<style>
    .third-section {
        height: 950px;
    }

    .third-section .carrusel {
        width: 80%;
    }

    .third-section .carrusel > div {
        width: 22%;
        height: 380px;
        background: #FEFCFB;
        border: 2px solid rgba(102, 102, 102, 0.08);
        border-radius: 8px;
    }

    .arrow-right-btn,
    .arrow-left-btn  {
        width: 40px;
        height: 40px;
        border-radius: 20px;
        border: none;
    }

    .arrow-left-btn {
        transform: rotate(180deg);
        background-color: white;
    }
    
    .card-info div p {
        font-size: 16px;
    }

    .inactive {
        display: none !important;
    }
    
    @media screen and ( max-width:1024px ) {
        .third-section .carrusel > div {
            height: 280px;
        }

        .card-info div p {
        font-size: 14px;
    }
    }

    @media screen and ( max-width:780px ) {
        .third-section .carrusel > div {
            height: 250px;
        }
        .card-info div p {
            font-size: 12px;
        }
    }
</style>