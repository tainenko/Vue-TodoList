<template>
    <div id="app">
        <Todos v-bind:todos="todos" v-on:mark-todo="markCompleted"/>
    </div>
</template>

<script>
    import Todos from './components/Todos'

    export default {
        name: 'App',
        components: {
            Todos
        },
        methods: {
            markCompleted(id) {
                this.todos.forEach(item => {
                    if (item.id === id) {
                        item.completed = !item.completed
                    }
                })
            }
        },
        data() {
            return {
                todos: [
                    {
                        id: 1,
                        title: "Todo One",
                        completed: false
                    },
                    {
                        id: 2,
                        title: "Todo Two",
                        completed: false
                    },
                    {
                        id: 3,
                        title: "Todo Three",
                        completed: false
                    }
                ]
            }
        }
    }
</script>

<style>
</style>
