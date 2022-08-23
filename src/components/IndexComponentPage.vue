<template>
    <div class="logo forHeader">
        <div class="wrapper">
            <div class="logo-left">
                <img class="indexLogo" src="../img/indexLogo.png" alt="indexLogo">
            </div>
            <div class="logo-right">
                <hr class="pinkLine">
                <p class="indexBanner">
                    <span class="indexBannerBold">THE BRAND</span><br>OF LUXERIOUS <span class="indexBannerPink">FASHION</span>
                </p>
            </div>
        </div>
    </div>
    <div class="sentenses container">
        <div class="sentensesTop">
            <div class="cardSentensesTop image-1">
                <p class="sentensesText">30% OFF<br><span class="sentensesTextPink">FOR WOMEN</span></p>
            </div>
            <div class="cardSentensesTop image-2">
                <p class="sentensesText">HOT DEAL<br><span class="sentensesTextPink">FOR MEN</span></p>
            </div>
            <div class="cardSentensesTop image-3">
                <p class="sentensesText">NEW ARRIVALS<br><span class="sentensesTextPink">FOR KIDS</span></p>
            </div>
        </div>
        <div class="sentensesBottom">
            <div class="cardSentensesBottom image-4">
                <p class="sentensesText">LUXIROUS & TRENDY<br><span class="sentensesTextPink">ACCESORIES</span></p>
            </div>
        </div>
    </div>
    <div class="catalogSection container">
        <p class="catalogBlockHeader">Fetured Items</p>
        <p class="catalogBlockText">Shop for items based on what we featured in this week</p>
    </div>
    <catalogCartBoxComponent />
    <advantagesComponent />
</template>

<script>
    import advantagesComponent from "./advantagesComponent.vue";
    import catalogCartBoxComponent from "./catalogCartBoxComponent.vue";

    export default {
        name: "IndexComponent",
        components: {
            advantagesComponent,
            catalogCartBoxComponent,
        }
    }
</script>

<style scoped>
    .logo {
        margin: 0;
        background-color: #F1E4E6;
        width: 100%;
        margin-bottom: 65px;
    }
    .sentenses {
        margin-bottom: 96px;
    }
    .wrapper {
        display: grid;
        grid-template-columns: 1fr 1fr;
    }
    .indexLogo {
        float: right;
    }
    .indexBannerBold {
        font-style: normal;
        font-weight: 900;
        font-size: 48px;
        line-height: 58px;
    }
    .indexBanner {
        font-size: 30px;
        font-weight: 300;
        font-display: normal;
        flex-wrap: nowrap;
    }
    .indexBannerPink {
        color: #F16D7F;
    }
    .pinkLine {
        width: 12px;
        height: 92px;
        background-color: #F16D7F;
        border: none;
    }
    .logo-right {
        display: flex;
        gap: 16px;
        height: 100%;
        align-items: center;
    }
    .sentensesTop {
        display: flex;
        justify-content: space-between;
        margin-bottom: 30px;
    }
    .cardSentensesTop {
        width: 360px;
        height: 260px;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    .cardSentensesBottom {
        width: 1140px;
        height: 180px;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }
    .sentensesText {
        font-weight: 400;
        font-size: 16px;
        display: block;
        color: #FFF;
    }
    .sentensesTextPink {
        font-weight: 700;
        font-size: 24px;
        color: #F16D7F;
    }
    .image-1 {
        background-image: url(../img/sentensesWoman.jpg);
    }
    .image-2{
        background-image: url(../img/sentensesMan.jpg);
    }
    .image-3 {
        background-image: url(../img/sentensesKids.jpg);
    }
    .image-4 {
        background-image: url(../img/sentensesLuxirous.jpg);
    }
    .catalogBlockHeader {
        text-align: center;
        margin-bottom: 6px;
        font-weight: 400;
        font-size: 30px;
        line-height: 36px;
        color: #222222;
    }
    .catalogBlockText {
        text-align: center;
    }
    .catalogSection {
        margin-bottom: 48px;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: #9F9F9F;
    }
    @media (max-width: 768px) and (min-width: 375px) {
        .indexLogo {
            width: 386px;
            height: 368px;
        }
    }
</style>