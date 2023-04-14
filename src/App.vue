<template>
    <div class="counter">
        <p class="counter__description">The current count is...</p>
        <span class="counter__count">{{ count }}</span>
        <div class="counter__btns">
            <button class="btns__btn" @click="count++">+</button>
            <button class="btns__btn" @click="count--">-</button>
        </div>
    </div>
</template>
<script setup>
import { ref } from "vue";

const count = ref(0);
</script>

<style scoped>
.counter {
    display: grid;
    place-items: center;
    text-align: center;
}

.counter__description {
    font-size: 1.5rem;
}

.counter__count {
    font-size: 4rem;
    font-weight: bold;
}

.counter__btns {
    display: flex;
    justify-content: center;
    gap: 2rem;
}

.btns__btn {
    font-size: 1.2rem;
    font-weight: 600;
    padding: 0.5rem 1rem;
    width: 150px;
    background-color: teal;
    color: white;
    border: 0;
    border-radius: 20px;
    cursor: pointer;
}
</style>
