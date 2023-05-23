<template>
    <header class="header">
        Header
    </header>

</template>

<script>
    export default{

        mounted(){
            window.addEventListener('resize', this.resize)
        },

        beforeUnmount() {
        console.log("beforeUnmount");
        console.log("Estado:", this.name);

    },
    unmounted() {
        console.log("unmounted");

    },
    methods:{
        resize($evt){
            console.log($evt);
        },
    }
    }
</script>

<style>
    .header {
        background: #000;
        color: #fff;
    }
</style>