<template>
    <div>
        <!-- App bar for larger screens -->
        <v-app-bar app fixed class="app-bar text-center d-flex justify-center" v-if="!smAndDown">
            <v-row align="center" justify="center" class="flex-container">
                <v-col cols="auto">
                    <router-link to="/" class="nav">
                        <v-btn class="text-white list-title text">Home</v-btn>
                    </router-link>
                </v-col>
                <v-col cols="auto">
                    <router-link class="nav">
                        <v-btn class="text-white list-title text" @click="scrollToAbout">About</v-btn>
                    </router-link>
                </v-col>
                <v-col cols="auto">
                    <router-link class="nav">
                        <v-btn class="text-white list-title text" @click="scrollToSkills">Skills</v-btn>
                    </router-link>
                </v-col>
                <v-col cols="auto">
                    <router-link class="nav">
                        <v-btn class="text-white list-title text" @click="scrollToProjects">Projects</v-btn>
                    </router-link>
                </v-col>
            </v-row>
        </v-app-bar>


        <!-- Navigation drawer for smaller screens -->
        <v-navigation-drawer app v-if="smAndDown" v-model="drawer" temporary>
            <v-list dense>
                <v-list-item class="text">
                    <router-link to="/" class="nav">
                        <v-list-item-title>Home</v-list-item-title>
                    </router-link>
                </v-list-item>
                <v-divider></v-divider>


                <v-expansion-panels flat>
                    <v-hover>
                        <template v-slot:default="{ isHovering, props }">
                            <v-expansion-panel>
                                <v-expansion-panel-title class="pl-2 ml-2">
                                    <template v-slot>
                                        <v-row no-gutters>
                                            <v-col class="d-flex justify-start text" cols="12">
                                                Our Properties
                                            </v-col>
                                        </v-row>
                                    </template>
                                </v-expansion-panel-title>

                            </v-expansion-panel>
                        </template>
                    </v-hover>


                </v-expansion-panels>
                <v-divider></v-divider>
                <v-list-item class="text">
                    <router-link to="/about" class="nav">
                        <v-list-item-title>About Ros</v-list-item-title>
                    </router-link>
                </v-list-item>
                <v-divider></v-divider>
                <v-list-item @click="scrollToFooter" class="text">
                    <v-list-item-title>Contact</v-list-item-title>
                </v-list-item>
                <v-divider></v-divider>
            </v-list>
        </v-navigation-drawer>
        <!-- Mobile app bar -->
        <v-app-bar app fixed v-if="smAndDown">
            <v-app-bar-nav-icon @click="toggleDrawer" />

        </v-app-bar>
    </div>
</template>

<script>
import { ref } from 'vue';
import { useDisplay } from 'vuetify';

export default {
    name: 'header',
    data: () => ({
    }),
    setup() {
        const { smAndDown } = useDisplay();
        const drawer = ref(false);

        const toggleDrawer = () => {
            drawer.value = !drawer.value;
        };

        return {
            smAndDown,
            drawer,
            toggleDrawer,
        };
    },
    methods: {
        scrollToAbout() {
            const footer = document.getElementById('about');
            if (footer) {
                footer.scrollIntoView({ behavior: 'smooth' });
            }
        },
        scrollToSkills() {
            const footer = document.getElementById('skills');
            if (footer) {
                footer.scrollIntoView({ behavior: 'smooth' });
            }
        },
        scrollToProjects() {
            const footer = document.getElementById('projects');
            if (footer) {
                footer.scrollIntoView({ behavior: 'smooth' });
            }
        },
        scrollToContainer() {
            const container = document.getElementById('container');
            if (container) {
                container.scrollIntoView({ behavior: 'smooth' });
            }
        },
    },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400&display=swap');

.text {
    font-family: 'Montserrat', sans-serif;
}

.app-bar {
    height: 10vh;
    padding: 0 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.toolbar-title {
    padding-left: 20px;
    font-size: 24px;
    text-transform: uppercase;
    display: flex;
    align-items: center;
}

.flex-container {
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

.nav {
    text-decoration: none;
    display: flex;
    align-items: center;
}

.list-title {
    font-size: 1rem;
    text-transform: uppercase;
}

.ho:hover {
    background-color: black;
    font-weight: bold;
}

@media (max-width: 600px) {
    .toolbar-title {
        font-size: 18px;
    }

    .list-title {
        font-size: 0.8rem;
    }
}

.nav-container {
    position: relative;
    top: 0;
    width: 100%;
}
</style>