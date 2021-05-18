<template>
    <section>
        <div class="circle"></div>
        <Header />
        <Content />
        <Social />
        <Swiper />
    </section>
</template>

<script>
import Header from './../components/Header'
import Content from './../components/Content'
import Social from './../components/Social'
import Swiper from './../components/Swiper'

export default {
    name:'Section',
    components: {
        Header,
        Content,
        Social,
        Swiper
    }
}
</script>

<style>

section {
    position: relative;
    width: 100%;
    min-height: 100vh;
    padding: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #161616;
}

section .circle {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #e51e2a;
    clip-path: circle(70% at right -20%);
}

@media (max-width: 991px) {
    
    section {
        padding: 150px 40px;
        flex-direction: column;
    }
}

</style>