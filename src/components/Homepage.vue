<template>
    <v-container class="h-100 d-flex align-center justify-center">
        <div class="d-flex flex-wrap justify-center align-center">
            <div class=" d-flex flex-column flex-wrap justify-center align-center">
                <v-row>
                    <v-col>
                        <div class="d-flex align-center justify-center flex-column">
                            <div class="w-100">
                                <p class="text-h5">Hi! I am</p>
                                <p class="text-h4">Ranielle Lloyd Cruz</p>
                                <p class="py-2 my-2">Frontend Developer</p>
                                <p>I'm a Javascript Developer that focuses on front-end frameworks such as React, Vue,
                                    NuxtJS and NextJS.
                                    I have a passion for Design Systems, Web Accessibility, Open Source Contribution,
                                    and System Integration.
                                    To grow I focus on contributing to open source projects.</p>
                                <v-btn class="mt-4">See more</v-btn>
                            </div>
                        </div>
                    </v-col>
                    <v-col>
                        <div class="d-flex flex-column rounded-5 align-center justify-center">
                            <!-- <picture>
                                <img src="/images/lloyd-pic.jpg" class="img-thumbnail rounded-circle">
                            </picture> -->
                            <v-img src="/images/lloyd-pic.jpg" min-height="300" min-width="300"
                                class="ranielle elevation-24"></v-img>
                        </div>
                    </v-col>
                </v-row>


            </div>
        </div>
    </v-container>
</template>
<script setup>
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
</style>