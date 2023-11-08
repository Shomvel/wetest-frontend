<template>
    <div class="cursor-pointer hover:bg-gray-100 border-solid border-gray-200 border-1 border bg-opacity-50 rounded-lg p-4 w-[300px]" @click="() => router.push({ path: '/datasets/' + dataset.datasetId })
    ">
        <div class="flex items-center">
            <Data theme="outline" size="24" fill="#333" class="mr-2" />
            <div class="text-lg">{{ dataset.userName }} / {{ dataset.datasetName }}</div>
        </div>
        <div class="text-gray-500 mt-2">
            <span>{{ formatDate(dataset.date) }}</span>
            <span class="ml-2">{{ dataset.itemCount }} 题目</span>
            <span class="ml-2">{{ dataset.favoriteCount }} 收藏</span>
        </div>
    </div>
</template>
  
<script setup lang="ts">
import type { Dataset } from '~/types/types';
import { Data } from '@icon-park/vue-next';

const router = useRouter()
// Define props
const { dataset } = defineProps<{ dataset: Dataset }>();

// Format date function
const formatDate = (date: string) => {
    const d = new Date(date);
    return d.getFullYear() + "-" + (d.getMonth() + 1).toString().padStart(2, '0') + "-" + d.getDate().toString().padStart(2, '0');
};
</script>