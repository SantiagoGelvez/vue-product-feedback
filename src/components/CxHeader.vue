<script setup lang="ts">
import IconSuggestion from './icons/IconSuggestion.vue';
</script>

<template>
    <header class="bg-[#373F68] rounded-xl flex justify-between p-4 text-white">
        <div class="ml-4 my-auto gap-4 flex">
            <span class="my-auto">
                <IconSuggestion />
            </span>

            <h3 class="text-lg font-bold">6 Suggestions</h3>

            <span class="ml-4 my-auto">Sort by: Most Upvotes</span>
        </div>

        <div>
            <button class="px-6 py-3 bg-[#AD1FEA] rounded-xl">
                <span class="font-semibold">+ Add Feedback</span>
            </button>
        </div>
    </header>
</template>