<template>
  <div class="myComponent">
    <!-- v-on: and @ si the same -->
    <button @click=" $event => toggleVisibility()" >AParece o desaparece</button>
    <h1 v-if="isVisible"> {{ msg }} </h1>
    <input type="text" v-model="msg">
  </div>
</template>

<script>

export default {
  name: 'myComponent',
  data(){
    return{
      msg: 'Welcome to Your Vue.js App',
      isVisible: false
    }
  },
  methods:{
    toggleVisibility(){
      this.isVisible = !this.isVisible
    }
  }
}

</script>