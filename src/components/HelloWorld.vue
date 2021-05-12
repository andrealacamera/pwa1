<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="spazio" :style="styleObject">
      <button @click="cambia">Premi qui</button>
      </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      styleObject: {
        backgroundColor: '#cccccc',
        border: '2px',
        height: '4em'
      }
    }
  },
  methods: {
    cambia()  {
      this.styleObject.backgroundColor = `#${Math.floor(Math.random()*16777215).toString(16)}`;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.spazio {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 50px;
}


h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
