<template>
    <header>
        <a href="#">
            <img src="../assets/img/logo.png" alt="CocaCola Logo" class="logo">
        </a>
        <div class="toggle" @click="toggleMenu">
            <i class="fas fa-bars" id="menuIcon"></i>
        </div>
        <ul class="navigation">
            <li><router-link class="nav-item" to="/">Home</router-link></li>
            <li><router-link class="nav-item" to="/about">About</router-link></li>
            <li><router-link class="nav-item" to="/">What's New</router-link></li>
            <li><router-link class="nav-item" to="/">Contact</router-link></li>
        </ul>
    </header>
</template>

<script>
export default {
    data () {
      return {
        active: false
      }
    },
    methods: {
      toggleMenu() {
        const menuToggle = document.querySelector('.toggle');
        const navigation = document.querySelector('.navigation');
        const menuIcon   = document.querySelector('#menuIcon');

        menuToggle.classList.toggle('active')
        navigation.classList.toggle('active')        
        if(navigation.classList.contains('active')){
            menuIcon.classList.remove('fa-bars')
            menuIcon.classList.add('fa-times')
        }else{
            menuIcon.classList.add('fa-bars')
            menuIcon.classList.remove('fa-times')
        }
      }
    }
  }
</script>

<style>

header {
    position:absolute;
    top:0;
    left:0;
    width: 100%;
    padding: 40px 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header .logo {
    position: relative;
    max-width: 150px;
}

header .navigation {
    position: relative;
    display: flex;
}

header .navigation li {
    list-style: none;
}

header .navigation li .nav-item{
    display: inline-block;
    color: #fff;
    font-weight: 500;
    text-decoration: none;
    margin-left: 40px;
    padding: 10px;
}

header .navigation li .nav-item:hover{
    color: #e51e2a;
    background: #fff;
    border-radius: 40px;
    padding: 10px;
}

@media (max-width: 991px) {
    
    header {
        padding: 30px;
    }

    header .navigation {
        display: none;
    }


    header .navigation.active {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: #e51e2a;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 10;
    }
    
    header .navigation li .nav-item{
        font-size: 3em;
        font-weight: 600;
        margin-left: 0;
    }
    
    header .navigation li .nav-item:hover{
        color: #e51e2a;
        background: #fff;
        border-radius: 40px;
        padding: 10px 60px;
    }
    
    .toggle {
        position: relative;
        width: 30px;
        height: 30px;
        cursor: pointer;
        z-index: 1000;
    }

    .toggle.active {
        position: fixed;
        right: 40px;

    }

    .toggle i {
        color: #fff;
        font-size: 25px;
    }
}
</style>