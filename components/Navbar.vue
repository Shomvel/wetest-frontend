<template>
    <div class="flex justify-between items-center px-8 py-4 border-b-blue border-b-1px mb-6">
        <div class="flex items-center">
            <div class="text-2xl font-bold mr-4 ">Wetest</div>
            <input type="text" class="form-input" placeholder="Search" />
        </div>
        <div class="flex items-center space-x-6 no-underline ">
            <NuxtLink to="/" class="decoration-none">测试题</NuxtLink>
            <NuxtLink to="/datasets" class="decoration-none">数据集</NuxtLink>
            <NuxtLink to="/leaderboard/datasets" class="decoration-none">能力排行榜</NuxtLink>
            <NuxtLink to="/leaderboard/arena" class="decoration-none">擂台排行榜</NuxtLink>
            <NuxtLink to="/users/name" class="decoration-none">用户头像</NuxtLink>
        </div>
    </div>
</template>
  
<script setup lang="ts">
// Your Vue 3 Composition API code here
</script>