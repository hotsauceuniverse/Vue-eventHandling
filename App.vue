<template>
  <button @click="handler('hi', $event)">
   click 1!
  </button>
  <button @click="handler('hello', $event)">
   click 2!
  </button><br>
  <a href="https://www.naver.com" target="_blank" @click.prevent="naver">Naver</a>
  
  <h2>{{ message }}</h2>
  <input type="text" :value="message" @input="message = $event.target.value">
  <h2>{{ checked }}</h2>
  <input type="checkbox" v-model="checked">

</template>

<script>
export default {
  data () {
    return {
      message: 'Hello World',
      checked: false
    }
  },

  methods: {
    handler(msg, event) {
      console.log(msg)
      console.log(event)
    },
    naver() {
      console.log('Naver')
    }
  }
}
</script>
