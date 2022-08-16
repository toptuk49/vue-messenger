<template>
    <div class="v-users-list">
        <v-user 
            v-for="chat in chats"
            :key="chat.id"
            :user_data="chat"
        />
    </div>
</template>

<script>
    import {mapActions, mapState} from 'vuex'
    import vUser from './v-user'

    export default {
        name: 'v-users-list',
        components: {
            vUser
        },
        data() {
            return {
                
            } 
        },
        computed: {
            ...mapState([
                'chats'
            ])
        },
        methods: {
            ...mapActions([
                'FETCH_CHATS',
                'SET_USER_TO_HEADER'
            ])
        },
        mounted() {
            this.FETCH_CHATS()
            this.SET_USER_TO_HEADER()
        }
    }
</script>

<style lang="scss">
    
</style>