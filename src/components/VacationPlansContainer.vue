<template>
    <section class="fourth-section w-100 d-flex flex-column align-items-center justify-content-evenly position-relative">
        <img src="../assets/trees.png" class="trees position-absolute img-fluid" alt="">
        <h2  class="fs-1 fw-bolder">Best <span class="text-danger">vacation plan</span></h2>
        <p class="text-secondary text-center">
        Plan your perfect vacation with outr travel agency. Chose
        <br>
        among hundreds of all-inclusive offers!
        </p>
        <div class="carrusel d-flex w-75 mb-3 justify-content-evenly">

            <div class="bg-white rounded" v-for="plan in vacationsplans" :key="plan.id">
                <img :src="plan.image" class="w-100 rounded" alt="...">
                <div class="mt-2 px-1 pt-2">
                <div class="d-flex justify-content-between align-items-bottom">
                    <h4 class="card-title">{{ plan.place }}, {{ plan.country }}</h4>
                    <p class="text-danger">${{ plan.price }}k</p>
                </div>
                <div class="d-flex justify-content-between">
                    <p class="col text-secondary d-flex fs-6">
                    <img src="../assets/cursor.png" class="h-75 img-fluid me-1" alt="">
                    {{ plan.duration }} Days trip
                    </p>
                    <p class="text-secondary fs-6">⭐ {{ plan.score }}</p>
                </div>
                </div>
            </div>
        
        </div>
        <div class="btns-fourth-section w-25 d-flex justify-content-center position-absolute"> <!--buttons-->
        <button class="arrow-left-btn me-4 border text-secondary border-dark-subtle">➔</button>
        <button class="arrow-right-btn bg-danger text-white fs-4">➔</button>
        </div>
    </section>
</template>

<script>
    import axios from 'axios'

    export default ({
        name: 'VacationPlansComponent',

        data() {
            return {
                vacationsplans: []
            }
        },

        mounted() {
            axios.get('http://127.0.0.1:8000/api/vacationplans/')
            .then(response => {
                this.vacationsplans = response.data
            })
            .catch(error => {
                console.log(error);
            })
        }
    })
</script>

<style>
    .fourth-section {
        height: 700px;
    }

    .fourth-section .carrusel > div {
        width: 30%;
        height: 400px;
        background: #FEFCFB;
        border: 2px solid rgba(102, 102, 102, 0.08);
        border-radius: 8px;
    }

    .trees {
        top: 5%;
        right: 25%;
    }

    .btns-fourth-section {
        top: 25%;
        right: 10%;
    }

    @media screen and ( max-width:1024px ) {
        .fourth-section {
            height: 600px;
        }
        .fourth-section .carrusel > div {
            height: 300px;
        }
        .trees {
            top: 5%;
            right: 19%;
        }
        
        .btns-fourth-section {
            top: 30%;
            right: 10%;
        }
    }

    @media screen and ( max-width:780px ) {
        .fourth-section {
            height: 500px;
        }
        .fourth-section .carrusel > div {
            height: 260px;
        }
    }

</style>