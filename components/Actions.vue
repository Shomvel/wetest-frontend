<template>
    <div class="flex justify-between items-center">
        <div class="pr-4 border-r border-gray-300">
            <div class="pb-4 font-bold">新建</div>
            <div class="flex">
                <NuxtLink to="/questions/new" class=" decoration-none">
                    <div class="mr-4 flex flex-col items-center cursor-pointer">
                        <thinking-problem theme="outline" size="36" fill="#333" />
                        <div class="font-bold mt-2">测试题</div>
                    </div>
                </NuxtLink>
                <NuxtLink to="/datasets/new" class=" decoration-none">
                    <div class="flex flex-col items-center cursor-pointer">
                        <Data theme="outline" size="36" fill="#333" />
                        <div class="font-bold mt-2">数据集</div>
                    </div>
                </NuxtLink>

            </div>
        </div>

        <div class="pl-6">
            <div class="pb-4 font-bold">测试</div>
            <div class="flex">
                <NuxtLink to="/datasets/test" class=" decoration-none">
                    <div class="mr-4 flex flex-col items-center cursor-pointer">
                        <scale-one theme="outline" size="36" fill="#333" />
                        <div class="font-bold mt-2">数据集</div>
                    </div>
                </NuxtLink>

                <NuxtLink to="/arena" class=" decoration-none">
                    <div class="flex flex-col items-center cursor-pointer">
                        <arena theme="outline" size="36" fill="#333" />
                        <div class="font-bold mt-2 decoration-none">对抗评测</div>
                    </div>

                </NuxtLink>

            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ThinkingProblem, Data, ScaleOne, Arena } from '@icon-park/vue-next';

</script>