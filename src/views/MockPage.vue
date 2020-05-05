<template>
    <div>
        <Header></Header>
        <SocialShare></SocialShare>
        <FeatureImage></FeatureImage>
        <div class="content-wrapper">
            <div class="container">
            <WebElements></WebElements>
            <WebElements></WebElements>
            <WebElements></WebElements>
            <WebElements></WebElements>
            </div>
            <div class="content-desc">
                <p>Food is an important factor of life that fuels every individual across the globe. Everyday, millions of Canadians across the country consume large quantities of food without acknowledging where this food was grown and processed. Individuals think they are purchasing freshly grown vegetables and fruits at the grocery store, however a large portion of the foods sold are exported from different countries. Unknowingly, the consumer buys exported foods that have been stocked up with preservatives too keep it fresh through out transportation. It is important for Canadians to be aware of where their fruits and vegetables are being grown and sent from so they can know how many preservatives have been added to keep them fresh. A lot of these additives have the ability to compromise the body’s structure and function and can cause serious harm.</p>
                <p>Based on the food diary I kept, it is seen that a large percentage of my food is produced in Canada. This is most probably due to the fact that my diet doesn’t consist of much variety from day to day, and it is mostly processed fast food. Assuming the average Canadian diet is like mine, I would say that Canadians are local global consumers. However, it would not be accurate to say that most Canadians share the same diet as me. In my perspective, a persons diet depends on the lifestyle that they live. It can vary depending on whether they are working or going to school, whether they have time to cook a full meal or only a five-minute microwavable meal. It also depends on their health choices; some people may not wish to consume processed fast food meals everyday while others don’t mind it.</p>
            </div>
        </div>
        <Footer></Footer>
    </div>
</template>

<style lang="scss">
    .content-wrapper{
        padding:0 20px;

        @media screen and (max-width: 500px){
                font-size: 12px;
            }

        .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;

        .web-elem-wrapper{
            &:first-child{
                margin-left: 0;
            }

            &:last-child{
                margin-right: 0;
            }
        }
    }
    }

</style>

<script>
import Header from "@/components/Header.vue";
import SocialShare from "@/components/SocialShare.vue";
import FeatureImage from "@/components/FeatureImage.vue";
import WebElements from "@/components/WebElements.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "MockPage",
  components: {
    Header,
    SocialShare,
    FeatureImage,
    WebElements,
    Footer
  },
};
</script>