<script setup>

import { ref } from 'vue';

defineProps(['message','message_from_child'])
const emit = defineEmits(['update:message_from_child'])

const customMessage = 'Reply from ChildComponent';

const emitMessageEmitted = () => {
	emit('update:message_from_child', customMessage)
}

</script>


<template>
	<div class="p-4 border border-gray-300 rounded mt-8">
		<h2 class="text-lg font-semibold mb-2">Child Component</h2>
		<p class="font-semibold">Message from ParentComponent: <span class="text-green-600">{{ message }}</span></p>
		<button  @click="emitMessageEmitted()"  class="px-4 py-2 mt-2 bg-blue-500 text-white rounded">Emit Message</button>
	</div>
</template>
