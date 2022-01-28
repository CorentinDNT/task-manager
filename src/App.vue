<template>
    <div id="app">
        <Menu />
        <Tasks />
    </div>
</template>

<script>
import Menu from '@/components/Menu.vue';
import Tasks from '@/components/Tasks/Tasks.vue';

export default {
    name: 'App',
    components: {
        Tasks,
        Menu,
    },
};
</script>

<style lang="scss">
#app {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    color: #2c3e50;
}
</style>
