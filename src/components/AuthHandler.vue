<template>
    <div>
        please wait .....
    </div>
</template>

<script>
import { mapActions } from 'vuex'
    export default {
        name: 'AuthHandler',
        methods: mapActions(['finalizeLogin']),
        created() {
            this.finalizeLogin(window.location.hash);
        },
            
    }
</script>

<style lang="scss" scoped>

</style>