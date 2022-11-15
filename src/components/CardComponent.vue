<template>
    <div class="card p-3 text-center mt-3 ">
        <img :src="character.img" alt="">
        <div class="card-body">
            <h3 class="text-uppercase">{{ character.name }}</h3>
            <h4>{{ character.category }}</h4>
            <h4>{{ character.status }}</h4>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        character: Object
    }
}
</script>


<style lang="scss" scoped>
@import "../assets/scss/general.scss";
.card {
    height: 450px;
    background-color: #2e3a46;
    
    h3 {
        color: white;
        font-size: medium;
        margin: 0.5rem 0;
    }

    h4 {
        color: $text_color;
        font-size: small;
        font-weight: 300;
    }

    img{
        max-height: 300px;
        object-fit: cover;
    }
}
</style>