<template>
    <div class="v-contact-user" @click="toContactInfo">
        <div class="user__avatar"></div>
        <div class="user__name">
            {{ contact_data.name }}
        </div>
        <div
            class="user__status"
            :class="className"
        >
        </div>
    </div>
</template>

<script>
    export default {
        name: 'v-contact-user',
        data() {
            return {}
        },
        props: {
            contact_data: {
                type: Object,
                default: () => {}
            }
        },
        computed: {
            className() {
                return {
                    'online': this.contact_data.status === 'online',
                    'offline': this.contact_data.status === 'offline'
                }
            }
        },
        methods: {
            toContactInfo() {
                this.$emit('to-contact-info')
            }
        }
    }
</script>

<style lang="scss">

</style>