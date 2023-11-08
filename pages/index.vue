<template>index

<DatasetListItem :dataset="datasetItem"/>
<QuestionListItem :question-item="question"/>
</template>

<script setup lang="ts">
import type { Dataset, QuestionItem } from '~/types/types';

const datasetItem: Dataset = {
    "datasetId": '1',
    "datasetName": "test",
    "userName": "test",
    "date": "2021-08-01T00:00:00.000Z",
    "itemCount": 1,
    "favoriteCount": 1
  }

  const question: QuestionItem = {
    "id": '1',
    "question": "test test test test",
    "answer": "test",
  }
</script>