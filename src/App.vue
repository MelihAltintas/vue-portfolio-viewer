<template>
<div id="app">

    <div class="row">
        <div class="col-md-3">
            <PortfolioItem borderColor="#e74c3c" :img="require('@/assets/layout-06.jpg')" />
        </div>

        <div class="col-md-3">
            <PortfolioItem :img="require('@/assets/layout-05.jpg')" />
        </div>

        <div class="col-md-3">
            <PortfolioItem :img="require('@/assets/layout-04.jpg')" />
        </div>
    </div>
</div>
</template>

<script>
import PortfolioItem from './components/PortfolioItem.vue'

export default {
    name: 'App',
    components: {
        PortfolioItem
    }
}
</script>

<style>

</style>
