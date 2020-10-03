<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png" />
        <app-switch v-model="isOn"></app-switch>
    </div>
</template>

<script>
import Switch from './components';

export default {
    name: 'App',
    data: function() {
        return {
            isOn: false,
        };
    },
    components: {
        appSwitch: Switch,
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
