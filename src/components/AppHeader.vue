<template>
    <div  class="ui secondary pointing menu">
        <a href="/" class="active item">Image Storage</a>
        <div class="right menu">
            <span v-if="isLoggedIn" class="horizontal">
                <a href="#" class="ui item"> Gallery</a>
                <a href="#" class="ui item"> Upload Image</a>
                <a class="ui item" @click="logout"> Logout</a>
            </span>
            <a v-else href="#" class="ui item" @click="login">Login</a>
        </div>
    </div>
</template>

<script>
import {mapActions, mapGetters} from 'vuex';
    export default {
        name: 'AppHeader',
        computed: mapGetters(['isLoggedIn']),
        methods: mapActions(['login', 'logout']),
    }
</script>

<style scoped>
    .horizontal {
        display: flex;
        flex-direction: row;
    }
</style>