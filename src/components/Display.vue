<script setup>
    const props = defineProps(
        { value: { type: String } }
    )
</script>

<template>
    <input type="text" readonly
    :value= "props.value"/>
</template>

<style></style>
