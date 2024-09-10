<script >
    import DC_Main from './DC_Main.vue';
    export default {
        data(){
            return {
                socialList:[
                    {
                        socialLink:"https://facebook.com",
                        socialIcon:"footer-facebook.png"
                    },
                    {
                        socialLink:"https://x.com",
                        socialIcon:"footer-twitter.png"
                    },
                    {
                        socialLink:"https://youtube.com",
                        socialIcon:"footer-youtube.png"
                    },
                    {
                        socialLink:"https://pinterest.com",
                        socialIcon:"footer-pinterest.png"
                    },
                    {
                        socialLink:"https://periscope.com",
                        socialIcon:"footer-periscope.png"
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
    <footer>
        <div class="dc reddit-font">
            <div class="container-xxl">
                <div class="row">
                    <div class="col-7 text-white">
                        <div class="d-flex pt-5">
                            <div class="mx-5">
                                <h4>DC COMICS</h4>
                                <ul>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                </ul>
                            </div>
                            
                            <div class="mx-5">
                                <h4>DC</h4>
                                <ul>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                </ul>
                            </div>
                            
                            <div class="mx-5">
                                <h4>SITES</h4>
                                <ul>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                    <li>Characters</li>
                                </ul>
                            </div>
                            
                        </div>
                        
                    </div>
                    <div class="col-5">
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </div>
                </div>
            </div>
        </div>
        <div class="lower-footer m-0 py-5">
            <div class="container-xxl">
                <div class="row">
                    <div class="col-6">
                        <button type="button" class="btn btn-outline-primary text-white p-3">SIGN-UP NOW!</button>
                    </div>
                    <div class="col-6 d-flex justify-content-end align-items-center">
                        <h3 class="me-3">FOLLOW US</h3>
                        <ul class="d-flex align-items-center">
                            <li v-for="(v, index) in socialList" :key="index" class="mx-3">
                                <a :href="v.socialLink">
                                    <img :src="getImagePath(v.socialIcon)" alt="">
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>

        </div>
    </footer>
</template>

<style lang="scss" scoped>

    @import url('../assets/scss/partials/components/DC_Footer.scss');

</style>