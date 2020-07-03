<template>

  <div id="app">
    <ul>
      <div v-for="fruit in fruits" :key="fruit">
        <p>{{fruit}}</p>
        <input type="text">
      </div>
    </ul>
    <button @click="remove">先頭を削除</button>
  </div>  


</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },

  data: function() {
    return {
     fruits: ['りんご','バナナ','ぶどう']
    }
  },
  methods: {
      remove: function() {
        this.fruits.shift()
      }
    }

};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
