<template>
    <div>
        <p><strong> Componente vue {{ myNumber }}</strong></p>
        <button @click="add">Add Version</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
let myNumber = ref(3);
function add() {
    myNumber.value++;
}
</script>

