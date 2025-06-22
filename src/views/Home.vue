<template>
  <div :style="getstyle()">
    <Menu @scroll-to="scrollToSection" :Desktop="Desktop" />
    <AboutMe id="about" :Desktop="Desktop" />
    <Education id="education" :Desktop="Desktop" />
    <Technical id="technical" :Desktop="Desktop" />
    <WorkExp id="workExp" :Desktop="Desktop" />
    <Projects id="projects" :Desktop="Desktop" />
    <Footer id="footer" :Desktop="Desktop" />
  </div>
</template>

<script>
// @ is an alias to /src
import Menu from "@/components/menu.vue";
import AboutMe from "@/components/aboutme.vue";
import Education from "@/components/education.vue";
import Technical from "@/components/technical.vue";
import WorkExp from "@/components/workexp.vue";
import Projects from "@/components/project.vue";
import Footer from "@/components/footer.vue";

export default {
  name: "Home",
  data() {
    return {
      // Desktop:true,
      // stylevalue : "margin: 0px 200px;"
    }
  },
  components: {
    Menu,
    AboutMe,
    Education,
    Technical,
    WorkExp,
    Projects,
    Footer,
  },
  methods: {
    getstyle() {
      if (this.Desktop) {
        return "margin: 0px 200px;"
      } else {
        return "margin: 0px 0px;"
      }
    },
    scrollToSection(id) {
      // wait until DOM is updated
      this.$nextTick(() => {
        const el = document.getElementById(id);
        if (el) {
          el.scrollIntoView({ behavior: 'smooth' });
        }
      });
    }
  },
  computed: {
    Desktop() {
      if (this.$vuetify.breakpoint.name == "xs" || this.$vuetify.breakpoint.name == "md" || this.$vuetify.breakpoint.name == "sm") {
        return false
      }
      return true
    }
  },
};
</script>
