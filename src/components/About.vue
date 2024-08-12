<template>
    <v-container class="about-section" align="center" id="about">
        <!-- About Section (My Journey) -->
        <div class="d-flex flex-wrap justify-center align-center">
            <div class=" d-flex flex-column flex-wrap justify-center align-center">
                <v-row class="d-flex align-center justify-center text-center">
                    <v-col class="d-flex align-center justify-center flex-column">
                        <div class="d-flex align-center justify-center flex-column text-start">
                            <div class="w-100">
                                <p class="text-h3">My Journey</p>
                                <p class="text-h6 font-weight-light mt-5">
                                    My interest in programming began during my first year in college, where I was
                                    captivated by the Computer Programming 1 course.
                                    It was then that I decided to focus on programming as my future career.
                                </p>
                                <p class="text-h6 font-weight-light mt-5">
                                    During my internship, I discovered the excitement of web development, especially
                                    after being introduced to various front-end development tools. The creative process
                                    of building and refining websites quickly became a passion of mine.
                                </p>

                                <p class="text-h6 font-weight-light mt-5">
                                    Today, I continue to work on projects not only to hone my skills but also because I
                                    genuinely enjoy the challenges and creativity involved in programming. Each project
                                    is an opportunity to learn and grow, fueling my enthusiasm for the ever-evolving
                                    world of technology.
                                </p>
                            </div>
                        </div>
                    </v-col>
                    <v-col class="d-flex align-center justify-center" cols="12" md="6">
                        <!-- Profile Image -->
                        <v-img src="/images/lloyd-pic.jpg" min-height="300" min-width="300" class="ranielle"></v-img>
                    </v-col>
                </v-row>
            </div>
        </div>
    </v-container>

    <!-- Adding Space Between Sections -->
    <v-container class="my-10"></v-container>

</template>
<script>
export default {
    name: "about",
    data: () => ({

    }),
    methods: {
        zoomIn(event) {
            event.currentTarget.style.transform = 'scale(1.05)';
        },

    }
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    font-family: "Poppins", sans-serif;
}

.ranielle {
    display: block;
    max-width: 70%;
    min-width: 70%;
    height: auto;
    min-height: 70%;
}

.about-section {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
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