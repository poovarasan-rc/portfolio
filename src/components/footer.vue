<template>
    <div>
        <div :class="Desktop ? 'd-flex' : ''">
            <div v-if="Desktop" class="d-flex align-center">
                <!-- <v-avatar rounded color="orange">
                    <strong>
                        <h2 class="white--text">P</h2>
                    </strong>
                </v-avatar> -->
                <div class="ml-4">
                    <h3>POOVARASAN</h3>
                    <div class="grey--text">Software Developer</div>
                </div>
            </div>
            <v-spacer></v-spacer>
            <div class="v-flex text-center">
                <a href="https://www.linkedin.com/in/r-c-poovarasan-790564366" target="_blank" style="font-size: 15px;">
                    <v-btn color="orange" fab text class="mr-4"><v-icon>mdi-linkedin</v-icon></v-btn>
                </a>
                <a href="https://github.com/poovarasan-rc" target="_blank" style="font-size: 15px;">
                    <v-btn color="orange" fab text class="mr-4"><v-icon>mdi-github</v-icon></v-btn>
                </a>
                <a href="mailto:poovarasan.rcfk@gmail.com" target="_blank" style="font-size: 15px;">
                    <v-btn color="orange" fab text class="mr-4"><v-icon>mdi-gmail</v-icon></v-btn>
                </a>
                <!-- <v-btn color="orange" fab text class="mr-4"><v-icon>mdi-linkedin</v-icon></v-btn>
                <v-btn color="orange" fab text class="mr-4"><v-icon>mdi-github</v-icon></v-btn>
                <v-btn color="orange" fab text class="mr-4"><v-icon>mdi-gmail</v-icon></v-btn> -->
            </div>
        </div>
        <v-divider class="mt-5"></v-divider>
        <div class="text-center my-5 grey--text">© 2025 Poovarasan. Crafted with passion and attention to detail.</div>
    </div>
</template>
<script>
export default {
    props: {
        Desktop: Boolean
    }
}
</script>