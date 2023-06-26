<template>
    <div class="user_profile">
        <div>
            <div class="user_profile_photo"><img src=../images/profile.png alt="profile"/></div>
            <div class="user_profile_name font_user_item">{{user.name}}</div>
            <br/>
            <div class="user_profile_email font_user_item">{{user.email}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'user-item',
        props: {
            user: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "../SCCS/Styles";

    .user_profile {
        width: 240px;
        height: 70px;
        margin-left: 20px;
        margin-top: 18px;
        background: $white;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        border-radius: 10px;
    }

    .user_profile_photo {
        box-sizing: border-box;
        width: 70px;
        height: 70px;
        border-right: 1px solid $light_gray;

    }

    .font_user_item {
        font-family: $font_family;
        font-style: normal;
        margin-left: 75px;
    }

    .user_profile_name {
        width: 115px;
        height: 15px;
        margin-top: -60px;
        font-weight: 600;
        font-size: 14px;
        line-height: 17px;
        color: $dark_gray;
    }

    .user_profile_email {
        width: 121px;
        height: 17px;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        color: $gray;
    }

    img {
        width: 40px;
        margin-left: 15px;
        margin-top: 15px;
    }
</style>
