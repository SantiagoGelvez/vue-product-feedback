<template>
    <main class="flex flex-col gap-6">
        <section v-for="suggestion in suggestions" :key="suggestion.id" class="w-full px-8 py-6 bg-white rounded-xl">
            {{ suggestion }}
        </section>
    </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const suggestions = ref(
    [
        {
            "id": 1,
            "title": "Add tags for solutions",
            "category": "enhancement",
            "upvotes": 112,
            "status": "suggestion",
            "description": "Easier to search for solutions based on a specific stack.",
        },
        {
            "id": 2,
            "title": "Add a dark theme option",
            "category": "feature",
            "upvotes": 99,
            "status": "suggestion",
            "description": "It would help people with light sensitivities and who prefer dark mode.",
        },
        {
            "id": 3,
            "title": "Q&A within the challenge hubs",
            "category": "feature",
            "upvotes": 65,
            "status": "suggestion",
            "description": "Challenge-specific Q&A would make for easy reference.",
        },
        {
            "id": 4,
            "title": "Allow image/video upload to feedback",
            "category": "enhancement",
            "upvotes": 51,
            "status": "suggestion",
            "description": "Images and videos can better illustrate feedback.",
        },
        {
            "id": 5,
            "title": "Ability to follow others",
            "category": "feature",
            "upvotes": 42,
            "status": "suggestion",
            "description": "Stay updated on comments and solutions other people post.",
        },
        {
            "id": 6,
            "title": "Preview images not loading",
            "category": "bug",
            "upvotes": 3,
            "status": "suggestion",
            "description": "Challenge preview images are missing when you apply a filter.",
        },
    ]
)
</script>