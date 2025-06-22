<template>
    <div style="margin: 30px 0px;">
        
        <h2 class="font-weight-bold display-1 text-center">Project</h2>
        <div class="orange-underline mx-auto my-2 mb-10"></div>
        <p class="subtitle-1 text-center">Projects and technical expertise</p>


        <v-row>
            <v-col cols="12" sm="6">
                <v-card class="pa-5">
                    <v-avatar  rounded size="50" color="orange" class="mr-2 mb-2">
                        <v-icon dark size="30">mdi-cash-multiple</v-icon>
                    </v-avatar>
                    <h2 class="orange--text">Allocating Clients Fund</h2>
                    <p class="mt-3">Automated RESTful APIs to report client fund allocation to exchanges, improving financial
                        compliance and operational efficiency.</p>
                    <h5>Key Features & Impact</h5>
                    <div>
                        <div class="d-flex mt-3">
                            <v-icon small color="orange">mdi-star-outline</v-icon>
                            <span class="ml-2">Improved financial compliance accuracy by 25%</span>
                        </div>
                        <div class="d-flex mt-3">
                            <v-icon small color="orange">mdi-star-outline</v-icon>
                            <span class="ml-2">Implemented hourly balance verification</span>
                        </div>
                        <div class="d-flex mt-3">
                            <v-icon small color="orange">mdi-star-outline</v-icon>
                            <span class="ml-2">Used microservice architecture with Vue.js, Go, PostgreSQL</span>
                        </div>
                    </div>
                    <div class="mt-4">
                        <v-chip outlined color="orange" class="ml-3">Vue.js</v-chip>
                        <v-chip outlined color="orange" class="ml-3">Golang</v-chip>
                        <v-chip outlined color="orange" class="ml-3">Postgres</v-chip>
                    </div>
                </v-card>
            </v-col>
            <v-col>
                <v-card class="pa-5">
                    <v-avatar  rounded size="50" color="orange" class="mr-2 mb-2">
                        <v-icon dark size="30">mdi-account</v-icon>
                    </v-avatar>
                    <h2 class="orange--text">Project Management Web App</h2>
                    <p class="mt-3">Full-stack application for task and team coordination with real-time collaboration features and comprehensive project tracking.</p>
                    <h5>Key Features & Impact</h5>
                    <div>
                        <div class="d-flex mt-3">
                            <v-icon small color="orange">mdi-star-outline</v-icon>
                            <span class="ml-2">Real-time task management and updates</span>
                        </div>
                        <div class="d-flex mt-3">
                            <v-icon small color="orange">mdi-star-outline</v-icon>
                            <span class="ml-2">Team collaboration and communication tools</span>
                        </div>
                        <div class="d-flex mt-3">
                            <v-icon small color="orange">mdi-star-outline</v-icon>
                            <span class="ml-2">Project analytics and progress tracking</span>
                        </div>
                    </div>
                    <div class="mt-4">
                        <v-chip outlined color="orange" class="ml-3">Vue.js</v-chip>
                        <v-chip outlined color="orange" class="ml-3">Golang</v-chip>
                        <v-chip outlined color="orange" class="ml-3">MySQL</v-chip>
                    </div>
                </v-card>
            </v-col>
        </v-row>
        <v-divider class="mt-10"></v-divider>

    </div>

</template>