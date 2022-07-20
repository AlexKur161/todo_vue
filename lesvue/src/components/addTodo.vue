<template>
    <form @submit.prevent='sub'> 
        <input placeholder="Введите заметку" class="create-task" v-model="title" type="text">
        <input class="create-task-btn" @click='sub' type="button" value="Добавить">
    </form>
</template>
<script>
export default{
    props:["todos"],
    data(){
        return {
            title:""
        }
    },
methods:{
    sub(){ 
       const newTodo = {
        id: Date.now(),
        title: this.title,
        completed: false,
        show: false
       }
       this.$emit("sub-item", newTodo)
       this.title = ""
    }
}
}
 </script>
 <style scoped>
 form{
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-bottom: 20px;
 }
 </style>