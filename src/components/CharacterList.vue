<template>
    <section class="container"> 
        <div class="row">
            <div class="col-12 col-sm-6 col-md-4 col-lg-3 mb-5" v-for="item in store.characters" :key="item.id">
                <CardComponent :character="item" />
            </div>
        </div>
    </section>

</template>

<script>
import { store } from '../assets/data/store';
import CardComponent from './CardComponent.vue';



export default {
    name: "CharacterList",
    components: { CardComponent, },
    data() {
        return {
            store
        }
    }
}
</script>

<style lang="scss" scoped>
.my_container {
    width: 80%;
    margin: 0 auto;
    background-color: white;
}
</style>