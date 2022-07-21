<template>
    <div class="forgrid">
        <div class="cartEl" v-for="cartel in getCart" :key="cartel.id">
            <h1>{{ cartel.name }}</h1>
            <br>
            <p>price: {{ cartel.price }}$</p>
            <button @click="deleteCart(cartel.index)">Удалить из корзины</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CartComponent',
        computed: {
            getCart() {
                return this.$store.getters.getCart
            }
        },
        methods: {
            deleteCart(index) {
                this.$store.dispatch("deleteElementCart", index)
            }
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
    .forgrid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        gap: 30px;
    }
</style>