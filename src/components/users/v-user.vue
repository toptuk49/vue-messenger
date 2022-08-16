<template>
    <div class="v-user" @click="toUserChat">
        <div class="v-user__avatar"></div>
        <div class="v-user__info">
            <div class="info__name">{{ user_data.name }}</div>
            <div class="info__last-message">{{ user_data.chat[user_data.chat.length - 1].text }}</div>
        </div>
        <div class="v-user__time">{{ user_data.chat[user_data.chat.length - 1].time }}</div>
    </div>
</template>

<script>
    export default {
        name: 'v-user',
        props: {
            user_data: {
                type: Object,
                default: () => {}
            }
        },
        data() {
            return {
                
            } 
        },
        methods: {
            toUserChat() {
                this.$router.push({
                    name: 'chat',
                    params: { 'messages': this.user_data.chat, 'user': this.user_data }
                })
            }
        }
    }
</script>

<style lang="scss">
    
</style>