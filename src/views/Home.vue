<template>
  <div>
    <Navbar />
    <Header />
    <!-- content -->
    <div style="margin-top:100px;">
      <p class="col-12 col-md-6 text-black text">
        I photograph those heart-warming, beautiful and real moments, I freeze them in time and I tell your story, creating images that will last you a lifetime.
      </p>
      <Carousel v-bind="settings" :breakpoints="breakpoints">
        <Slide v-for="slide in images" :key="slide">
          <div class="carousel__item">
            <img :src="slide.UrlImg" alt="" style="width:100%; height:auto;">
          </div>
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>
      <!-- secund slider -->
      <p class="col-12 col-md-6 text-black text" style="margin-top:80px;">
        Even if you don't like posing or feel uncomfortable in front of the camera - I got you covered. I will give you tips and guide you through the shoot in a way that you won't feel any pressure.      </p>
      <Carousel v-bind="settings" :breakpoints="breakpoints">
        <Slide v-for="slide in images2" :key="slide">
          <div class="carousel__item">
            <img :src="slide.UrlImg" alt="" style="width:100%; height:auto;">
          </div>
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>
       <!-- three slider -->
      <p class="col-12 col-md-6 text-black text" style="margin-top:80px;">
        Photographs are a powerful and invaluable investment. They can capture energy, emotion and movement. One single moment in time can evoke a thousand feelings    
      </p> 
      <Carousel v-bind="settings" :breakpoints="breakpoints">
        <Slide v-for="slide in images3" :key="slide">
          <div class="carousel__item">
            <img :src="slide.UrlImg" alt="" style="width:100%; height:auto;">
          </div>
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>

    </div>
    <Form />
  </div>
</template>
<script>
import Navbar from '../components/Navbar.vue'
import Header from '../components/Header.vue'
import Form from '../components/Form.vue'
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'Breakpoints',
  components: {
    Navbar,
    Header,
    Form,
    Carousel,
    Slide,
  },

  data: () => ({
    // carousel settings
    settings: {
      itemsToShow: 1,
      snapAlign: 'center',
    },
    // breakpoints are mobile first
    // any settings not specified will fallback to the carousel settings
    breakpoints: {
      // 700px and up
      700: {
        itemsToShow: 3,
        snapAlign: 'center',
      },
      // 1024 and up
      1024: {
        itemsToShow: 5,
        snapAlign: 'start',
      },
    },
    // images array
    images: [
      { id: '1' ,type: '2', UrlImg:'people/peope (24).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '5' ,type: '2', UrlImg:'people/peope (19).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '2' ,type: '2', UrlImg:'people/peope (17).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '3' ,type: '2', UrlImg:'people/peope (6).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '5' ,type: '2', UrlImg:'people/peope (39).jpeg' , alt:'image-slug', class:"vertical" },
    ],
    images2: [
      { id: '1' ,type: '2', UrlImg:'people/peope (36).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '5' ,type: '2', UrlImg:'people/peope (38).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '2' ,type: '2', UrlImg:'people/peope (30).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '3' ,type: '2', UrlImg:'people/peope (31).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '5' ,type: '2', UrlImg:'people/peope (37).jpeg' , alt:'image-slug', class:"vertical" },
    ],
    images3: [
      { id: '1' ,type: '2', UrlImg:'people/peope (11).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '5' ,type: '2', UrlImg:'people/peope (27).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '2' ,type: '2', UrlImg:'people/peope (9).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '3' ,type: '2', UrlImg:'people/peope (10).jpeg' , alt:'image-slug', class:"vertical" },
      { id: '5' ,type: '2', UrlImg:'people/peope (12).jpeg' , alt:'image-slug', class:"vertical" },
    ],
  }),
})
</script>

<style setup>
.me {
  background-color: #75402824;
}

.text {
  display: flex;
  justify-content: center;
  text-align: center;
  margin: 0 auto;
  padding-bottom: 100px;
}



</style>