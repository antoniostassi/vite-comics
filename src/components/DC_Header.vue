<script >

    export default {
        data(){
            return {
                testMessage:"MESSAGE",
                headerLinks:[
                    
                    {
                        linkText:"CHARACTERS",
                        linkUrl:"#",
                    },
                    {
                        linkText:"COMICS",
                        linkUrl:"#",
                    },
                    {
                        linkText:"MOVIES",
                        linkUrl:"#",
                    },
                    {
                        linkText:"TV",
                        linkUrl:"#",
                    },
                    {
                        linkText:"GAMES",
                        linkUrl:"#",
                    },
                    {
                        linkText:"COLLECTIBLES",
                        linkUrl:"#",
                    },
                    {
                        linkText:"VIDEOS",
                        linkUrl:"#",
                    },
                    {
                        linkText:"FANS",
                        linkUrl:"#",
                    },
                    {
                        linkText:"NEWS",
                        linkUrl:"#",
                    },
                    {
                        linkText:"SHOP",
                        linkUrl:"#",
                    }
                ],
                currentLink:1
            }
        },
        methods:{

        }
    }

</script>

<template>

    <header class="reddit-font">
        <div class="container-xxl p-3 open-sans">
            <div class="row pb-3">
                <div class="col-4">
                    <img src="../assets/img/dc-logo.png" alt="" class="m-3">
                </div>
                <div class="col-8">
                    <ul class="d-flex align-items-center justify-content-end">
                        <li v-for="(v, index) in headerLinks" @click="currentLink = index" :key="index" class="mx-2 px-1" ><a :href="v.linkUrl" :class="{'active':index == currentLink}">{{v.linkText}} <div v-show="index == currentLink"></div></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
    

</template>

<style lang="scss" scoped>

    @import url('../assets/scss/partials/components/DC_Header.scss');

</style>
