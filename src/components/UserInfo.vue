<template>
    <div class="main_user_info">
        <div class="wrapper_user_info ">
            <img src=../images/profile.png alt="profile"/>
            <div>
                <div class="name_user_info">{{user.name}}</div>
                <br/>
                <div class="email_user_info">{{user.email}}</div>
                <br/>
                <div class="phone_user_info">{{user.phone}}</div>
                <div class="aboutMe_user_info">О себе</div>
                <div class="content_user_info">
                    Email:{{user.username}}
                    <br/>
                    street: {{user.address.street}}
                    <br/>
                    suite: {{user.address.suite}}
                    <br/>
                    city: {{user.address.city}}
                    <br/>
                    zipcode: {{user.address.zipcode}}
                    <br/>
                    lat: {{user.address.geo.lat }}
                    <br/>
                    lng: {{user.address.geo.lng}}
                    <br/>
                    Company name: {{user.company.name}}
                    <br/>
                    Company catchPhrase: {{user.company.catchPhrase}}
                    <br/>
                    Company bs:{{user.company.bs}}
                    <br/>
                    website:{{user.website}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'UserInfo',
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

    .main_user_info {
        width: 975px;
        height: 575px;
    }

    .wrapper_user_info {
        display: flex;
    }

    img {
        margin-top: 30px;
        margin-left: 21px;
        width: 424px;
        height: 286px;
        background: $white;
        border: 1px solid $light_gray;
    }

    .name_user_info {
        width: 233px;
        height: 19px;
        margin-top: 30px;
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 140%;
        margin-left: 61px;
        font-family: $font_family;
    }

    .email_user_info {
        width: 242px;
        height: 21px;
        margin-top: 10px;
        font-style: normal;
        font-weight: 600;
        font-size: 14px;
        line-height: 140%;
        margin-left: 61px;
        font-family: $font_family;
        color: $dark_gray;
    }

    .phone_user_info {
        width: 242px;
        height: 21px;
        margin-top: 10px;
        font-style: normal;
        font-weight: 600;
        font-size: 14px;
        line-height: 140%;
        margin-left: 61px;
        font-family: $font_family;
        color: $dark_gray;
    }

    .aboutMe_user_info {
        width: 233px;
        height: 22px;
        margin-top: 20px;
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 140%;
        margin-left: 61px;
        font-family: $font_family;
        color: $dark_gray;
    }

    .content_user_info {
        width: 439px;
        height: 136px;
        margin-top: 25px;
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 17px;
        margin-left: 61px;
        font-family: $font_family;
        color: $dark_gray;
    }
</style>
