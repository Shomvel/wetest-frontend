<template>index
<DatasetListItem :dataset="datasetItem"/>
</template>

<script setup lang="ts">
import type { Dataset } from '~/types/types';

const datasetItem: Dataset = {
    "datasetId": '1',
    "datasetName": "test",
    "userName": "test",
    "date": "2021-08-01T00:00:00.000Z",
    "itemCount": 1,
    "favoriteCount": 1
  }
</script>