<template>
    <div class="v-user-chat">
        <v-message
            v-for="message in messages"
            :key="message.id"
            :message="message"
        />
        <div class="input__field">
            <input 
                type="text"
                class="v-user-chat__textfield"
                v-model="textValue"
                @keypress:enter="sendMessage"
            >
            <i class="material-icons" @click="sendMessage">send</i>
        </div>
    </div>
</template>

<script>
    import vMessage from './v-message'

    export default {
        name: 'v-user-chat',
        components: {
            vMessage
        },
        props: {
            messages: {
                type: Array,
                default: () => []
            },
            user: {
                type: Object,
                default: () => {}
            }
        },
        data() {
            return {
                textValue: ''
            }
        },
        methods: {
            sendMessage() {

            }
        }
    }
</script>

<style lang="scss" scoped>

</style>