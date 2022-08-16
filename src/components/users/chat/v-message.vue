<template>
    <div class="v-message">
        <div class="v-message__content">
            <p>{{ message.text }}</p>
            <p class="content__time">{{ message.time }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'v-message',
        props: {
            message: {
                type: Object,
                default: () => {}
            }
        }
    }
</script>

<style lang="scss">

</style>