<template>
    <v-container fluid>
        <v-row justify="center">
            <v-col cols="12" class="text-center">
                <h2 class="font-weight-bold display-1">Technical Skills</h2>
                <div class="orange-underline mx-auto my-2 mb-10"></div>
                <p class="subtitle-1">Technologies and tools to build exceptional applications</p>
            </v-col>
        </v-row>

        <v-row justify="center" align="center" class="mt-6" dense>
            <v-col v-for="(skill, index) in skills" :key="index" cols="6" sm="4" md="3" lg="2"
                class="d-flex justify-center">
                <v-card class="pa-4 text-center" width="180" elevation="4">
                    <img :src="skill.icon" alt="" width="70" height="70" />
                    <div class="font-weight-medium mt-1">{{ skill.name }}</div>
                </v-card>
            </v-col>
        </v-row>
        <v-divider class="mt-10"></v-divider>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            skills: [
                { name: 'HTML', icon: 'https://img.icons8.com/color/48/html-5.png' },
                { name: 'CSS', icon: 'https://img.icons8.com/color/48/css3.png' },
                { name: 'JavaScript', icon: 'https://img.icons8.com/color/48/javascript.png' },
                { name: 'Bootstrap', icon: 'https://img.icons8.com/color/48/bootstrap.png' },
                { name: 'Golang', icon: 'https://img.icons8.com/color/48/golang.png' },
                { name: 'Vue.js', icon: 'https://img.icons8.com/color/48/vue-js.png' },
                { name: 'Maria DB', icon: 'https://img.icons8.com/fluency/48/database.png' },
                { name: 'MySQL', icon: 'https://img.icons8.com/color/48/mysql-logo.png' },
                { name: 'PostgreSQL', icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg' },
                { name: 'Git', icon: 'https://img.icons8.com/color/48/git.png' }
            ]
        }
    }
}
</script>

<style>
.orange-underline {
    width: 50px;
    height: 4px;
    background-color: #f4511e;
    border-radius: 2px;
}
</style>
