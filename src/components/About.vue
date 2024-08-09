<template>
    <v-container class="d-flex align-center justify-center" align="center" id="container">
        <!-- About Section (My Journey) -->
        <div class="d-flex flex-wrap justify-center align-center">
            <div class=" d-flex flex-column flex-wrap justify-center align-center">
                <v-row>
                    <v-col>
                        <div class="d-flex align-center justify-center flex-column text-start">
                            <div class="w-100">
                                <p class="text-h5">My Journey</p>
                                <p class="mt-5">
                                    My journey in web development began when I discovered Frontend Mentor. At that time,
                                    my knowledge of
                                    HTML and CSS was limited, but this did not stop me from starting the challenge.
                                    After several hours of
                                    Googling and searching for solutions, I completed my very first project. The joy I
                                    felt when I saw it
                                    working motivated me to take on more difficult challenges.
                                </p>
                                <p class="mt-5">
                                    My journey in web development began when I discovered Frontend Mentor. At that time,
                                    my knowledge of
                                    HTML and CSS was limited, but this did not stop me from starting the challenge.
                                    After several hours of
                                    Googling and searching for solutions, I completed my very first project. The joy I
                                    felt when I saw it
                                    working motivated me to take on more difficult challenges.
                                </p>
                                <p class="mt-5">
                                    My journey in web development began when I discovered Frontend Mentor. At that time,
                                    my knowledge of
                                    HTML and CSS was limited, but this did not stop me from starting the challenge.
                                    After several hours of
                                    Googling and searching for solutions, I completed my very first project. The joy I
                                    felt when I saw it
                                    working motivated me to take on more difficult challenges.
                                </p>
                            </div>
                        </div>
                    </v-col>
                    <v-col>
                        <!-- Profile Image -->
                        <v-img src="/images/lloyd-pic.jpg" min-height="300" min-width="300"
                            class="ranielle elevation-24"></v-img>
                    </v-col>
                </v-row>
            </div>
        </div>
    </v-container>

    <!-- Adding Space Between Sections -->
    <v-container class="my-10"></v-container>

    <!-- My Skills Section -->
    <v-container>
        <div>
            <p class="text-h5 mb-5">My Skills</p>
        </div>
        <div class="d-flex align-center justify-center" align="start" id="container">
            <v-row justify="center">
                <v-col cols="12" sm="6" md="4" lg="3" class="text-center" v-for="skill in skills" :key="skill.name">
                    <v-icon large class="ma-4">{{ skill.icon }}</v-icon>
                    <p class="text-h6 mt-2">{{ skill.name }}</p>
                </v-col>
            </v-row>
        </div>
    </v-container>
</template>
<script>
export default {
    name: "Home page",
    data: () => ({
        skills: [
            { name: "Javascript", icon: "mdi-language-javascript" },
            { name: "VueJS", icon: "mdi-vuejs" },
            { name: "HTML5", icon: "mdi-language-html5" },
            { name: "CSS", icon: "mdi-language-css3" },
            { name: "Tailwind CSS", icon: "mdi-tailwind" },
            { name: "PHP", icon: "mdi-language-php" },
            { name: "Laravel", icon: "mdi-laravel" },
            { name: "Node.js", icon: "mdi-nodejs" },
        ],
    }),
    methods: {
        zoomIn(event) {
            event.currentTarget.style.transform = 'scale(1.05)';
        },

    }
}
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300..900;1,300..900&display=swap");

* {
    font-family: "Rubik", sans-serif;
}

.ranielle {
    display: block;
    max-width: 50%;
    min-width: 50%;
    height: auto;
    min-height: 50%;
}

@keyframes slideUp {
    0% {
        transform: translateY(20px);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}

#container {
    animation: slideUp 0.5s ease-out forwards;
}
</style>