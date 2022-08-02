<template>
    <div>
        <p><strong>Componente vue {{ myNumber }}</strong> </p>
        <button @click="add">Add Version</button>
    </div>
</template>

<script>
export default {

    name: 'MyComponent2',
    data() {
        return {
            myNumber: 2,
        }
    },
    methods: {
        add() {
            this.myNumber++;
        }
    }

}
</script>

<style>
</style>