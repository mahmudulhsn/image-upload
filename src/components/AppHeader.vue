<template>
    <div  class="ui secondary pointing menu">
        <router-link to="/" class="active item">Image Storage</router-link>
        <div class="right menu">
            <span v-if="isLoggedIn" class="horizontal">
                <router-link to="/" href="#" class="ui item"> Gallery</router-link>
                <router-link to="/upload" href="#" class="ui item"> Upload Image</router-link>
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