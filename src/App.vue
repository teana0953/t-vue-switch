<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png" />

        <span class="margin-top"></span>

        <div class="app__demo" v-for="(n, index) in statuss" :key="index">
            <app-switch v-model="statuss[index]" :isRound="index"></app-switch>

            <span class="margin-top"></span>

            <div class="result-text">{{ statuss[index] }}</div>

            <span class="margin-top"></span>
        </div>
    </div>
</template>

<script>
import Switch from './components';

export default {
    name: 'App',
    data: function() {
        return {
            statuss: [false, false],
        };
    },
    components: {
        appSwitch: Switch,
    },
};
</script>

<style>
#app {
    display: flex;
    flex-direction: column;
    justify-content: center;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

.app__demo {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

img {
    align-self: center;
    width: 200px;
    height: 200px;
}

.switch {
    align-self: center;
}

.result-text {
    align-self: center;
    padding: 4px 6px 4px 6px;
}

.margin-top {
    margin-top: 10px;
}
</style>
