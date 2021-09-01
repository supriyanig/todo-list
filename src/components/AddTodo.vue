<template>
    <div class="container">
        <input class="form-control"
               :value="newTodo"
               @change="getTodoList">
        <button class="btn btn-primary" @click="addTodo">Add Todo</button>
    </div>
</template>
<script>
    export default{
        methods: {
            getTodoList(e){
                this.$store.dispatch('getTodoList', e.target.value)
            },
            addTodo(){
                this.$router.push({ name:'Dashboard'}).catch(() => {});
                this.$store.dispatch('addTodo')
                this.$store.dispatch('clearTodo')
            }
        },
        computed: {
            newTodo(){
                return this.$store.getters.newTodo
            }
        }
    }
</script>