<template>
    <div>
        <home-header></home-header>
        <price-list></price-list>
        <home-footer></home-footer>
        
    </div>
</template>

<script>
import PriceList from './components/PriceList'
import HomeHeader from './components/Header'
import HomeFooter from './components/Footer'
export default {
    name:"Home",
    components:{
        PriceList,
        HomeHeader,
        HomeFooter
    }
}
</script>

<style lang="stylus" scoped>
    
</style>