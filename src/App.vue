<template>
<h1>{{title}}</h1>
  <input class="" type="text" ref="name">
  <button class="text-lg" @click="handleClick">Click here</button>
  <p>Welcome</p>
  <div v-if="showModel">
    <second-view :header="header" :text="text"></second-view>
  </div>
<button @click="toggleModal">
  <span v-if="showModel">Hide</span>
  <span v-if="!showModel">hid</span>
</button>
</template>
<script>

import SecondView from "@/components/Second";
export default {
  name: 'App',
  components: {SecondView},
  data() {
    return{
      title:'The last Lord',
      header:'The sing and ring',
      text:'Show the lord',
      showModel: false
    }
  },
  methods: {
    toggleModal(){
      this.showModel=!this.showModel
    },
    handleClick(){
      console. log (this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()


    }

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
