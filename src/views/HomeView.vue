<template>
    <div class="flex justify-center gap-8">
        <div>
            <CxNavFilters />
        </div>

        <div class="w-[825px] flex flex-col gap-6">
            <CxHeader />
            <CxSuggestionCard />
        </div>
    </div>

</template>

<script setup lang="ts">
import CxHeader from '@/components/CxHeader.vue';
import CxNavFilters from '@/components/CxNavFilters.vue';
import CxSuggestionCard from '@/components/CxSuggestionCard.vue';
</script>
