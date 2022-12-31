<template>
    <div class="hello">
        <h1>My Name Is  <a href="https://linktr.ee/adedevs"> {{firstName}} </a></h1>
        <p>And i am a student of {{school | uppercase}}</p>
        <p> {{count}} </p>
        <button @click="incrementCount">+</button>
        <button @click="decrementCount">-</button>
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
      firstName: "Adeyemi",
      school: "AltSchool",
      count: 0
    }
  },
  filters: {
    uppercase: function (value){
      if (!value) return"";
        return value.toUpperCase();
    }
  },
  methods:{
    incrementCount(){
      this.count++;
    },
    decrementCount(){
      this.count--;
    }
  },
  beforeCreate() {
    console.log('beforeCreate has been called');
  },
  created() {
    console.log('created has been called');
  },
  beforeMount() {
    console.log('beforeMount has been called')
  },
  mounted() {
    console.log('mounted has been called')
  },
  beforeUpdate() {
    console.log('beforeUpdate has been called');
  },
  updated() {
    console.log('The count is now ' + this.count)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a{
    text-decoration: none;
}
h1 {
  font-family: "Poppins";
}

p{
 text-transform: capitalize;
 font-family: 'Quicksand';
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
button {
  padding: 5px 15px;
  margin:3px;
  background-color: transparent;
  border: 2px solid red;
  border-radius: 5px;
}

button:hover {
  background-color: black;
  color: white;
  border: 2px solid red;
  transition: 200ms;
}

</style>