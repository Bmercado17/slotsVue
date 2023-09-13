



<template>
  <app-form>
    <template v-slot:help>
      <p>This help text</p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="email">
      <input type="text" placeholder="username">
      <input type="text" placeholder="password"> 
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
  </app-form>

  <!-- Secondform affected by slots -->
  <app-form>
    <template v-slot:help>
      <p>contact help text</p>
      <h6>{{ help }}</h6>
      <!-- v-slot and template to be able to pass it down to child component -->
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="name">
      <input type="text" placeholder="message">
    </template>      
    <template v-slot:buttons>
      <button type="submit">Submit me</button>
    </template>
    <p>dummy default slot on child comp</p>
  </app-form>
  </template>
<!-- vue logic -->

<script>
import AppForm from "./components/Form.vue"
// register the child component so it can be utilized
  export default {
    name:"App",
    components:{
      AppForm,
    },
    data(){
      return {
        help:'this can be passed with double brackets, once building the data func'
      }
    }

  }
</script> 