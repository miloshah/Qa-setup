<template>
    <div class="web-elem-wrapper">
        <div class="element-content"
            @mouseover="hover = true"
            @mouseleave="hover = false"
            :class="{ active: hover}"
        >
         <h2 class="heading">Food Item</h2>
        </div>
    </div>
</template>

<style lang="scss">
.active{
    opacity: 1 !important;
}
.web-elem-wrapper{
    height: 300px;
    flex: 1;
    margin: 0 20px;

    .element-content{
        opacity: 0.8;
        height: 100%;
        background: url("../assets/1.jpg") no-repeat;
        background-color: #efefef;
        background-size: cover;
        background-position: 50%;

        .heading{
            text-align: center;
            line-height: 40px;
            background-color: black;
            color: white;
            margin: 0;
        }
    }
}

</style>

<script>
export default {
    name:"WebElements",
    data: function(){
        return{
            hover: false,
        }
    }
}
</script>