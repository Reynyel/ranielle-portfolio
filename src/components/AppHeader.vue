<template>
    <div>
        <!-- App bar for larger screens -->
        <v-app-bar app fixed class="app-bar text-center d-flex justify-center align-center" v-if="!smAndDown">
            <v-row align="center" justify="center" class="flex-container">
                <v-col cols="auto">
                    <router-link to="/" @click="scrollToHome" class="nav">
                        <v-btn class="text-white list-title text">Home</v-btn>
                    </router-link>
                </v-col>
                <v-col cols="auto">
                    <router-link to="/" @click="scrollToAbout" class="nav">
                        <v-btn class="text-white list-title text">About</v-btn>
                    </router-link>
                </v-col>
                <v-col cols="auto">
                    <router-link to="/" @click="scrollToSkills" class="nav">
                        <v-btn class="text-white list-title text">Skills</v-btn>
                    </router-link>
                </v-col>
                <v-col cols="auto">
                    <router-link to="/" @click="scrollToProjects" class="nav">
                        <v-btn class="text-white list-title text">Projects</v-btn>
                    </router-link>
                </v-col>
            </v-row>
        </v-app-bar>


        <!-- Navigation drawer for smaller screens -->
        <v-navigation-drawer app v-if="smAndDown" v-model="drawer" temporary>
            <v-list dense>
                <v-list-item @click="scrollToHome" class="text">
                    <router-link to="/" class="nav">
                        <v-list-item-title>Home</v-list-item-title>
                    </router-link>
                </v-list-item>
                <v-divider></v-divider>
                <v-list-item @click="scrollToAbout" class="text">
                    <router-link class="nav">
                        <v-list-item-title>About</v-list-item-title>
                    </router-link>
                </v-list-item>
                <v-divider></v-divider>
                <v-list-item @click="scrollToSkills" class="text">
                    <v-list-item-title>Skills</v-list-item-title>
                </v-list-item>
                <v-divider></v-divider>
                <v-list-item @click="scrollToProjects" class="text">
                    <v-list-item-title>Projects</v-list-item-title>
                </v-list-item>
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
        scrollToHome() {
            const footer = document.getElementById('home');
            if (footer) {
                footer.scrollIntoView({ behavior: 'smooth' });
            }
        },
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
    height: 8vh;

}

.app-bar:hover{
    height: 10vh;
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