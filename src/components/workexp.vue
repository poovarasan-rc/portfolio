<template>
    <div style="margin: 30px 0px;">

        <h2 class="font-weight-bold display-1 text-center">Work Experience</h2>
        <div class="orange-underline mx-auto my-2 mb-10"></div>

        <v-row justify="center">
            <v-col cols="12" md="10" lg="12">
                <v-card class="pa-5 mx-auto" elevation="4" max-width="1200">
                    <v-row align="center" no-gutters dense>
                        <v-col cols="auto">
                            <v-avatar size="70" color="orange" class="mr-4">
                                <v-icon dark size="30">mdi-briefcase</v-icon>
                            </v-avatar>
                        </v-col>
                        <v-col>
                            <h1 class="orange--text">
                                Software Developer
                            </h1>
                            <div class="font-weight-bold text--primary mb-1">
                                Fortune Capital Service Pvt Ltd
                            </div>
                            <div class="grey--text mb-4">
                                <v-icon small class="mr-1">mdi-calendar</v-icon> Mar 2023 - Present
                            </div>
                        </v-col>
                    </v-row>

                    <v-row dense>
                        <!-- Column 1 -->
                        <v-col cols="12" sm="6">
                            <div class="font-weight-bold orange--text">Key Responsibilities & Contributions</div>
                            <ul class="pl-4">
                                <li class="mt-2">Took on team leadership responsibilities, acted as team lead on key projects for the past 6 months.</li>
                                <li class="mt-2">Designed and developed scalable, responsive web applications using Vue.js for frontend and Golang for backend services.</li>
                                <li class="mt-2">Created and maintained RESTful APIs, improving data handling and reducing processing latency by 20%.</li>
                                <li class="mt-2">Optimized SQL queries and database structures in MySQL and PostgreSQL to boost performance and reliability.</li>
                            </ul>
                        </v-col>

                        <!-- Column 2 -->
                        <v-col cols="12" sm="6">
                            <div class="font-weight-bold orange--text">Impact & Achievements</div>
                            <ul class="pl-4">
                                <li class="mt-2">Mentored junior developers through feature planning, code reviews, and delivery cycles</li>
                                <li class="mt-2">Enforced coding standards, and fostered a collaborative team culture.</li>
                                <li class="mt-2">Seamlessly integrated UI components with backend APIs, ensuring a smooth user experience across platforms.</li>
                                <li class="mt-2">Implemented unit and integration tests, reducing production bugs by 30% and increasing system reliability.</li>
                            </ul>
                        </v-col>
                    </v-row>
                </v-card>
            </v-col>
        </v-row>
        <v-divider class="mt-10"></v-divider>
    </div>
</template>

<style scoped>
ul {
    padding-left: 16px;
    list-style: none;
    margin-top: 15px;
}

ul li::before {
    content: "•";
    color: #f4511e;
    font-weight: bold;
    display: inline-block;
    width: 1em;
    margin-left: -1em;
}
</style>
