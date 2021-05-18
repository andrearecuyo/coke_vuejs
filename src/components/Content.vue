<template>
    <div class="content">
        <div class="textBox">
            <h2>Taste the Feeling</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum soluta quae enim fuga, nisi nobis neque explicabo optio dolores animi iste eaque ab iure quaerat repudiandae nemo beatae ullam dicta!
            Cupiditate quo vel a ipsam voluptatem corrupti nam architecto ipsa, nesciunt ea eveniet illo facere necessitatibus assumenda quibusdam reprehenderit, rem quia enim mollitia aliquam quas fugiat ducimus tempora sit! Nam?</p>
            <a href="#">Learn More</a>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>

.content {
    position: relative;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.content .textBox {
    position: relative;
    max-width: 650px;
    margin-right: 20px;
}

.content .textBox h2 {
    color: #fff;
    font-size: 3em;
    margin-bottom: 10px;
    line-height: 1.4em;
    font-weight: 700;
}

.content .textBox p {
    color: #fff;
}

.content .textBox a {
    display: inline-block;
    margin-top: 20px;
    padding: 8px 20px;
    background: #e51e2a;
    border: 2px solid #e51e2a;
    color: #fff;
    border-radius: 40px;
    font-weight: 500;
    letter-spacing: 1px;
    text-decoration: none;
}

.content .textBox a:hover {
    background: transparent;
    border: 2px solid #fff;
    color: #fff;
}

@media (max-width: 991px) {
    
    .content {
        flex-direction: column;
    }

    .content .textBox {
        max-width: 100%;
    }
}

</style>