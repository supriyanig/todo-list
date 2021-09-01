<template>
    <div id="completed-todos">
        <h3 v-if="completed.length > 0">Completed({{completed.length}})</h3>
        <ul class="list-group">
            <li v-bind:key="index" class="list-group-item" v-for="(todo,index) in completed">
                {{todo.body}}
                <button type="button" @click="remove(todo)" class="">
                <span class=""></span> Remove
                </button>
            </li>
        </ul>

    </div>
</template>

<script>
    export default{
        methods: {
            remove(todo){
                  this.$router.push('/dashboard');
                this.$store.dispatch('removeTodo', todo)
            }
        },
        computed: {
            completed(){
                return this.$store.getters.completedTodos
            }
        }
    }
</script>