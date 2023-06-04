<template>
    <section class="sixth-section w-100 d-flex flex-column align-items-center justify-content-evenly">
        <h2  class="fs-1 fw-bolder">Get update with <span class="text-danger">latest blog</span></h2>
        <div class="carrusel d-flex w-75 mb-3 justify-content-evenly align-items-center">
            
            <div class="bg-white rounded d-flex flex-column justify-content-between" v-for="blog in blogs" :key="blog.id">
                <img :src="blog.image" class="w-100 rounded" alt="...">
                <h5 class="fs-5 ps-1 mt-2">{{ blog.title }}</h5>
                <p class="text-secondary fs-6 ms-1 mt-0">{{ new Date(blog.pub_date).toLocaleDateString('es-us', { year:"numeric", month:"short", day:"numeric"}) }}</p>
            </div>
            
        </div>
        <div class="d-flex justify-content-center mt-2">
            <button class="carousel-indicator"></button>
            <button class="carousel-indicator bg-danger mx-4"></button>
            <button class="carousel-indicator"></button>
        </div>
    </section>
</template>

<script>
    import axios from 'axios'

    export default ({
        name: 'BlogsComponent',

        data() {
            return {
                blogs: []
            }
        },

        mounted() {
            axios.get('http://127.0.0.1:8000/api/blogs/')
            .then(response => {
                this.blogs = response.data
                console.log(this.blogs[0].pub_date);
            })
            .catch(error => {
                console.log(error);
            })
        }
    })
</script>

<style>
    .sixth-section h2 {
        font-family: 'Volkhov', serif;
        font-size: 50px;
    }
    .sixth-section {
        height: 750px;
    }

    .sixth-section .carrusel > div {
        width: 22%;
        height: 360px;
        background: #FEFCFB;
        border: 2px solid rgba(102, 102, 102, 0.08);
        border-radius: 8px;
    }

    .carousel-indicator {
        width: 10px;
        height: 10px;
        border-radius: 5px;
        border: none;
    }

    @media screen and ( max-width:1024px ) {
        .sixth-section {
            height: 600px;
        }
    }

    @media screen and ( max-width:780px ) {
        .sixth-section {
            height: 500px;
        }
    }
</style>