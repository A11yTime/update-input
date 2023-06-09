<template>
<section>
    <form @submit.prevent="submitData">
    <label for="name">Name </label>
    <input type="text" id="name" v-model="enteredName">
    <label for="age">Age </label>
    <input type="text" id="age" v-model="enteredAge">
    <button>Set User Data</button>
</form>
</section>
<div>
    
</div>
</template>

<script>
export default{
    emits: ['set-data'],
 data(){
    return{
        enteredName: '',
        enteredAge: ''
    }
 },
 methods: {
    submitData(){
        this.$emit('set-data', this.enteredName, this.enteredAge)
    }
 }
}
</script>