<template>

    <v-container class="skills-section" style="min-height: 100vh;" align="center" id="skills">
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
    name: "skills",
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
<style lang="scss">
.skills-section {
    min-height: 100vh; // Full viewport height
    display: flex;
    flex-direction: column;
    justify-content: center; // Center content vertically
    align-items: center; // Center content horizontally
    text-align: center;
}
</style>