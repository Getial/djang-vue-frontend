<template>
    <header class="row d-flex justify-content-between w-100 px-3 ms-3" style="height: 7em">
        <div class="col-3 d-flex align-items-center" style="height: 100%">
        <img style="height: 24px;" src="../assets/Logo.png" alt="">
        </div>
        <div class="col-5">
        <nav class="navbar h-100 align-items-center">
            <a class="nav-link" href="#">Home</a>
            <a class="nav-link" href="#">About</a>
            <a class="nav-link" href="#">Destination</a>
            <a class="nav-link" href="#">Tour</a>
            <a class="nav-link" href="#">Blog</a>
        </nav>
        </div>
        <div class="col-4 h-100 d-flex align-items-center justify-content-end pe-5">
        <button type="button" class="btn text-danger">Login</button>
        <button type="button" class="btn btn-danger text-white">Sign Up</button>
        </div>
    </header>
</template>

<script>
    export default ({
        name: 'HeaderComponent'
    })
</script>

<style>
    
</style>