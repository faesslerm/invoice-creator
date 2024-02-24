<script setup lang="ts">
import { jsPDF } from "jspdf";

function createPdf(event) {
    console.log("Generating pdf...");
    // Default export is a4 paper, portrait, using millimeters for units
    const doc = new jsPDF();

    doc.text("Hello world!", 10, 10);
    doc.save("sample_a4.pdf");
}
</script>

<template>
    <div>
        <h1>Home Page</h1>
        <p>This is a sample</p>
        <UButton @click="createPdf">Generate PDF</UButton>
        <PersonForm />
    </div>
</template>