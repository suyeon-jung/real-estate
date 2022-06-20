<template>
    <div class="menu">
        <a v-for="(menu, idx) in menus" :key="idx">{{ menu }}</a>
    </div>
</template>

<script>
export default {
    name: "navigation-bar",
    data() {
        return {
            menus: ["Home", "Shop", "About"],
        }
    },
    methods: {

    }
}

</script>

<style>
.menu {
    background: darkslateblue;
    padding: 15px;
    border-radius: 5px;
}

.menu a {
    color: white;
    padding: 10px;
}
</style>