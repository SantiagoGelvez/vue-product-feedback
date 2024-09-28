<template>
    <nav class="w-[255px] rounded flex flex-col gap-6">
        <section class="w-full h-[137px] pt-16 pl-6 nav-section rounded-xl text-white">
            <h1 class="font-bold text-xl">Frontend Mentor</h1>
            <h2 class="font-light">Feedback Board</h2>
        </section>

        <section class="flex gap-x-2 gap-y-4 p-6 flex-wrap bg-white rounded-xl">
            <button v-for="category in categories" :key="category.name"
                class="py-1 px-4 rounded-xl bg-[#F2F4FF] text-[#4661E6] font-semibold">
                {{ category.name }}
            </button>
        </section>

        <section class="bg-white rounded-xl p-6 flex flex-col">
            <div class="flex justify-between mb-6">
                <h3 class="font-bold text-xl text-[#3A4374]">Roadmap</h3>

                <a href="#" class="font-semibold"><span class="text-sm underline">View</span></a>
            </div>

            <div v-for="status in statuses.filter(s => s.name !== 'Suggestion')" :key="status.name"
                class="flex justify-between mb-1">
                <div class="flex">
                    <p>
                        <span class="h-2 w-2 mr-4 rounded-full inline-block" :class="status.color"></span>

                        <span class="text-[#647196]">{{ status.name }}</span>
                    </p>
                </div>

                <div>
                    <span class="font-bold text-[#647196]">{{ status.count }}</span>
                </div>
            </div>
        </section>
    </nav>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const categories = ref([
    { name: 'All' },
    { name: 'UI' },
    { name: 'UX' },
    { name: 'Enhancement' },
    { name: 'Bug' },
    { name: 'Feature' },
]);

const statuses = ref([
    { name: 'Suggestion', count: 0, color: null },
    { name: 'Planned', count: 2, color: 'bg-[#F49F85]' },
    { name: 'In-Progress', count: 3, color: 'bg-[#AD1FEA]' },
    { name: 'Live', count: 1, color: 'bg-[#62BCFA]' },
]);
</script>

<style scoped>
.nav-section {
    background:
        linear-gradient(to bottom left, #e84d71ee -100px, #a337f6ee 53%, #28a8edee 100%)
}
</style>