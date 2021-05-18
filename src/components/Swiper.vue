<template>
  <div class="imgBox">
    <swiper 
        :effect="'coverflow'" 
        :grabCursor="true" 
        :centeredSlides="true" 
        :slidesPerView="'auto'" 
        :coverflowEffect="{
            'rotate': 0,
            'stretch': 0,
            'depth': 100,
            'modifier': 1,
            'slideShadows': true
        }" 
        :pagination="false" 
        class="mySwiper"
       :loop="true">
        <swiper-slide>
            <img src="@/assets/img/cocacola1.png" />
        </swiper-slide>
        <swiper-slide>
            <img src="@/assets/img/cocacola2.png" />
        </swiper-slide>
        <swiper-slide>
            <img src="@/assets/img/cocacola3.png" />
        </swiper-slide>
        <swiper-slide>
            <img src="@/assets/img/cocacola4.png" />
        </swiper-slide>
        <swiper-slide>
            <img src="@/assets/img/cocacola5.png" />
        </swiper-slide>
        <swiper-slide>
            <img src="@/assets/img/cocacola6.png" />
        </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';

import "swiper/components/effect-coverflow/effect-coverflow.min.css"
import "swiper/components/pagination/pagination.min.css"

import "swiper/swiper-bundle.min.css";

// import Swiper core and required modules
import SwiperCore, {
  EffectCoverflow,Pagination
} from 'swiper/core';

// install Swiper modules
SwiperCore.use([EffectCoverflow,Pagination]);


export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
        
        
    };
  },
  methods: {
    
  }
  
}
</script>

<style>
.swiper-container {
  width: 100%;
  padding-top: 50px;
  padding-bottom: 50px;
}

.swiper-slide {
  background-position: center;
  background-size: cover;
  width: 200px;
  height: 460px;
  justify-content: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  position: absolute;
  bottom: 0;
  max-height: 100%;
}

.swiper-container-3d .swiper-slide-shadow-left,
.swiper-container-3d .swiper-slide-shadow-right  {
    background-image: none;
}

.imgBox {
  display: flex;
  width: 750px;
  justify-content: flex-end;
}

.imgBox img {
  max-width: 150px;
}

@media (max-width: 991px) {
  
    .imgBox {
        max-width: 100%;
    }

    .swiper-slider {
      height: 300px;
    }
}

</style>