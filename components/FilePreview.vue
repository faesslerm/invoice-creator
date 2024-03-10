<script setup>
const content = ref(null);
defineExpose({ content });
</script>

<template>
    <div ref="content" class="invoice border-slate-600 rounded p-4">
        <h1>This is a sample pdf</h1>
        <p>Hello World</p>
    </div>
</template>

<style scoped>
.invoice {
    width: 210mm;
    min-width: 210mm;
    height: 297mm;
    min-height: 297mm;
    background-color: rgb(241, 241, 241);
}
</style>