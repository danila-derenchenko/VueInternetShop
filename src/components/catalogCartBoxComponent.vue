<template>
    <div class="catalog">
        <div class="wrapper container">
            <div class="card">
                <img src="../img/catalogImg-1.png" alt="cardImage" class="cartImg">
                <div class="cardText">
                    <p class="cardIntroText">ELLERY X M'O CAPSULE</p>
                    <p class="cardSmallText">Known for her sculptural takes on traditional tailoring, Australian arbiter of cool Kym Ellery teams up with Moda Operandi.</p>
                    <p class="cardPrice">$52.00</p>
                </div>
            </div>
            <div class="card">
                <img src="../img/catalogImg-2.png" alt="cardImage" class="cartImg">
                <div class="cardText">
                    <p class="cardIntroText">ELLERY X M'O CAPSULE</p>
                    <p class="cardSmallText">Known for her sculptural takes on traditional tailoring, Australian arbiter of cool Kym Ellery teams up with Moda Operandi.</p>
                    <p class="cardPrice">$52.00</p>
                </div>
            </div>
            <div class="card">
                <img src="../img/catalogImg-3.png" alt="cardImage" class="cartImg">
                <div class="cardText">
                    <p class="cardIntroText">ELLERY X M'O CAPSULE</p>
                    <p class="cardSmallText">Known for her sculptural takes on traditional tailoring, Australian arbiter of cool Kym Ellery teams up with Moda Operandi.</p>
                    <p class="cardPrice">$52.00</p>
                </div>
            </div>
            <div class="card">
                <img src="../img/catalogImg-4.png" alt="cardImage" class="cartImg">
                <div class="cardText">
                    <p class="cardIntroText">ELLERY X M'O CAPSULE</p>
                    <p class="cardSmallText">Known for her sculptural takes on traditional tailoring, Australian arbiter of cool Kym Ellery teams up with Moda Operandi.</p>
                    <p class="cardPrice">$52.00</p>
                </div>
            </div>
            <div class="card">
                <img src="../img/catalogImg-5.png" alt="cardImage" class="cartImg">
                <div class="cardText">
                    <p class="cardIntroText">ELLERY X M'O CAPSULE</p>
                    <p class="cardSmallText">Known for her sculptural takes on traditional tailoring, Australian arbiter of cool Kym Ellery teams up with Moda Operandi.</p>
                    <p class="cardPrice">$52.00</p>
                </div>
            </div>
            <div class="card">
                <img src="../img/catalogImg-6.png" alt="cardImage" class="cartImg">
                <div class="cardText">
                    <p class="cardIntroText">ELLERY X M'O CAPSULE</p>
                    <p class="cardSmallText">Known for her sculptural takes on traditional tailoring, Australian arbiter of cool Kym Ellery teams up with Moda Operandi.</p>
                    <p class="cardPrice">$52.00</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {

    }
</script>

<style scoped>
    .catalog {
        width: 100%;
        margin-bottom: 48px;
    }
    .wrapper {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 30px;
    }
    .card {
        width: 360px;
        height: 581px;
        background: #F8F8F8;
    }
    .cartImg {
        width: 360px;
        height: 420px;
        margin-bottom: 25px;
    }
    .cardText {
        width: 100%;
        padding-left: 8px;
        padding-right: 8px;
    }
    .cardIntroText {
        font-weight: 400;
        font-size: 13px;
        line-height: 16px;
        color: #000000;
        margin-bottom: 12px;
    }
    .cardSmallText {
        font-weight: 300;
        font-size: 14px;
        line-height: 17px;
        color: #5D5D5D;
        margin-bottom: 18px;
    }
    .cardPrice {
        font-weight: 400;
        font-size: 16px;
        line-height: 19px;
        color: #F16D7F;
    }
</style>