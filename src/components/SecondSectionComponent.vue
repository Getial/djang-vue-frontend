<template>
    <section class="second-section mt-5 bg-light d-flex flex-column align-items-center justify-content-center">
        <h2 class="my-5 fw-bolder w-75 text-center">Things you need <span class="text-danger">to do</span></h2>
        <p class="my-5 w-50 fs-3 text-secondary">We ensure that you'll embark on a perfectly planned, safe vacation at a price you can afford. </p>
        <div class="row w-100 my-5 d-flex justify-content-center">
        <div class="col-3 card bg-white rounded pt-3 position-relative">
            <!-- <img src="./assets/line1.png" class="position-absolute w-100 z-0" alt=""> -->
            <img src="../assets/Group3.png" class="card-img card-img-top" alt="...">
            <div class="card-body">
            <h5 class="card-title fw-bold">Sign Up</h5>
            <p class="card-text text-secondary fs-6">Completes all the work associated with planning and proccessing</p>
            </div>
        </div>
        <div class="col-3 card mx-5 bg-white rounded pt-3">
            <img src="../assets/Group2.png" class="card-img card-img-top" alt="...">
            <div class="card-body">
            <h5 class="card-title fw-bold">Worth of Money</h5>
            <p class="card-text text-secondary fs-6">After succesful access then book from exclusive deals & pricing</p>
            </div>
        </div>
        <div class="col-3 card bg-white rounded pt-3">
            <img src="../assets/Group1.png" class="card-img card-img-top" alt="...">
            <div class="card-body">
            <h5 class="card-title fw-bold">Exciting Travel</h5>
            <p class="card-text text-secondary fs-6">Start and explore a wide range of exciting travel experience</p>
            </div>
        </div>
        </div>
    </section>
</template>

<script>
    export default ({
        name: 'SecondSectionComponent'
    })
</script>

<style>
    .second-section {
        width: 100%;
        height: 800px;
    }

    .second-section h2,
    .third-section h2,
    .fourth-section h2,
    .sixth-section h2 {
        font-family: 'Volkhov', serif;
        font-size: 50px;
    }

    .second-section .card-img {
        width: 15%;
        margin: 10px
    }

    .card-active {
        box-shadow: 0px 16px 80px rgba(254, 147, 94, 0.2);
    }

</style>