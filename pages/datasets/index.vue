<template>
    <a-layout class=" h-100vh">
        <a-layout-sider class="w-1xl">sider</a-layout-sider>
        <a-layout-content class="ml-6  w-3xl">
            <div class="flex flex-col">
                <div class="grid-container">
                    <div v-for="item in datasets" :key="item.datasetId" class=" py-2">
                        <DatasetListItem :dataset="item" />
                    </div>
                </div>
                <a-pagination :total="datasets.length" />
            </div>
        </a-layout-content>
    </a-layout>
</template>
  
<script lang="ts" setup>
import { ref } from 'vue';
import type { Dataset } from '~/types/types';
const datasets = ref<Dataset[]>([
    {
        date: '2023-11-01',
        datasetId: 'ds1',
        userName: 'John Doe',
        datasetName: 'Dataset 1',
        itemCount: 100,
        favoriteCount: 50,
    },
    {
        date: '2023-11-02',
        datasetId: 'ds2',
        userName: 'Jane Doe',
        datasetName: 'Dataset 2',
        itemCount: 200,
        favoriteCount: 60,
    },
    {
        date: '2023-11-03',
        datasetId: 'ds3',
        userName: 'Alice',
        datasetName: 'Dataset 3',
        itemCount: 150,
        favoriteCount: 30,
    },
    {
        date: '2023-11-04',
        datasetId: 'ds4',
        userName: 'Bob',
        datasetName: 'Dataset 4',
        itemCount: 180,
        favoriteCount: 80,
    },
    // ... more datasets
])

</script>
  
<style scoped>
.grid-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);

}
</style>