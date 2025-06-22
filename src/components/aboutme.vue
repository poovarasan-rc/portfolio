<template>
    <div style="margin: 30px 0px;">
        <h2 class="font-weight-bold display-1 text-center">About</h2>
        <div class="orange-underline mx-auto my-2 mb-10"></div>

        <v-row style="line-height: 25px; padding: 0px 20px;">
            <v-col md6 lg6 sm12 xs12>
                <div>
                    <div>I’m a detail-oriented and results-driven Software Developer with a strong foundation in both frontend and backend development, specializing in building scalable web applications using Vue.js and Golang.</div>
                    <div class="mt-4">With hands-on experience in RESTful API design, UI integration, and SQL performance optimization, I take pride in writing clean, maintainable code that delivers real-world impact.</div>
                    <div class="mt-4">
                        I’m passionate about performance tuning, code quality, and continuous learning, and I thrive in collaborative, fast-paced environments. Whether it’s architecting new features or solving complex bugs, I’m always driven by the challenge of delivering seamless, user-centric solutions.
                    </div><br><br>
                    <div :class="Desktop ? 'd-flex justify-space-around text-center' : 'text-center'">
                        <v-card class="orange lighten-5 pt-4 mx-auto" width="200">
                            <v-icon color="orange" large>mdi-code-not-equal-variant</v-icon>
                            <h2 class="orange--text">2+</h2>
                            <div class="grey--text text--darken-2 overline">Years Experience</div>
                        </v-card>
                        <v-card class="orange lighten-5 pt-4 mx-auto" width="200">
                            <v-icon color="orange" large>mdi-folder-star</v-icon>
                            <h2 class="orange--text">4+</h2>
                            <div class="grey--text text--darken-2 overline">Projects</div>
                        </v-card>
                    </div>
                </div>
            </v-col>

            <v-col md6 lg6 sm12 xs12>
                <v-card style="padding: 3%;" max-width="600">
                    <div class="d-flex">
                        <v-icon color="orange" class="mt-n4">mdi-trending-up</v-icon>
                        <p class="orange--text ml-2">Core Competencies</p>
                    </div>
                    <div class="d-flex" v-for="(item, idx) in Skills" :key="idx">
                        <p>{{ item.name }}</p>
                        <v-spacer></v-spacer>
                        <!-- <div style="width: 100px;">
                            <v-slider v-model="item.level" readonly></v-slider>
                        </div> -->

                        <v-chip small color="blue-grey lighten-5">
                            <div style="width: 100px; margin-top: 20px;">
                                <v-slider v-model="item.level" readonly color="orange"></v-slider>
                            </div>
                        </v-chip>
                    </div>
                </v-card>

            </v-col>
        </v-row>
        <v-divider class="mt-10"></v-divider>
    </div>
</template>
<script>
export default {
    name: "aboutme",
    data() {
        return {
            Skills: [
                { name: "Full-Stack Development", level: 90 },
                { name: "API Development & Integration", level: 90 },
                { name: "Database Optimization", level: 90 },
                { name: "Performance Tuning", level: 90 }
            ]
        }
    },

    props: {
        Desktop: Boolean
    }
}
</script>