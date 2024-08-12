<template>
    <v-container class="d-flex align-center justify-center" align="center" id="container" style="height: 100vh;">
        <div class="d-flex flex-wrap justify-center align-center">
            <div class=" d-flex flex-column flex-wrap justify-center align-center">
                <v-row class="d-flex align-center justify-center">
                    <v-col>
                        <div class="d-flex align-center justify-center flex-column text-start">
                            <div class="w-100">
                                <p class="text-h5">Hi! I am</p>
                                <p class="text-h4">Ranielle Lloyd Cruz</p>
                                <p class="py-2 my-2">Web Developer</p>
                                <p>I am a developer passionate about learning and expanding knowledge in the field of
                                    web.
                                    I am also determined to create solutions that provide excellent online experiences.
                                    Explore my portfolio to see my growing skills and dedication to quality development.
                                </p>

                                <div class="d-flex align-center justify-center ga-5">
                                    <v-btn class="mt-4" rounded="lg" size="x-large" @click="scrollToAbout">About</v-btn>
                                    <v-btn class="mt-4" rounded="lg" size="x-large" variant="outlined"
                                        href="/public/resume/Cruz-Resume.pdf" download>Resume</v-btn>
                                </div>

                            </div>
                        </div>
                    </v-col>
                    <v-col>
                        <!-- <div class="d-flex flex-column rounded-5 align-center justify-center"> -->
                        <!-- <picture>
                                <img src="/images/lloyd-pic.jpg" class="img-thumbnail rounded-circle">
                            </picture> -->
                        <!-- <v-img src="/images/webdev.png" min-height="300" min-width="300"
                                class="ranielle elevation-24"></v-img> -->
                        <!-- </div> -->
                        <v-img src="/images/webdev.png" min-height="300" min-width="300"
                            class="ranielle elevation-24"></v-img>
                    </v-col>
                </v-row>


            </div>
        </div>
    </v-container>
</template>
<script>
export default {
    name: "Homepage",
    data: () => ({

    }),
    methods: {
        zoomIn(event) {
            event.currentTarget.style.transform = 'scale(1.05)';
        },

        scrollToAbout() {
            const footer = document.getElementById('about');
            if (footer) {
                footer.scrollIntoView({ behavior: 'smooth' });
            }
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