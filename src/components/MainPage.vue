<template>
    <div class="wrapper_user_info"><label>
    </label>
        <div>
            <div class="search margin_left font_family">Поиск сотрудников</div>
            <textarea v-model='searchQuery' type="text" class="input margin_left" placeholder="Введите id или имя"
                      @update:model-value="setSearchQuery"></textarea>
            <div class="results margin_left font_family">Результаты</div>
            <div>
                <div v-if="!isLoading">
                    <div>
                        <div v-if="!error">
                            <UserItem v-for="user in filteredList" :key="user.id" :user="user"
                                      @click="getId(user.id)"/>

                        </div>
                        <div v-else="error">
                            <NotFound/>
                        </div>
                        <div v-if="searchQuery && !filteredList.length">
                            <NotFound/>
                        </div>
                    </div>
                </div>
                <div v-else>
                    <Preloader/>
                </div>
            </div>
        </div>
        <div class="info">
            <div v-if="id>0">
                <div v-if="!isLoadingInfo">
                    <UserInfo :user="users[this.id-1]"/>
                </div>
                <div v-else>
                    <Preloader/>
                </div>
            </div>
            <div v-else>
                <EmptyInfo/>
            </div>
        </div>
    </div>

</template>
<script>
    import UserItem from "./UserItem";
    import {mapActions, mapGetters, mapMutations, mapState} from "vuex";
    import NotFound from "./NotFound";
    import UserInfo from "./UserInfo";
    import EmptyInfo from "./EmptyInfo";
    import Preloader from "./Preloader";

    export default {
        name: 'main-page',
        components: {Preloader, EmptyInfo, UserInfo, NotFound, UserItem},
        data() {
            return {
                id: 0,
                isLoadingInfo: false
            }
        },
        methods: {
            ...mapMutations({
                setUsers: 'user/setUsers',
                setError: 'user/setError',
                setSearchQuery: 'user/setSearchQuery',
            }),
            ...mapActions({
                fetchUsers: 'user/fetchUsers'
            }),
            getId(id) {
                this.isLoadingInfo = true;
                setTimeout(() => {
                    this.id = id;
                    this.isLoadingInfo = false;
                }, 300);
                console.log('Id:', id)
            }
        },
        mounted() {
            this.fetchUsers();
        },
        computed: {
            ...mapState({
                users: state => state.user.users,
                isLoading: state => state.user.isLoading,
                searchQuery: state => state.user.searchQuery,
                error: state => state.user.error
            }),
            ...mapGetters({
                filteredList: 'user/filteredList'
            }),
        }
    }

</script>
<style lang="scss" scoped>
    @import "../SCCS/Styles";

    .margin_left {
        margin-left: 20px;
    }

    .font_family {
        font-family: $font_family;
    }

    .wrapper_user_info {
        display: flex;
        width: 1266px;
        height: 575px;
        background: $white2;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        border-radius: 10px;
    }

    .input {
        box-sizing: border-box;
        display: flex;
        flex-direction: row;
        align-items: center;
        padding: 16px;
        gap: 16px;
        width: 240px;
        height: 46px;
        background: $white;
        border: 1.5px solid $light_gray;
        border-radius: 8px;
        outline: none;
        overflow: hidden
    }

    .info {
        position: absolute;
        width: 975px;
        height: 575px;
        margin-left: 290px;
        background: $white2;
        border-left: 1px solid $light_gray;
        border-radius: 0 10px 10px 0;
    }

    textarea {
        height: 24px;
        width: 108px;
    }

    .results {
        margin-top: 15px;
        width: 233px;
        height: 22px;
        left: 70px;
        top: 254px;
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 140%;
        color: $dark_gray;
    }

    .search {
        width: 261px;
        height: 22px;
        margin-top: 27px;
        margin-bottom: 22px;
        top: 142px;
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 140%;
        color: $dark_gray;
    }
</style>
