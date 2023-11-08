<template>
    <div class="p-4 border border-gray-500 border-opacity-50 rounded-lg mb-4">
        <NuxtLink :to="'/questions/' + questionItem.id"
            class="text-lg  text-blue-500 hover:text-blue-700 no-underline">{{ questionItem.question }}</NuxtLink>
        <p class="mt-2">{{ questionItem.answer }}</p>
    </div>
</template>
  
<script setup lang="ts">
import { defineProps } from 'vue'
import { useRouter } from 'vue-router'
import type { QuestionItem } from '~/types/types';
const { questionItem } = defineProps<{
    questionItem: QuestionItem
}>();

const router = useRouter();
</script>