<template>
    <section class="hero d-flex flex-column justify-content-between align-items-center mb-5">
        <div class="row h-75 w-100 mt-5">
            <div class="col-6 d-flex flex-column justify-content-between py-5">
                <h1 class="title-hero fw-bold">
                    Get started your exciting <span class="text-danger">journey</span> with us.
                </h1>
                <p class="text-secondary">
                    A Team of experienced tourism professionals will
                    provide you with the best advice and tips for your desire place. 
                    Discover Now
                </p>
                <button class="btn text-danger btn-outline-danger w-25 fs-6 px-0">Discover Now</button>
            </div>
            <div class="col-6 position-relative">
                <div class="elipse position-absolute top-50 start-50 translate-middle-x"></div>
                <img class="img-fluid w-75 position-absolute top-50 start-50 translate-middle" src="../assets/hero.png" alt="">
                <img class="w-100 ms-5 mt-5" src="../assets/aviones.png" alt="">
                <img class="img-fluid position-absolute top-50 start-0 h-25" src="../assets/27k.png" alt="">
                <img class="img-fluid position-absolute top-0 start-0 h-25" src="../assets/best-tour-awards.png" alt="">
                <img class="img-fluid position-absolute start-50 translate-middle-y h-25" src="../assets/explore.png" alt="">
            </div>
        </div>
        <div class="row h-25 w-100 mt-5 d-flex align-items-center justify-content-center" style="width: 70%;">
            <div class="nav search-nav w-75 h-75 rounded shadow d-flex justify-content-center align-items-center">
                <button class="btn col-3 nav-item d-flex flex-column justify-content-center">
                    <h5>Location <span class="text-danger fw-bolder fs-3">⌵</span></h5>
                    <p class="fs-6 text-secondary">Where are you going</p>
                </button>
                <button class="btn col-3 nav-item d-flex flex-column justify-content-center">
                    <h5>Date <span class="text-danger fw-bolder fs-3">⌵</span></h5>
                    <p class="fs-6 text-secondary">Where are will going</p>
                </button>
                <button class="btn col-3 nav-item d-flex flex-column justify-content-center">
                    <h5>Guest <span class="text-danger fw-bolder fs-3">⌵</span></h5>
                    <p class="fs-6 text-secondary">Number of guest</p>
                </button>
                <div class="col-3 nav-item h-50 d-flex flex-column justify-content-center align-items-center">
                    <button class="btn btn-danger text-white w-75 h-75 fs-4">Explore Now</button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default ({
        name: 'HeroComponent'
    })
</script>

<style>
    .hero {
        width: 90%;
        height: 999px;
    }

    .title-hero {
        font-family: 'Volkhov', serif;
        font-size: 64px;
    }

    .hero p {
        font-size: 26px;
    }

    .elipse {
        width: 500px; 
        height: 250px; 
        border: none; 
        background: #fd7e14;
        border-radius: 0 0 500px 500px;
    }

    @media screen and ( max-width:1024px ) {
        .hero {
            height: 750px;
        }
        .title-hero {
            font-size: 56px;
        }
        .hero p {
            font-size: 18px;
        }
        .elipse {
            width: 400px; 
            height: 200px;
            border-radius: 0 0 400px 400px;
        }
    }

    @media screen and ( max-width: 780px){ 
        .hero {
            height: 600px;
        }
        .title-hero {
            font-size: 42px;
        }
        .hero p {
            font-size: 14px;
        }
        .elipse {
            width: 300px; 
            height: 150px;
            border-radius: 0 0 300px 300px;
        }
    }
</style>