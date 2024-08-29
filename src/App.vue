<template>
  <div class="container text-center">
    <HelloWord :sub-title="subTitle" :name="user.name" :age="user.age" />
    <input type="text" v-model="subTitle" /><br /><br />
    <input type="text" v-model="user.name" /><br /><br />
    <input type="text" v-model="user.age" />
    <div v-if="user.age > 15">Mon age</div>
  </div>
</template>

<script setup>
import HelloWord from "./components/HelloWord.vue";
import { reactive } from "vue";
const subTitle = reactive(
  "Lorem, ipsum dolor sit amet consectetur adipisicing elit."
);
const user = reactive({
  name: "Ousmane",
  age: 24,
});
</script>



<style scoped>
.container {
  background-color: rgb(214, 203, 185);
}
input {
  width: 400px;
  padding: 10px;
  border: 1px solid black;
  border-radius: 10px;
}

</style>
