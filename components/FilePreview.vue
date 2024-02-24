<script setup>
const content = ref(null);
defineExpose({ content });
</script>

<template>
    <div ref="content">
        <h1>This is a sample pdf</h1>
        <p>Hello World</p>
    </div>
</template>