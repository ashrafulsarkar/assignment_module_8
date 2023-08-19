<script setup>
import { ref } from 'vue'
import ChildComponent from './ChildComponent.vue'

const message = ref('Hello from Parent!')
const emittedMessage = ref('')
</script>
<template>
    <div class="bg-gray-200 p-8">
        <h2 class="text-xl mb-4">Parent Component</h2>

        <ChildComponent :message="message" v-model:emittedMessage="emittedMessage" />
        
        <div v-if="emittedMessage">
            <p class="text-green-600 mt-4">Emitted Message: {{ emittedMessage }}</p>
        </div>
    </div>
</template>