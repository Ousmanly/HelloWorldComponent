<template>
<HelloWord :sub-title="subTitle" :name="user.name" :age="user.age"/>
<input type="text" v-model="subTitle"><br><br>
<input type="text" v-model="user.name"><br><br>
<input type="text" v-model="user.age">
<div
  v-if="user.age>15"
>
  Mon age
</div>
<div id="con">
  {{count}}
</div>
<button id="count" v-on:click="counter()">Compte</button>
<button id="reset" v-on:click="reset()">Recomence</button>
</template>

<script setup>
import HelloWord from './components/HelloWord.vue';
import { reactive} from 'vue';
const subTitle = reactive('Lorem, ipsum dolor sit amet consectetur adipisicing elit.');
const user = reactive({
  name :"Ousmane",
  age : 24
});
let count = 0;
function counter() {
  count +=1;
  document.getElementById('con').innerHTML=count;
  if (count >5) {
    document.getElementById('con').style.color="blue";
    document.getElementById('con').style.border="4px solid blue";
  }
}
function reset() {
  count =0;
  document.getElementById('con').innerHTML=count;
  document.getElementById('con').style.color="red";
  document.getElementById('con').style.border="4px solid red";
}
</script>



<style scoped>
  input{
   width: 400px;  
  }
  #con{
    width: 200px;
    height: 200px;
    border-radius: 50%;
    /* background-color: bisque; */
    text-align: center;
    border: 4px solid red;
    align-content: center;
    color: red;
    font-size: 60px;
    font-weight: bold;
    margin: 30px;
  }
  button{
    margin: 15px;
    height: 35px;
    width: 100px;
    background-color: red;
    font-weight: bold;
    color: bisque;
    border: none;
  }
  #count{
    background-color: green;
  }
</style>
