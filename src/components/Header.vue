<template>
    <div>
        <div class="text">Жилфонд</div>
        <div class="user">Пользователь</div>
    </div>

</template>
<script>
    export default {
        name: 'Header'
    }
</script>

<style lang="scss" scoped>
    @import "../SCCS/Styles";

    .text {
        width: 171px;
        height: 39px;
        font-style: normal;
        font-weight: 700;
        font-size: 32px;
        line-height: 39px;
        color: $red;
        margin-bottom: 30px;
        font-family: $font_family;
    }

    .user {
        position: absolute;
        width: 117px;
        height: 20px;
        left: 1199px;
        top: 30px;
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 20px;
        color: $dark_gray;
        font-family: $font_family;
    }
</style>
