<script setup>
    import { ref } from 'vue';
    const startWidth = 300;
    const startHeight = 300;
    const width = ref(300);
    const height = ref(300);

    const changeSize = () => {
        width.value = width.value * 1.2;
        height.value = height.value * 1.2;
    };

    const reset = () => {
        width.value =startWidth;
        height.value = startHeight;
    };

</script>

<template>
    <div class="viewer-container">
        <div class="button-container">
            <button @click="changeSize">Increase Size</button>
            <button @click="reset">Reset</button>
        </div>
    
        <div class="image-container">
            <img alt="Raster Example" src="../assets/girl.jpg" :width="width" :height="height" />
        </div>

        <div class="image-container">
            <img alt="Vector Example" src="../assets/house.svg" :width="width" :height="height" />
        </div>
    </div>
</template>

<style scoped>
    button {
        background-color: hsla(160, 100%, 37%, 1);
        
        cursor: pointer;
        border: none;
        color: var(--color-heading);
        padding: 10px 28px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        font-weight: 2em;
    }
    button:hover {
        background-color: hsla(160, 100%, 37%, 0.2);
    }

    h3 {
        font-size: 1.2rem;
    }

    .logo {
        margin: 0 2rem 0 0;
    }

    .viewer-container {
        margin-top: 30px;
    }

    .button-container {
        padding-bottom: 20px;
        margin-bottom: 20px;
    }

    .button-container button + button {
        margin-left: 10px;
    }

    .image-container {
        text-align: center;
        max-width: 1024px;
    }
</style>
