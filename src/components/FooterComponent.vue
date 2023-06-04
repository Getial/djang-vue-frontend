<template>
  <footer class="position-relative d-flex flex-column align-items-center justify-content-end w-100 ">
    <div class="modal-footer position-absolute w-75 bg-danger rounded-4 d-flex flex-column justify-content-center">
      <h3 class="text-light text-center mb-4">
        Subscribe and get exclusive
        <br />
        deals & offer
      </h3>
      <div class="bg-white rounded d-flex justify-content-center mt-2">
        <form class="d-flex align-items-center justify-content-between">
          <input class="me-2 border-0 w-75" type="search" placeholder="✉ Enter Your mail" aria-label="Search">
          <button class="btn bg-danger text-white" type="submit">Subscribe</button>
        </form>
      </div>
      <img src="../assets/circles.png" class="position-absolute" alt="">
      <img src="../assets/treees2.png" class="s position-absolute" alt="" id="modal-footer-tree">
    </div>
    <div class="footer-details-container bg-light w-100 h-75 d-flex flex-column align-items-center justify-content-end">
      <div class="footer-details w-75 d-flex justify-content-evenly">
        <div class="d-flex flex-column justify-content-between">
          <img src="../assets/Logo.png" class="m-1" alt="">
          <p class="fs-6 text-secondary">
            Book your trip in minute, get full
            <br/>
            Control for much longer.
          </p>
          <div class="icons-social-network mb-5">
            <img src="../assets/icon-facebook.png" alt="">
            <img src="../assets/icon-instagram.png" alt="">
            <img src="../assets/icon-twiter.png" alt="">
          </div>
        </div>
        <div class="lists-footer">
          <ul class="d-flex flex-column">
            <h5 class="fw-bold">Company</h5>
            <li class="my-2">About</li>
            <li class="my-2">Careers</li>
            <li class="my-2">Logistic</li>
            <li class="my-2">Privacy & Policy</li>
          </ul>
        </div>
        <div class="lists-footer">
          <ul class="d-flex flex-column">
            <h5 class="fw-bold">Contact</h5>
            <li class="my-2">Help/FAQ</li>
            <li class="my-2">Press</li>
            <li class="my-2">Affiliates</li>
          </ul>
        </div>
        <div class="lists-footer">
          <ul class="d-flex flex-column">
            <h5 class="fw-bold">More</h5>
            <li class="my-2">Press Centre</li>
            <li class="my-2">Our Blog</li>
            <li class="my-2">Low fare tips</li>
          </ul>
        </div>
      </div>
      <div class="copyright w-75 d-flex align-items-center justify-content-between mx-3 border-top text-secondary">
        <p>
          Copyright, Trabook 2023. All rights reserved.
        </p>
        <p>
          Terms & Conditions
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
    export default ({
        name: 'FooterComponent'
    })
</script>

<style>


    footer {
        height: 900px;
        width: 100%;
    }

    .modal-footer {
        height: 38%;
        top: 3%;
    }

    .modal-footer h3 {
        font-size: 45px;
    }

    .modal-footer > div {
        width: 60%;
        height: 15%;
        z-index: 1;
    }
    .modal-footer > div form {
        width: 95%;
        height: 100%;
    }

    .modal-footer > img {
        height: 55%;
        top: 45%;
        left: 0;
        z-index: 0;
    }

    #modal-footer-tree {
        height: 40%;
        top: 2%;
        left: 85%;
    }

    .footer-details {
        width: 100%;
        height: 50%;
    }

    .footer-details > div {
        width: 20%;
    }
    .footer-details div:nth-child(1) {
        width: 30%;
    }
    .footer-details div:nth-child(1) > img {
        width: 40%;
    }

    .lists-footer ul {
        list-style-type: none;
        height: 100%;
    }

    .lists-footer li {
        color: #666666;
    }

    .copyright {
        height: 20%;
    }

    @media screen and ( max-width:1024px ) {
        .footer-details div:nth-child(1) > img {
            width: 50%;
        }
        .modal-footer h3 {
            font-size: 40px;
        }
        .modal-footer > div {
            width: 60%;
            height: 12%;
        }
    }
</style>