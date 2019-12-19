<template>
    <b-navbar id="chat-navbar" toggleable="md" type="dark" variant="info">
        <b-navbar-brand href="#">
            Vue Chat
        </b-navbar-brand>
        <b-navbar-nav class="ml-auto">
            <b-nav-text>{{ user.name }} | </b-nav-text>
            <b-nav-item href="#" active>Logout</b-nav-item>
        </b-navbar-nav>
    </b-navbar>
</template>

<script>
    import { mapState } from 'vuex'

    export default {
        name: 'ChatNavBar',
        computed: {
            ...mapState([
                'user',
            ])
        },
    }
</script>

<style>
    #chat-navbar {
        margin-bottom: 15px;
    }
</style>