<template>
    <HeaderComponent />
    <main>
        <CharacterList />
    </main>
</template>

<script>
import axios from "axios";
import HeaderComponent from './components/HeaderComponent.vue'
import CharacterList from './components/CharacterList.vue';

import { store } from "./assets/data/store"
export default {
    components: { HeaderComponent, CharacterList, },
    data() {
        return {
            store
        }
    },
    created() {
        axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
            this.store.loading = true;
            this.store.characters = resp.data;
            console.log(this.store.characters);
            this.store.loading = false;
        })
    }
    
}

</script>

<style lang="scss" scoped>

</style>