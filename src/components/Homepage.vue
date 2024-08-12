<template>
    <v-container class="homepage" id="home">
        <v-row class="d-flex align-center justify-center text-center">
            <v-col class="d-flex align-center justify-center flex-column">
                <div>
                    <p class="text-h4 text-start">Hi! I am</p>
                    <p class="text-h3 text-start">Ranielle Lloyd Cruz</p>
                    <p class="py-2 my-2 text-start text-h5">A Junior Web Developer</p>
                    <p class="text-start text-h6 font-weight-light">I am a developer passionate about learning and expanding knowledge in
                        the field of
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
            </v-col>
            <v-col class="d-flex align-center justify-center" cols="12" md="6">
                <v-img src="/images/webdev.png" min-height="300" min-width="300" class="ranielle"></v-img>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: "Homepage",
    data: () => ({}),
    methods: {
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
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    font-family: "Poppins", sans-serif;
}

.homepage {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
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

#home {
    animation: slideUp 0.5s ease-out forwards;
}
</style>
