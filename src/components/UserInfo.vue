<template>
    <div class="user-info">
        <div class="container">
            <img class="user-info__image" src=../images/profile.png alt="profile"/>
            <div>
                <div class="user-info__name">{{user.name}}</div>
                <br/>
                <div class="user-info__email">{{user.email}}</div>
                <br/>
                <div class="user-info__phone">{{user.phone}}</div>
                <div class="user-info__about-me">О себе</div>
                <div class="user-info__content">
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
    @import "../SCCS/Colors";
    @import "../SCCS/Fonts";

    .user-info {
        width: 975px;
        height: 575px;
        color: $dark_gray;
        line-height: 140%;
        font-family: $font-montserrat;

        &__image {
            margin-top: 30px;
            margin-left: -40px;
            width: 424px;
            height: 286px;
            background: $white;
            border: 1px solid $light_gray;
            margin-right: 61px;
        }

        &__name {
            width: 233px;
            height: 19px;
            margin-top: 30px;
            font-weight: 600;
            font-size: 16px;
        }

        &__email {
            width: 242px;
            height: 21px;
            margin-top: 10px;
            font-weight: 600;
        }

        &__phone {
            width: 242px;
            height: 21px;
            margin-top: 10px;
            font-weight: 600;
        }

        &__about-me {
            width: 233px;
            height: 22px;
            margin-top: 20px;
            font-style: normal;
            font-weight: 600;
            font-size: 16px;
        }

        &__content {
            width: 439px;
            height: 136px;
            margin-top: 25px;
            font-style: normal;
            font-weight: 400;
            line-height: 17px;
        }
    }

    .container {
        display: flex;
        margin-left: 61px;
        font-size: 14px;
        font-style: normal;
    }
</style>
