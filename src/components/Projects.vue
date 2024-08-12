<template>
    <v-container class="project-section" id="projects">
        <div>
            <p class="text-h5 mb-5">My Projects</p>
        </div>
        <v-carousel class="fill-height" hide-delimiters>
            <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover>
                <v-row class="fill-height d-flex flex-wrap align-bottom justify-center">
                    <div class="d-flex align-center justify-center flex-column" style="position: absolute; bottom: 0;">
                        <div class="carousel-subtitle d-flex align-center justify-center flex-column">
                            <span class="text-h6">
                                {{ item.title }}
                            </span>
                            <span>
                                {{ item.subtitle }}
                            </span>
                        </div>

                    </div>
                </v-row>
            </v-carousel-item>

        </v-carousel>
    </v-container>
</template>
<script>
export default {
    data() {
        return {
            items: [
                {
                    title: 'Ros Properties',
                    src: '/images/projects/ros-ui.png',
                    subtitle: "Developed the frontend interface for a property listings web application",
                },
                {
                    title: 'Freshcery',
                    src: '/images/projects/freshcery.png',
                    subtitle: "Developed an e-commerce web app with cart and checkout system.",
                },
                {
                    title: 'Library Management System for Santa Rosa Educational Institute',
                    src: '/images/projects/lms.png',
                    subtitle: "Created a library system in Java with MySQL for our Capstone 2 project that manages inventory of books, circulation, user data, reports, and backups.",
                },
                {
                    title: 'Bayanihan Transpo',
                    src: '/images/projects/transpo2.png',
                    subtitle: "Developed a vehicle rental web app with distance-based pricing.",
                },
            ],
        }
    },
}
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300..900;1,300..900&display=swap");

* {
    font-family: "Rubik", sans-serif;
}



.carousel-subtitle {
    background-color: rgba(0, 0, 0, 0.8);
    /* Semi-transparent grey background */
    padding: 10px;
    /* Add padding to create space between text and background */
    border-radius: 5px;
    /* Add border radius for rounded corners */
    color: #fff;
    /* Set text color to white for better visibility */
}

.carousel-subtitle:hover {
    background-color: rgba(0, 0, 0);
}

.project-section {
    min-height: 100vh;
    /* Full viewport height */
    display: flex;
    flex-direction: column;
    justify-content: center;
    /* Center content vertically */
    align-items: center;
    /* Center content horizontally */
    text-align: center;
}
</style>