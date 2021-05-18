<template>
    <ul class="social">
        <li><a href=""><i class="icon fab fa-facebook-f"></i></a></li>
        <li><a href=""><i class="icon fab fa-twitter"></i></a></li>
        <li><a href=""><i class="icon fab fa-instagram"></i></a></li>
    </ul>
</template>

<script>
export default {
    
}
</script>

<style>

    .social {
        position: absolute;
        bottom: 40px;
        left: 90px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .social li {
        list-style: none;
    }
    
    .social li a {
        display: inline-block;
        margin-left: 15px;
        background: #222;
        color: #fff;
        width: 50px;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        transition: 0.2s ease-in-out;
        text-decoration: none;
    }
    
    .social li a:hover {
        background: #e51e2a;
        transform: translateY(-10px);
    }

    .social li a i {
        transform: scale(0.5);
        font-size: 40px;
        color: #fff;
    }

    @media (max-width: 991px) {
    
    .social {
        position: absolute;
        left: 30px;
    }
}

</style>