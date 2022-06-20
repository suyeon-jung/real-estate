<template>
    <navigation-bar />

    <div class="black-bg" v-if="모달창">
        <div class="white-bg">
            <h4>상세페이지</h4>
            <p>상세페이지 내용</p>
            <button @click="모달창 = false">닫기</button>
        </div>
    </div>

    <div v-for="(product, idx) in products" :key="idx">
        <img :src="product.image" class="room-img">
        <h4 @click="모달창 = true">{{ product.title }}</h4>
        <p>{{ product.price }}원</p>
    </div>
</template>

<script>
import products from "./assets/data";
import NavigationBar from "./components/NavigationBar.vue";


export default {
    name: 'App',
    data() {
        return {
            모달창: false,
            products: products,
            prices: ["50만원", "60만원", "70만원"]
        }
    },
    methods: {
        increase(idx) {
            this.신고수[idx] += 1;
        }
    },
    components: {
        NavigationBar
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

.room-img {
    width: 600px;
    margin-top: 40px;
}

body {
    margin: 0
}

div {
    box-sizing: border-box;
}

.black-bg {
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    position: fixed;
    padding: 20px;
}

.white-bg {
    width: 100%;
    background: white;
    border-radius: 8px;
    padding: 20px;
}
</style>
