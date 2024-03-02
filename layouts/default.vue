<template>
    <div>
        <div class="header shadow-sm mb-6">
            <p>Invoice Creator</p>
        </div>
        <slot />
    </div>
</template>

<style scoped>
.header {
    padding: 1rem 2rem;
}

.header p {
    font-size: 1.5rem;
    font-weight: 800;
}
</style>