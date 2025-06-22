<template>
    <div>
        <v-app-bar app dark v-if="Desktop">
            <div class="d-flex align-center">
                <v-avatar rounded color="orange"><strong>
                        <h2>P</h2>
                    </strong></v-avatar>
                <h3 class="ml-2">POOVARASAN</h3>
            </div>
            <v-spacer></v-spacer>
            <div>
                <v-btn v-for="item in menuItems" :key="item.id" small text color=""
                    @click="$emit('scroll-to', item.id)">{{ item.label }}</v-btn>
            </div>
        </v-app-bar>

        <v-btn v-if="!Desktop" fab color="orange" dark fixed top right class="v-btn--example" @click="drawer = true">
            <v-icon>mdi-menu</v-icon>
        </v-btn>
        <v-navigation-drawer v-model="drawer" fixed temporary v-if="!Desktop">
            <v-list-item>
                <v-list-item-avatar>
                    <!-- <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img> -->

                    <v-icon>mdi-menu</v-icon>
                </v-list-item-avatar>

                <v-list-item-content>
                    <v-list-item-title>Menu</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
            <v-divider></v-divider>
            <v-list-item v-for="item in menuItems" :key="item.id" link
                @click="$emit('scroll-to', item.id); drawer = false">
                <!-- <v-list-item-icon>
                    <v-icon>{{ item.ico }}</v-icon>
                </v-list-item-icon> -->

                <v-list-item-content>
                    <v-list-item-title>{{ item.label }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>

        </v-navigation-drawer>
        <div style="align-items: center;justify-items: center; padding: 30px 0px;">

            <v-avatar size="100" class="orange-shadow" color="#FF91009D">
                <h1 class="white--text">P</h1>
            </v-avatar>
            <div style="margin-top: 40px;">
                <v-chip outlined color="orange">👋 Welcome to my portfolio</v-chip>
            </div>
            <div style="font-family: 'Times New Roman', Times, serif; margin: 20px 0px; font-size: 25px;">
                <h1 class="ml-2">SOFTWARE</h1>
                <h1 class="orange--text mt-n2">DEVELOPER</h1>
            </div>
            <div style="font-size: 22px; margin-bottom: 20px; font-family: 'Courier New', Courier, monospace;"
                :class="getStyle()">
                Detail-oriented and solution-driven developer based in Chennai, specializing in building scalable web
                applications with modern technologies.
            </div>
            <v-layout v-if="Desktop">
                <v-flex v-for="(item, index) in Details" :key="index" class="mx-5">
                    <v-icon color="orange">{{ item.icon }}</v-icon>
                    <i class="ml-2">{{ item.text }}</i>
                </v-flex>
            </v-layout>
            <v-row v-else>
                <v-col cols="12" v-for="(item, index) in Details" :key="index">
                    <div class="text-center">
                        <v-icon color="orange">{{ item.icon }}</v-icon>
                        <i class="ml-2">{{ item.text }}</i>
                    </div>
                </v-col>
            </v-row>


            <div style="margin: 30px 0px 15px 0px;">
                <a href="/files/resume.pdf" download="Poovarasan_Resume.pdf" target="_blank">
                    <v-btn color="orange" small class="white--text">
                        <v-icon left>mdi-download</v-icon>
                        Download Resume
                    </v-btn>
                </a>
            </div>

            <v-layout>
                <v-flex v-for="(item, index) in links" :key="index">
                    <a :href="item.url" target="_blank" style="font-size: 15px;">
                        <v-btn color="orange" fab text class="mr-4"><v-icon>{{ item.icon }}</v-icon></v-btn>
                    </a>
                </v-flex>
            </v-layout>
        </div>
        <v-divider></v-divider>
    </div>
</template>
<script>
export default {
    name: "menu",
    data() {
        return {
            drawer: false,
            group: null,
            Details: [
                { icon: "mdi-phone-outline", text: "+91 9344241588" },
                { icon: "mdi-email-outline", text: "poovarasan.rcfk@gmail.com" },
                { icon: "mdi-map-marker-radius-outline", text: "Chennai - 600050" }
            ],
            links: [
                { text: "LinkedIn", icon: "mdi-linkedin", url: "https://www.linkedin.com/in/r-c-poovarasan-790564366" },
                { text: "Github", icon: "mdi-github", url: "https://github.com/poovarasan-rc" }
            ],
            menuItems: [
                { icon: "mdi-account", label: "About", id: "about" },
                { icon: "mdi-account", label: "Education", id: "education" },
                { icon: "mdi-account", label: "Skills", id: "technical" },
                { icon: "mdi-account", label: "Experience", id: "workExp" },
                { icon: "mdi-account", label: "Projects", id: "projects" },
                { icon: "mdi-account", label: "Contact", id: "about" },
            ]
        }
    },
    props: {
        Desktop: Boolean
    },
    methods: {
        getStyle() {
            if (this.Desktop) {
                return "contentDes"
            } else {
                return "contentMob"
            }
        },
        // downloadPDF() {
        //     const link = document.createElement('a');
        //     link.href = '/files/Resume.pdf'; // Or a remote URL
        //     link.setAttribute('download', 'Poovarasan_Resume.pdf');
        //     document.body.appendChild(link);
        //     link.click();
        //     document.body.removeChild(link);
        // }
    }
}
</script>
<style scoped>
.orange-shadow {
    box-shadow: 0 0px 30px 10px rgba(255, 145, 0, 0.616);
    /* orange colored shadow */
}

.contentDes {
    max-width: 50%;
}

.contentMob {
    margin: 0px 30px;
}

/* This is for documentation purposes and will not be needed in your application */
#lateral .v-btn--example {
    bottom: 0;
    position: relative;
    margin: 0 0 16px 16px;
}
</style>