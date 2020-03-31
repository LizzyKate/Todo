<template>
  <div :class="currentClass" class="screenbody">
    <p>i am a boy</p>
    <button type="button" class="btn btn-primary btn-lg" v-on:click="change()">Large button</button>
  </div>
</template>

<script>
import "./assets/main.css";

export default {
  data() {
    return {
      currentClass: "white"
    };
  },
  methods: {
    change() {
      if (this.currentClass === "white") {
        this.currentClass = "black";
      } else {
        this.currentClass = "white";
      }
      //  document.body.className = this.toggle;
      //  if (this.toggle === true){
      //    document.body.style.backgroundColor = 'black'
      //  } else {
      //    document.body.style.removeProperty("background-color")
      //  }
    }
  }
};
</script>

<style>
.black {
  background: black;
}
.white {
  background: white;
}

.black p {
  color:blue;
}
.white p{
  color: yellow;
}
.screenbody{
  min-height:100vh ;
}
</style>
