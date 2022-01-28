<template>
    <div class="tasks-conainer">
        <h1>liste des tâches</h1>
        <TaskCard />
    </div>
</template>

<script>
import TaskCard from './TaskCard.vue';
export default {
    components: { TaskCard },
    name: 'tasks',
};
</script>

<style lang="scss" scoped>
.tasks-conainer {
    width: 100%;
    height: 100%;
    border: 1px solid red;
    margin: 10px;
}
</style>
