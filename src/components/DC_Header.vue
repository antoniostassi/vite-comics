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

</template>

<style lang="scss" scoped>


    ul {
        li {
            font-size:0.9rem;
            div {
                position:relative;
                width:100%;
                height:5px;
                background-color:#0282F9;
            }
        }
    }

    a {
        color:black;
        text-decoration:none;
        &:hover {
            color:#0282f9a4;
        }
    }

    .active {
        color:#0282F9 !important;
    }

</style>
