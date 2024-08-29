<template>
    <v-container class="skills-section" style="min-height: 100vh;" align="center" id="skills">
        <div>
            <p class="text-h3 mb-5">My Skills</p>
        </div>
        <div class="d-flex align-center justify-center" align="start" id="container">
            <v-row justify="center">
                <v-col cols="12" sm="6" md="4" lg="3" class="text-center" v-for="skill in skills" :key="skill.name">
                    <v-icon large class="ma-4" size="70">{{ skill.icon }}</v-icon>
                    <p class="text-h6 mt-2">{{ skill.name }}</p>
                    <v-progress-linear :model-value="skill.value" color="blue-grey" height="25"></v-progress-linear>
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
            { name: "Javascript", icon: "mdi-language-javascript", value: 65 },
            { name: "Vue.js", icon: "mdi-vuejs", value: 65 },
            { name: "React", icon: "mdi-react", value: 45 },
            { name: "HTML5", icon: "mdi-language-html5", value: 75 },
            { name: "CSS", icon: "mdi-language-css3", value: 60 },
            { name: "Bootstrap", icon: "mdi-bootstrap", value: 70 },
            { name: "Tailwind CSS", icon: "mdi-tailwind", value: 65 },
            { name: "PHP", icon: "mdi-language-php", value: 58 },
            { name: "Laravel", icon: "mdi-laravel", value: 50 },
            { name: "Node.js", icon: "mdi-nodejs", value: 40 },
            { name: "Java", icon: "mdi-language-java", value: 80 },
            { name: "C#", icon: "mdi-language-csharp", value: 60 },
            { name: "Python", icon: "mdi-language-python", value: 75 },
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
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    font-family: "Poppins", sans-serif;
}

.skills-section {
    min-height: 100vh; // Full viewport height
    display: flex;
    flex-direction: column;
    justify-content: center; // Center content vertically
    align-items: center; // Center content horizontally
    text-align: center;
}
</style>
