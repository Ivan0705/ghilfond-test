<template>
    <div class="info_empty ">
        <div class="text_center">Выберите сотрудника, чтобы посмотреть</div>
    </div>
</template>

<script>
    export default {
        name: 'EmptyInfo'
    }
</script>

<style lang="scss" scoped>
   @import "../SCCS/Styles";

    .info_empty {
        background: $white;
        width: 975px;
        height: 575px;
        box-sizing: border-box;
        border-radius: 0 10px 10px 0;
        position: absolute;
    }

    .text_center {
        position: absolute;
        width: 397px;
        height: 17px;
        margin-top: 250px;
        margin-left: 284px;
        font-family: $font_family;
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: $gray;
    }
</style>
