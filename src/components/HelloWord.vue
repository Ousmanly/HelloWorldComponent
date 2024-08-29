<template>
    <h1>{{ msg }}</h1>
    <p>{{ props.subTitle }}</p>
    <p>{{ props.name }} {{ props.age }}</p>
    
</template>
<script setup>
    const msg = 'HelloWorld'
    const props = defineProps(["subTitle", "name", "age"])
</script>
<style>

</style>