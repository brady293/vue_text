<template>
  <div class="test">
    <!-- <button @click="addnum">ADD</button> -->
    <input type="text" v-model="text" @keyup.enter="addtext" />

    <button @click="addtext">Submit</button>

    <!-- <p>{{ text }}</p> -->
    <p v-for="(task, index) in todo_list" :key="task">{{ index }}{{ task }}</p>
  </div>
</template>

<script>
export default {
  name: "Test-one",

  data() {
    return {
      todo_list: [],
      text: "",
    };
  },

  mounted() {},

  methods: {
    // addnum() {
    //   this.text += 1;
    // },
    addtext() {
      this.todo_list.push(this.text);
      this.text = "";
    },
  },
};
</script>

<style lang="scss" scoped></style>
