<template>
  <div class="tasks">
    <h1>{{ msg }}</h1>

    <h3>Daily Tasks</h3>
    <div :key="task" class="task" v-for="task in tasks">
      <div class="complete" @click="task.done = !task.done">DONE</div>
      <div class="option">{{ task.value }}</div>
    </div>

    <div class="task">
      <input type="checkbox" class="checkbox" id="various-reading" />
      <label for="various-reading">15 Minutes of Various Reading</label>
    </div>
    <div class="task">
      <input type="checkbox" class="checkbox" id="budget" />
      <label for="budget">All Transactions in EveryDollar</label>
    </div>
    <h3>Weekly Tasks</h3>
    <div class="task">
      <input type="checkbox" class="checkbox" id="goetchius" />
      <label for="checkbox">1 Chapter of Goetchius</label>
    </div>
    <div class="task">
      <input type="checkbox" class="checkbox" id="convo" />
      <label for="checkbox">1 Intentional Conversation</label>
    </div>
    <div class="task">
      <div>12 Hours of Software Development</div>

      <input type="checkbox" class="checkbox" id="dev4" />
      <label for="checkbox">4</label>

      <input type="checkbox" class="checkbox" id="dev8" />
      <label for="checkbox">8</label>

      <input type="checkbox" class="checkbox" id="dev12" />
      <label for="checkbox">12</label>
    </div>
  </div>
</template>

<script>
export default {
  name: "Tasks",
  props: {
    msg: String
  },
  data() {
    return {
      tasks: [
        {
          name: "hebrew-reading",
          value: "5 Verses of Hebrew",
          done: false
        },
        {
          name: "various-reading",
          value: "15 Minutes of Various Reading",
          done: false
        }
      ],
      toDo: [],
      done: []
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 20px 0;
}
.task {
  display: block;
  margin: 1em 0;
}
input {
  margin-right: 1.25em;
  margin-left: 1.25em;
}
</style>
