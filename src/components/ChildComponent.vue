<script setup>
import { defineProps, defineEmits } from 'vue'

defineProps({
    message: String,
    emittedMessage: String,
})

const emit = defineEmits(['update:emittedMessage'])

const emitMessage = () => {
    emit('update:emittedMessage', 'Custom message from ChildComponent')
}

</script>
<template>
    <div class="bg-gray-300 p-4">
        <h3 class="text-lg mb-2">Child Component</h3>
        <p>{{ message }}</p>
        
        <button @click="emitMessage" class="mt-2 bg-blue-500 text-white px-4 py-2 rounded">
            Emit Message
        </button>
    </div>
</template>