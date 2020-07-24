<template>
    <div>
        <h1>Todos</h1>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoItem :todo="todo" v-on:mark-todo="$emit('mark-todo',todo.id)"/>
        </div>
    </div>
</template>

<script>
    import TodoItem from "./TodoItem";

    export default {
        name: "Todos",
        components: {TodoItem},
        props: ["todos"]
    }
</script>

<style scoped>

</style>