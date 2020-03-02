<template>
    <b-navbar id="chat-navbar" toggleable="md" type="dark" variant="info">
        <b-navbar-brand href="#">
            Vue Chat
        </b-navbar-brand>
        <b-navbar-nav class="ml-auto">
            <b-nav-text> {{ user.name }} | </b-nav-text>
            <b-nav-item href="#" active>Logout</b-nav-item>
        </b-navbar-nav>
    </b-navbar>
</template>

<script>
import { mapState } from 'vuex'

export default {
    name: 'message-list',
    computed: {
        ...mapState([
            'user'
        ])
    }
}
</script>

<style>

.message-list {
    margin-bottom: 15px;
    padding-right: 15px;
}

.message-group {
    height: 65vh !important;
    overflow-y: scroll;
}

.message {
    border: 1px solid lightblue;
    border-radius: 4px;
    padding: 10px;
    margin-bottom: 15px;
}

.message-title {
    font-size: 1rem;
    display: inline;
}

.message-text {
    color: gray;
    margin-bottom: 0;
}

.user-typing {
    height: 1rem;
}

</style>