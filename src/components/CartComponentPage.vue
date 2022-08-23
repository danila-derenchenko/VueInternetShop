<template>
    <div class="cart">
        <div class="intro">
            <div class="wrapperIntro container">
                <p class="textIntro">SHOPPING CART</p>
            </div>
        </div>
        <div class="wrapper container">
            <div class="cartBox">
                <div class="cartElement" v-for="element in this.getCart" :key="element">
                    <img v-bind:src=element.imgurl alt="" class="cartImg">
                    <div class="cartInfo">
                        <div class="headerCartElement">
                            <p class="cartInfoName">{{ element.name }}</p>
                            <img src="../img/close.svg" alt="closeButton" class="closeButton">
                        </div>
                        <div class="parametrBox">
                            <p class="cartInfoParametr">Price: <span class="cartPink">{{ element.price }}</span></p>
                            <p class="cartInfoParametr">Color: <span class="cartGray">{{ element.color }}</span></p>
                            <p class="cartInfoParametr">Size: <span class="cartGray">{{ element.size }}</span></p>
                            <p class="cartInfoParametr">Quantity:   <span class="cartGray">2</span></p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="cartForm"></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CartComponent',
        computed: {
            getCart() {
                console.log(this.$store.getters.getCart)
                return this.$store.getters.getCart
            }
        },
        methods: {
            deleteCart(index) {
                this.$store.dispatch("deleteElementCart", index)
            }
        },
        async mounted() {
            let cartElements = await fetch("https://raw.githubusercontent.com/danila-derenchenko/forApi/main/cart.json")
            let result = await cartElements.json()
            this.$store.dispatch("firstLoadingCart", result)        
        }
    }
</script>

<style>
    .cartEl {
        border: 1px solid black;
        width: 200px;
        height: 200px;
        margin: auto;
    }
    .cart {
        width: 100%;
        padding-top: 75px;
    }
    .cartImg {
        width: 262px;
        height: 306px;
    }
    .cartElement {
        width: 100%;
        height: 306px;
        box-shadow: 6px 4px 35px rgba(0, 0, 0, 0.21);
        margin-bottom: 40px;
        display: flex;
        gap: 0px;
    }
    .parametrBox {
        display: flex;
        flex-direction: column;
        gap: 6px;
    }
    .cartInfo {
        width: 390px;
        height: 306px;
        padding-top: 22px;
        padding-left: 31px;
        padding-bottom: 62px;
        padding-right: 22px;
    }
    .intro {
        width: 100%;
        height: 148px;
        background: #F8F3F4;
        margin-bottom: 96px;
    }
    .textIntro {
        font-weight: 400;
        font-size: 24px;
        line-height: 148px;
        color: #F16D7F;
    }
    .wrapper {
        display: grid;
        grid-template-columns: 1.5fr 1fr;
    }
    .cartBox {
        width: 652px;
    }
    .cartForm {
        width: 360px;
        height: 500px;
        border: 1px solid black;
    }
    .headerCartElement {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 42px;
    }
    .cartInfoName {
        font-weight: 400;
        font-size: 24px;
        line-height: 29px;
        color: #222222;
    }
    .closeButton:hover {
        cursor: pointer;
    }
    .cartInfoParametr {
        font-weight: 400;
        font-size: 22px;
        line-height: 26px;
        color: #575757;
    }
    .cartPink {
        color: #F16D7F;
    }
    .cartGray {
        color: #656565;
    }
</style>