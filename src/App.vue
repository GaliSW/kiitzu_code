<template>
    <myHeader></myHeader>
    <myBanner></myBanner>
    <myPara></myPara>
    <we-do></we-do>
    <work></work>
    <product></product>
    <location></location>
    <my-footer></my-footer>
</template>

<script>
import myHeader from "./components/header.vue";
import myBanner from "./components/banner.vue";
import myPara from "./components/top_para.vue";
import weDo from "./components/we_do.vue";
import work from "./components/work.vue";
import product from "./components/product.vue";
import location from "./components/location.vue";
import myFooter from "./components/footer.vue";

export default {
    name: "App",
    components: {
        myHeader,
        myBanner,
        myPara,
        weDo,
        work,
        product,
        location,
        myFooter,
    },
};
</script>
<style>
@import "./assets/scss/style.css";
</style>
