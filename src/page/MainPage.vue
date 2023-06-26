<template>
    <div class="app_body">
        <Header/>
        <router-view>
        </router-view>
    </div>
</template>

<script>
    import Header from "../components/Header";

    export default {
        name: 'main-page',
        components: {
            Header
        }
    }
</script>

<style lang="scss" scoped>
    $white: #FFFFFF;

    .app_body {
        width: 1266px;
        height: 748px;
        background: $white;
        margin-left: 5px;
    }
</style>
