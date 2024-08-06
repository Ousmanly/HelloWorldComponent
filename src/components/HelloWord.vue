<template>
    <h1>Hello {{ nom }}</h1>
    <p>{{ props.subTitle }}</p>
    <p>{{ props.name }} {{ props.age }}</p>
    
</template>
<script setup>
    const nom = "Ousmane";
    const props = defineProps(["subTitle", "name", "age"])
</script>
<style>
</style>