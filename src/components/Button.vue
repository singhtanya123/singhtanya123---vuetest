<template>
  <button @click="createUser()" :style="{background: color}">{{text}}</button>
</template>

<script>
export default {
    name:"Button",
    props: {
    text: String,
    color: String,
  },
    methods : {
    createUser(){
        this.$emit('show-user-form');
    }
  }
}
</script>

<style>
    button{
        padding: 1%;
        float: right;
        margin: 2%;
    }
</style>