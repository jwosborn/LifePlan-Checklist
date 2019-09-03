<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <h3>Daily Tasks</h3>
    <ul>
      <li>
        <input type="checkbox" class="checkbox" id="hebrew-reading" v-model="toDo" />
        <label for="checkbox">5 Verses of Hebrew</label>
      </li>
      <li>
        <input type="checkbox" class="checkbox" id="various-reading" v-model="toDo" />
        <label for="checkbox">15 Minutes of Various Reading</label>
      </li>
    </ul>
    <h3>Weekly Tasks</h3>
    <ul>
      <li>
        <div>1 Chapter of Goetchius</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: {
    toDo: []
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
