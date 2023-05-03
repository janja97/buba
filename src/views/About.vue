<template>
    <div>
        <NavbarBlack />
        <!-- destop  -->
        <div class="container-fluid about d-none d-md-block">
            <div class="col-5 about-me">
                <div class="my-photo img-container">
                    <img src="me/faruk.jpeg" alt="me">
                </div>
                <div class="content">
                    <h4>Hello</h4>
                    <p>My name is Faruk and I'm a freelance photographer specialising in portraits, weddings and lifestyle photography. 
                        I was interested in photography from a young age and I have been involved in photography for several years.
                    </p>
                    <p>
                        I was born in Dubrovnik and I am now based in London and I'm available to hire for commercial projects worldwide. 
                    </p>
                    <p>
                        I use the latest photography equipment to achieve the best results and guarantee to deliver the highest quality photography on time.
                    </p>                                                
                        <a href="mailto:photographybuba@gmail.com" class="mail"> <img src="/image/icons/arrow.png" alt="arrow">photographybuba@gmail.com</a>
                </div>
                <hr>
                <div class="social-link">
                    <a href="https://instagram.com/bubaaphotography?igshid=YmMyMTA2M2Y="><img src="/image/icons/instagram-black.png" alt="instagram" class="ico"></a>
                    <a href="https://www.facebook.com/profile.php?id=100090263107531"><img src="/image/icons/facebook-black.png" alt="facebook" class="ico"></a>
                    <a href="https://wa.me/00447931588770"><img src="/image/icons/whatsapp-black.png" alt="whatsApp" class="ico"></a>
                    <a href="mailto:photographybuba@gmail.com"><img src="/image/icons/email-black.png" alt="whatsApp" class="ico"></a>
              
                </div>
            </div>
        </div>
        <!-- mobile -->
        <div class="about-me-mobile d-md-none container" style="margin-top:100px;">
            <div class="col-12">
                <img src="me/faruk.jpeg" alt="me" style="width: inherit;">
            </div>
            <div class="content mt-5">
                <h4>Hello</h4>
                    <p>My name is Faruk and I'm a freelance photographer specialising in portraits, weddings and lifestyle photography. 
                        I was interested in photography from a young age and I have been involved in photography for several years.
                    </p>
                    <p>
                        I was born in Dubrovnik and I am now based in London and I'm available to hire for commercial projects worldwide. 
                    </p>
                    <p>
                        I use the latest photography equipment to achieve the best results and guarantee to deliver the highest quality photography on time.
                    </p>   
                        <a href="mailto:photographybuba@gmail.com" class="mail"> <img src="/image/icons/arrow.png" alt="arrow">photographybuba@gmail.com</a>
                </div>
            <hr>
            <!-- <div class="social-link">
                <a href="https://instagram.com/bubaaphotography?igshid=YmMyMTA2M2Y="><img src="/image/icons/instagram-black.png" alt="instagram" class="ico"></a>
                <a href="https://www.facebook.com/profile.php?id=100090263107531"><img src="/image/icons/facebook-black.png" alt="facebook" class="ico"></a>
                <a href="https://wa.me/00447931588770"><img src="/image/icons/whatsapp-black.png" alt="whatsApp" class="ico"></a>
                <a href="mailto:photographybuba@gmail.com"><img src="/image/icons/email-black.png" alt="whatsApp" class="ico"></a>
            
            </div> -->
        </div>
    </div>
</template>
<script>
import NavbarBlack from '../components/NavbarBlack.vue'

export default {
name: 'AppAbout',
//   class: horizontal (2x1), vertican (1x2), none (2x2), big (4x4)

components: {
    NavbarBlack,
    },
    mounted() {
    var checkbox = document.getElementById("menuToggle");
    if (checkbox.checked) {
      checkbox.checked = false;
    }
  }
};

</script>

<style setup>
.about {
    background-image:url('../assets/faruk.jpeg');
    padding-top:200px; 
    position: relative;
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
    margin-bottom: 100px;
    width: 100%;
    height: calc(100vh - 100px);
    margin-top: 80px;
}
.about-me {
    background-color: white;
    position: absolute;
    top: 50%;
    left: 55%;
    max-width: 1100px;
    padding: 40px 50px;
    z-index: 2;
    -webkit-transform: translate(-50%, -50%);
    -moz-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);

}
.img-container img {
    position: absolute;
    top: 50%;
    left: -300px;
    width: 300px;
    height: auto;
    -webkit-transform: translate(0, -50%);
    -moz-transform: translate(0, -50%);
    transform: translate(0, -50%);
}
.content {
    border-bottom: 1px solid #F0F0F0;
    padding-bottom: 20px;
}
.mail {
    color: black;
    text-decoration: underline;
}
.mail img {
    width: 15px;
    height: 15px;
    margin-right: 5px;
}
.social-link{
    width: auto;
    float: right;
    background-color: #F0F0F0;

    height: 50px;
    display: flex;
}
.link {
    margin: 0px 0px;
    border-right: 1px solid #d9d9d9;
    width: 50px;
    height: 50px;
    display: grid;
    align-items: center;
    justify-content: center;
}
.link img {
    width: 10px;
}
.link:last-child {
    border: none;
}
.ico {
    width: 15px;
    height: 15px;
    margin: 20px;

}

</style>
    