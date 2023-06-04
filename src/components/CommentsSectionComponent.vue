<template>
    <section class="fifth-section mt-2 bg-light d-flex justify-content-center">
        <div class="col-4 d-flex flex-column justify-content-center">
        <h2  class="fs-1 fw-bolder mb-2">
            What people say 
            <br/>
            <span class="text-danger">about us.</span>
        </h2>
        <p class="text-secondary my-5">
            Our Clients send us bunch of smiles with our
            <br>
            services and we love them
        </p>
        <div class="w-100 d-flex mt-2"> <!--buttons-->
            <button class="arrow-left-btn me-5 border text-secondary border-dark-subtle">➔</button>
            <button class="arrow-right-btn bg-danger text-white fs-4">➔</button>
        </div>
        </div>
        <div class="col-5 position-relative">
        <div class="card-container w-75 px-4 pt-3 rounded position-absolute shadow">
            <img src="../assets/person1.png" class="w-25 position-absolute p-2 border border-light rounded-circle" alt="">
            <p class="mb-5">
            “On the Windows talking painted pasture yet its express parties use. Sure last upon he same as knew next. Of believed or diverted no.”
            </p>
            <h4 class="fs-6 mb-0">Mike Taylor</h4>
            <p class="text-secondary">Lahore, Pakistan</p>
        </div>
        <div class="card-container w-75 px-4 pt-3 bg-light rounded position-absolute top-50 shadow">
            <p class="mb-5">
            “On the Windows talking painted pasture yet its express parties use. Sure last upon he same as knew next. Of believed or diverted no.”
            </p>
            <h4 class="fs-6 mb-0">Chris Thomas</h4>
            <p class="text-secondary">CEO of Red Button</p>
        </div>
        <img src="../assets/aviones2.png" class="position-absolute" style="top: 15%; right: -10%" alt="">
        </div>
    </section>
</template>

<script>
    export default ({
        name: 'CommentsSectionComponent'
    })
</script>
    
<style>
    .fifth-section {
        width: 100%;
        height: 650px;
    }

    .card-container img {
        top: -40%;
        left: -15%;
    }

    .card-container:nth-child(1) {
        background-color: white;
        top:36%;
        left: 15%;
        z-index: 1;
    }

    .card-container:nth-child(2) {
        background-color: #F7F8FC;
        opacity: 0.7;
        left: 20%;
        z-index: 0;
    }

    .card-container p:nth-child(3) {
        font-size: 14px;
    }
</style>