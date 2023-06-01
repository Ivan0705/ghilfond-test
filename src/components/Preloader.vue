<template>
    <img src=../images/preloader.gif alt="preloading"/>
    <div class="preloader">
        Идет загрузка...
    </div>
</template>
<script>
    export default {
        name: 'Preloader'
    }
</script>
<style lang="scss">
    @import "../SCCS/Styles";

    .preloader {
        margin-left: 20px;
        margin-top: 10px;
        font-family: $font_family;
    }

    img {
        width: 90px;
    }
</style>
