<template>
    <div class="not_found">Ничего не найдено</div>
</template>
<script>
    export default {
        name: 'NotFound'
    }
</script>
<style lang="scss" scoped>
    @import "../SCCS/Styles";

    .not_found {
        width: 141px;
        height: 17px;
        margin-top: 15px;
        margin-left: 20px;
        font-family: $font_family;
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: $gray;
    }
</style>
