# t-vue-switch

## Module Usage

```bash
npm i t-vue-switch
```

#### 

#### demo.vue

```vue
<template>
    <div id="app">
        <app-switch v-model="statuss[index]" :isRound="index"></app-switch>
    </div>
</template>

<script>
import Switch from 't-vue-switch';

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
```



## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

## Other Notes

1. [npm url](https://www.npmjs.com/package/t-vue-switch)
2. [demo](https://teana0953.github.io/t-vue-switch/)