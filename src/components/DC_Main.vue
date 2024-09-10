<script >

    export default {
        data(){
            return {
                servicesList:[
                    {
                        imgSrc: "buy-comics-digital-comics.png",
                        serviceName: "DIGITAL COMICS"
                    },
                    {
                        imgSrc: "buy-comics-merchandise.png",
                        serviceName: "DC MERCHANDISE"
                    },
                    {
                        imgSrc: "buy-comics-subscriptions.png",
                        serviceName: "SUBSCRIPTION"
                    },
                    {
                        imgSrc: "buy-comics-shop-locator.png",
                        serviceName: "COMIC SHOP LOCATOR"
                    },
                    {
                        imgSrc: "buy-dc-power-visa.svg",
                        serviceName: "DC POWER VISA"
                    }
                ]
            }
        },
        methods:{
            getImagePath(imgSource){
                return new URL(`../assets/img/${imgSource}`, import.meta.url).href;
            }
        }
    }

</script>

<template>
    
    <main class="reddit-font">
        <div class="black-bg m-0 p-0">
            <div class="container-xxl">
                <h1>--&gt; Content goes here &lt;--</h1>
            </div>
        </div>
        <div class="blue-bg m-0 p-0 text-white">
            <div class="container-xxl">
                <ul class="d-flex align-items-center justify-content-between">
                    <li v-for="(v, index) in servicesList" :key="index">
                        <img :src="getImagePath(v.imgSrc)" :alt="v.serviceName" class="mx-3">
                        {{ v.serviceName }}
                    </li>
                </ul>
            </div>
        </div>
    </main>
    

</template>

<style lang="scss" scoped>

    @import url('../assets/scss/partials/components/DC_Main.scss');
    
</style>
