<template>
    <div>
        <div class="text font_family">Жилфонд</div>
        <div class="user font_family">Пользователь</div>
    </div>

</template>
<script>
    export default {
        name: 'Header'
    }
</script>

<style lang="scss" scoped>
    @import "../SCCS/Styles";

    .font_family {
        font-family: $font_family;
    }

    .text {
        width: 171px;
        height: 39px;
        font-style: normal;
        font-weight: 700;
        font-size: 32px;
        line-height: 39px;
        color: $red;
        margin-bottom: 30px;
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
    }
</style>
