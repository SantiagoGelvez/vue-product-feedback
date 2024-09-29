<template>
    <main class="flex flex-col gap-6">
        <section v-for="suggestion in suggestions" :key="suggestion.id"
            class="w-full px-8 py-6 bg-white rounded-xl flex gap-10">
            <div class="rounded-xl px-2 pb-2 pt-4 mb-auto bg-[#F2F4FE]">
                <div class="w-full mb-2">
                    <span>
                        <IconArrowUp />
                    </span>
                </div>

                <span class="text-[#3A4374] font-bold">{{ suggestion.upvotes }}</span>
            </div>

            <div class="w-full flex flex-col gap-1">
                <h3 class="text-[#3A4374] font-bold text-lg">{{ suggestion.title }}</h3>

                <p class="text-[#647196]">{{ suggestion.description }}</p>

                <span class="text-sm rounded-xl bg-[#F2F4FE] text-[#4661E6] font-semibold w-fit py-2 px-4">{{
                    suggestion.category }}</span>
            </div>

            <div class="my-auto flex gap-3">
                <span class="my-auto">
                    <IconComment />
                </span>

                <span class="text-[#3A4374] font-bold">{{ suggestion.comments.length }}</span>
            </div>
        </section>
    </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import IconArrowUp from '@/components/icons/IconArrowUp.vue';
import IconComment from '@/components/icons/IconComment.vue';

const suggestions = ref(
    [
        {
            "id": 1,
            "title": "Add tags for solutions",
            "category": "Enhancement",
            "upvotes": 112,
            "status": "suggestion",
            "description": "Easier to search for solutions based on a specific stack.",
            "comments": [
                {
                    "id": 1,
                    "content": "Awesome idea! Trying to find framework-specific projects within the hubs can be tedious",
                    "user": {
                        "image": "./assets/user-images/image-suzanne.jpg",
                        "name": "Suzanne Chang",
                        "username": "upbeat1811"
                    }
                },
                {
                    "id": 2,
                    "content": "Please use fun, color-coded labels to easily identify them at a glance",
                    "user": {
                        "image": "./assets/user-images/image-thomas.jpg",
                        "name": "Thomas Hood",
                        "username": "brawnybrave"
                    }
                }
            ]
        },
        {
            "id": 2,
            "title": "Add a dark theme option",
            "category": "Feature",
            "upvotes": 99,
            "status": "suggestion",
            "description": "It would help people with light sensitivities and who prefer dark mode.",
            "comments": [
                {
                    "id": 3,
                    "content": "Also, please allow styles to be applied based on system preferences. I would love to be able to browse Frontend Mentor in the evening after my device’s dark mode turns on without the bright background it currently has.",
                    "user": {
                        "image": "./assets/user-images/image-elijah.jpg",
                        "name": "Elijah Moss",
                        "username": "hexagon.bestagon"
                    }
                },
                {
                    "id": 4,
                    "content": "Second this! I do a lot of late night coding and reading. Adding a dark theme can be great for preventing eye strain and the headaches that result. It’s also quite a trend with modern apps and  apparently saves battery life.",
                    "user": {
                        "image": "./assets/user-images/image-james.jpg",
                        "name": "James Skinner",
                        "username": "hummingbird1"
                    },
                    "replies": [
                        {
                            "content": "While waiting for dark mode, there are browser extensions that will also do the job. Search for 'dark theme' followed by your browser. There might be a need to turn off the extension for sites with naturally black backgrounds though.",
                            "replyingTo": "hummingbird1",
                            "user": {
                                "image": "./assets/user-images/image-anne.jpg",
                                "name": "Anne Valentine",
                                "username": "annev1990"
                            }
                        },
                        {
                            "content": "Good point! Using any kind of style extension is great and can be highly customizable, like the ability to change contrast and brightness. I'd prefer not to use one of such extensions, however, for security and privacy reasons.",
                            "replyingTo": "annev1990",
                            "user": {
                                "image": "./assets/user-images/image-ryan.jpg",
                                "name": "Ryan Welles",
                                "username": "voyager.344"
                            }
                        }
                    ]
                }
            ]
        },
        {
            "id": 3,
            "title": "Q&A within the challenge hubs",
            "category": "Feature",
            "upvotes": 65,
            "status": "suggestion",
            "description": "Challenge-specific Q&A would make for easy reference.",
            "comments": [
                {
                    "id": 5,
                    "content": "Much easier to get answers from devs who can relate, since they've either finished the challenge themselves or are in the middle of it.",
                    "user": {
                        "image": "./assets/user-images/image-george.jpg",
                        "name": "George Partridge",
                        "username": "soccerviewer8"
                    }
                }
            ]
        },
        {
            "id": 4,
            "title": "Allow image/video upload to feedback",
            "category": "Enhancement",
            "upvotes": 51,
            "status": "suggestion",
            "description": "Images and videos can better illustrate feedback.",
            "comments": [
                {
                    "id": 6,
                    "content": "Right now, there is no ability to add images while giving feedback which isn't ideal because I have to use another app to show what I mean",
                    "user": {
                        "image": "./assets/user-images/image-javier.jpg",
                        "name": "Javier Pollard",
                        "username": "warlikeduke"
                    }
                },
                {
                    "id": 7,
                    "content": "Yes I'd like to see this as well. Sometimes I want to add a short video or gif to explain the site's behavior..",
                    "user": {
                        "image": "./assets/user-images/image-roxanne.jpg",
                        "name": "Roxanne Travis",
                        "username": "peppersprime32"
                    }
                }
            ]
        },
        {
            "id": 5,
            "title": "Ability to follow others",
            "category": "Feature",
            "upvotes": 42,
            "status": "suggestion",
            "description": "Stay updated on comments and solutions other people post.",
            "comments": [
                {
                    "id": 8,
                    "content": "I also want to be notified when devs I follow submit projects on FEM. Is in-app notification also in the pipeline?",
                    "user": {
                        "image": "./assets/user-images/image-victoria.jpg",
                        "name": "Victoria Mejia",
                        "username": "arlen_the_marlin"
                    },
                    "replies": [
                        {
                            "content": "Bumping this. It would be good to have a tab with a feed of people I follow so it's easy to see what challenges they’ve done lately. I learn a lot by reading good developers' code.",
                            "replyingTo": "arlen_the_marlin",
                            "user": {
                                "image": "./assets/user-images/image-zena.jpg",
                                "name": "Zena Kelley",
                                "username": "velvetround"
                            }
                        }
                    ]
                },
                {
                    "id": 9,
                    "content": "I've been saving the profile URLs of a few people and I check what they’ve been doing from time to time. Being able to follow them solves that",
                    "user": {
                        "image": "./assets/user-images/image-jackson.jpg",
                        "name": "Jackson Barker",
                        "username": "countryspirit"
                    }
                }
            ]
        },
        {
            "id": 6,
            "title": "Preview images not loading",
            "category": "Bug",
            "upvotes": 3,
            "status": "suggestion",
            "description": "Challenge preview images are missing when you apply a filter.",
            "comments": []
        },
    ]
)
</script>