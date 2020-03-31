<template>
  <div :class="change()">
    <p> i am a boy</p>
      <button type="button" class="btn btn-primary btn-lg" v-on:click="toggle=!toggle">Large button</button>
  </div>
</template>

<script>
import  './assets/main.css';


export default {
  data(){
    return{
      toggle:false,
    }
  },
   methods:{
     change(){
       document.body.className = this.toggle;
       if (this.toggle === true){
         document.body.style.backgroundColor = 'black'
       } else {
         document.body.style.removeProperty("background-color")
       }
      //  return {
      //    toggle: this.toggle
      //  }
     }
   }
  
}
</script>

<style>
</style>
