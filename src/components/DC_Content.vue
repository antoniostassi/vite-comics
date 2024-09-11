<script>
    export default{
        data(){
            return{

            };
        },
        props:{
            comicsList: Object
        }
    }
</script>

<template>
    <div class="comic-card">
        <img :src="comicsList.thumb" :alt=comicsList.series>
    </div>
</template>


<style lang="scss" scoped>
  @import url("../assets/scss/partials/components/DC_Content.scss");
</style>