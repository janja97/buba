<template>
    <div class="container-fluid text-center header">
        <div class="wrapper">
            <h1 class="title mb-4">BUBAPHOTOGRAPHY</h1>
            <hr class="first-hr mx-auto">
            <hr class="last-hr mx-auto mb-4">
            <h5 class="small-title mb-4" style="color:white;">Portrait, weddings, lifestyle and fashion photography.</h5>
            <div class="social d-flex justify-content-center">
                <a href="https://instagram.com/bubaaphotography?igshid=YmMyMTA2M2Y="><img src="/image/icons/instagram.png" alt="instagram" class="icons"></a>
                <a href="https://www.facebook.com/profile.php?id=100090263107531"><img src="/image/icons/facebook.png" alt="facebook" class="icons"></a>
                <a href="https://wa.me/00447931588770"><img src="/image/icons/whatsApp.png" alt="whatsApp" class="icons"></a>
                <a href="mailto:photographybuba@gmail.com"> <img src="/image/icons/email.png" alt="mail" class="icons"></a>
            </div>
        </div>
    </div>
   
</template>

<script>
export default {
    name: "AppHeader",
};
</script>

<style setup>
.header {
    padding-top:200px; 
    background-image:url('/public/bac/svadba.jpeg');
    position: relative;
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
    /* margin-bottom: 100px; */
    width: 100%;
    height: calc(100vh - 100px);
    
}
@media screen and (max-width:991px){
    .header {
        background-image: url('/public/bac/svadba-mob.jpeg');
    }
    
}

.header::after {
    position: absolute;
    content: "";
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: #000;
    opacity: 0.4;
}
.wrapper {
    position: relative;
    top: 40%;
    left: 50%;
    text-align: center;
    z-index: 1;
    -webkit-transform: translate(-50%, -35%);
    -moz-transform: translate(-50%, -35%);
    transform: translate(-50%, -35%);
    margin: 0;
    padding: 0;
    border: 0;
    outline: 0;
    background: transparent;
}
/* @media screen and (max-width: 768px){
    .header {
        height: 100vh;
        background-position: right !important;

    }
    
}
@media screen and (max-width: 420px){
    .header {
        background-position: -460px !important;

    }
    
} */
/* title */
h1,h5, hr {
    color: white !important;
    letter-spacing:2px;
}
hr {
    opacity: 1;
    margin: 5px auto !important;
}
/* hr */
.first-hr {
    width: 60px;
}
.last-hr {
    width: 40px;
}

/* icons */
.icons {
    width: 15px;
    height: 15px;
    margin: 0px 5px;
}
.social a:not(:last-child)::after {
    content: "-";
    color: white;
}
.social:last-child::after {
    display: none;
}




</style>
  