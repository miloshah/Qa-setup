<template>
    <div class="feature-wrapper">
        <div class="image-wrapper">
            <span class="media-credit" v-if="!isFireFox">&copy;Paul Drinkwater/NBC/Getty Images; Alice S. Hall/NBC/Getty Images; Terry O'Neill/Terry O'Neill/Terry O'Neill/</span>
        </div>
        <div class="title-wrapper">
            <div class="content">
                <h2>These Unique Sizzlers At Mystery Of Spice Will Make You Crave For More</h2>
                <p>The origin of the sizzler probably goes back the teppanyaki-sizzled dishes of Japan. From there it moved to the US after World War II, and became popular in the 1950s. Sizzler steaks are generally prepared using high-heat to sear the outside and leaving the inside moist. Once plated, the steak lets off a dramatic hiss of steam, which is its great appeal.</p>
            </div>
        </div>

    </div>
</template>

<style lang="scss">

.feature-wrapper{
    height: calc(100vh - 126px);
    display: flex;
    margin-bottom: 30px;

    .image-wrapper{
        flex:1;
        height: 100%;
        background: url("../assets/FeatureImg.jpg") no-repeat;
        background-color: #efefef;
        background-size: cover;
        background-position: 50%;
        position: relative;

        .media-credit{
            position: absolute;
            bottom: 0;
            left:0;
            right:0;
            color: azure;
            text-align: center;
            font-size: 10px;

            @media screen and (max-width: 600px){
                font-size: 7px;
            }
        }
    }

    .title-wrapper{
        flex:1;
        height: 100%;
        display: flex;
        align-items: center;
        
        .content{
            padding: 0 20px;

            @media screen and (max-width: 500px){
                font-size: 12px;
            }
        }
    }
}

</style>

<script>
export default {
    name:"FeatureImage",
    computed:{
        isFireFox: function(){
            return window.isFireFox;
        }
    }
}
</script>