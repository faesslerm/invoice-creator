<script setup lang="ts">
import { jsPDF } from "jspdf";
import { ref } from "vue";
import FilePreview from "../components/FilePreview.vue";

const preview = ref(null);

function createPdf(event) {
    console.log("Generating pdf...");
    // Default export is a4 paper, portrait, using millimeters for units
    const doc = new jsPDF();

    if (preview.value) {
        doc.html(preview.value.content, {
            callback: function (doc) {
                // Save the PDF
                doc.save('sample-document.pdf');
            },
            x: 15,
            y: 15,
            width: 170, //target width in the PDF document
            windowWidth: 650 //window width in CSS pixels
        });
    }
}
</script>

<template>
    <div>
        <h1>Home Page</h1>
        <p>This is a sample</p>
        <UButton @click="createPdf">Generate PDF</UButton>
        <PersonForm />

        <FilePreview ref="preview" />
    </div>
</template>