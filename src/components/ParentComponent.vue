<script setup>

import {ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

const message = ref('Hello from ParentComponent');
const messageFromChild = ref('');

</script>

<template>
    <div class="p-4">
        <h1 class="text-2xl font-semibold mb-2">Parent Component</h1>
        <p class="font-semibold">Message from ChildComponent: <span class="text-green-600">{{ messageFromChild }}</span></p>
        <ChildComponent v-model:message="message" v-model:message_from_child="messageFromChild"/>
    </div>
</template>
