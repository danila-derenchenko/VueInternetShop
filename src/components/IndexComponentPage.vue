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
            <ul class="menu" v-show="this.menu">
                <li class="close" @click="showMenu()"><img src="../img/CloseButton.svg" alt="close" class="closeMenu"></li>
                <li class="menuIntro">MENU</li>
                <li class="menuCategory">MAN</li>
                <li class="menuElement">Accessories</li>
                <li class="menuElement">Bags</li>
                <li class="menuElement">Denim</li>
                <li class="menuElement">T-Shirts</li>
                <li class="menuCategory">WOMAN</li>
                <li class="menuElement">Accessories</li>
                <li class="menuElement">Jackets & Coats</li>
                <li class="menuElement">Polos</li>
                <li class="menuElement">T-Shirts</li>
                <li class="menuElement">Shirts</li>
                <li class="menuCategory">KIDS</li>
                <li class="menuElement">Accessories</li>
                <li class="menuElement">Jackets & Coats</li>
                <li class="menuElement">Polos</li>
                <li class="menuElement">T-Shirts</li>
                <li class="menuElement">Shirts</li>
                <li class="menuElement">Bags</li>
            </ul>
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
        },
        data: () => ({
            menu: true,
        }),
        methods: {
            showMenu() {
                if (this.menu == false) {
                    this.menu = true
                }
                else {
                    this.menu = false
                }
            }
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
        grid-template-columns: 1fr 1fr 0.5fr;
    }
    ul > li {
        list-style-type: none;
    }
    .menu {
        background-color: white;
        padding-left: 33px;
        padding-top: 16px;
        padding-right: 16px;
    }
    .menuCategory {
        color: #F16D7F;
        font-weight: 400;
        font-size: 14px;
        margin-bottom: 11px;
    }
    .menuElement {
        margin-left: 21px;
        color: #6F6E6E;
        font-size: 14px;
        margin-bottom: 11px;
    }
    .menuElement:hover {
        font-weight: 700;
    }
    .close {
        float: right;
    }
    .close:hover {
        cursor: pointer;
    }
    .menuElement:hover {
        cursor: pointer;
    }
    .menuIntro {
        color: black;
        font-size: 14px;
        font-weight: 700;
        line-height: 17px;
        margin-bottom: 24px;
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