<script setup>
// define the props this child receives from the parent
// value is the value that the Display component will show
    const props = defineProps(
        { value: { type: String } }
    )
</script>

<template>
<!-- bind the input's value to the value prop received from the parent -->
<!-- : needed for binding -->
    <input type="text" readonly
    :value= "props.value"/>
</template>

<style></style>
