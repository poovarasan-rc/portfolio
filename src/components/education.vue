<template>
    <div style="margin: 30px 0px;">
        <h2 class="font-weight-bold display-1 text-center">Education</h2>
        <div class="orange-underline mx-auto my-2"></div>
        <v-card class="pa-5 mx-auto mt-10" max-width="1200" elevation="4" v-for="(item, index) in EduList" :key="index">
            <v-row align="center" no-gutters>
                <!-- Left Icon -->
                <v-col cols="auto">
                    <v-avatar size="50" color="orange" class="mr-4">
                        <v-icon dark>{{ item.icon }}</v-icon>
                    </v-avatar>
                </v-col>
                <!-- Right Content -->
                <v-col>
                    <div :class="Desktop?'d-flex':''">
                        <div><b class="orange--text">{{ item.institute }}</b><br><span>{{ item.course }}</span></div>
                        <v-spacer></v-spacer>
                        <div class="caption grey--text">{{ item.duration }}</div>
                    </div>
                </v-col>
            </v-row>
            <div class="mt-3">
                <span>{{ item.desp }}</span>
            </div>
        </v-card>
        <v-divider class="mt-10"></v-divider>
    </div>
</template>
<script>
export default {
    name:"education",
    data() {
        return {
            EduList: [
                {
                    icon: "mdi-code-tags",
                    institute: "QSPIDER",
                    course: "Java Full Stack Developer",
                    duration: "Oct 2022 - Feb 2023",
                    desp: "Comprehensive training in Java full-stack development, covering both frontend and backend technologies, database management, and modern development practices."
                },
                {
                    icon: "mdi-school",
                    institute: "St. Xavier's College",
                    course: "B.Sc. Computer Science",
                    duration: "2019 - 2022 • 61% Grade",
                    desp: "Bachelor's degree in Computer Science with focus on programming fundamentals, data structures, algorithms, and software engineering principles."
                },
                {
                    icon: "mdi-school",
                    institute: "St. Xavier's Higher Secondary School",
                    course: "Higher Secondary Education",
                    duration: "2017 - 2019 • 72.4% Grade",
                    desp: "Completed higher secondary education with strong academic performance, building foundation in mathematics and sciences."
                },
            ]
        }
    },
    props:{
        Desktop: Boolean
    }
}
</script>