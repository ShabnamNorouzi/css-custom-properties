<template>
    <div class="grid">
        <img src="" alt="home" />
        <img src="" alt="search" />
        <img src="" alt="gallery" />
        <img src="" alt="setting" />
        <img src="" alt="study" />
    </div>
</template>

<style scoped>
.grid {
    --columns: auto-fit;
    display: grid;
    gap: 10px;
    grid-template-columns: repeat(var(--columns), minmax(0, 1fr));
}
</style>