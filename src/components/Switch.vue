<template>
    <div class="switch">
        <span class="switch__slider" :class="{ 'switch__slider--active': value }" @click="toggle(!value)"></span>
    </div>
</template>

<script>
export default {
    props: ['value', 'type'],
    methods: {
        toggle(value) {
            this.$emit('input', value);
        },
    },
};
</script>

<style scoped>
.switch {
    position: relative;
    width: 60px;
    height: 34px;
}

.switch__slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    transition: 0.4s;
}

.switch__slider::before {
    position: absolute;
    content: '';
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: #fff;
    transition: 0.4s;
}

.switch__slider--active {
    background-color: #2196f3;
}

.switch__slider--active::before {
    transform: translateX(26px);
}
</style>
