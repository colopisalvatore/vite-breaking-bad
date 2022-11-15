<template>
    <div class="text-center">
        <h4 class="text-center">Found {{ store.characters.length }} characters</h4>
    </div>
</template>

<script>
import { store } from "../assets/data/store"

export default {
    name: 'ResultCount',
    data() {
        return {
            store
        }
    }
}
</script>

<style lang="scss" scoped>
h4 {
    color:white;
}

</style>