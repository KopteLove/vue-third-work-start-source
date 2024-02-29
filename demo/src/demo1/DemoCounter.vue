<template>
    <div class="counter">
        <CounterButton @action="decrement">-</CounterButton>

        <CounterValue :value="count" />

        <CounterButton @action="increment">+</CounterButton>
    </div>
</template>

<script setup>
    import CounterButton from '@/demo1/CounterButton.vue';
    import CounterValue from '@/demo1/CounterValue.vue';
    import { ref } from 'vue';

    const count = ref(0);

    /* Метод уменьшения значения */
    const decrement = () => {
        count.value = count.value - 1;
    };

    /* Метод увеличения значения */
    const increment = () => {
        count.value = count.value + 1;
    };
</script>

<style lang="scss" scoped>
    .counter {
        display: flex;
        align-items: center;
    }
</style>
