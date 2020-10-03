<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png" />
        <app-switch v-model="isOn"></app-switch>
		<span class="margin-top"></span>
        <div class="result-text">{{ isOn }}</div>
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
	padding: 4px 6px 4px 6px
}

.margin-top {
	margin-top: 10px;
}
</style>
