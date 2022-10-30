<template>
  <header class="container-fluid">
    <div class="row">
      <div class="col-lg-2 col-4 pt-2">
        <div class="side">
          <div class="comps">
            <img class="img-fluid pb-4" src="./assets/index.png" alt="logo" />
            <p
              v-for="(link, i) in links"
              :key="i"
              @click="component = link.comp"
            >
              {{ link.name }}
            </p>
          </div>
        </div>
      </div>
      <div class="col-lg col pt-2">
        <component :is="component" icon="xxx" />
      </div>
    </div>
  </header>
</template>

<script>
// imports
import TheWarnings from "@/components/TheWarnings.vue";
import TheAccordion from "./components/TheAccordion.vue";
import ThePopup from "./components/ThePopup.vue";
export default {
  components: {
    TheWarnings,
    TheAccordion,
    ThePopup,
  },
  data() {
    return {
      component: "TheWarnings",
      links: [
        {
          name: "التنبيهات",
          comp: "TheWarnings",
        },
        {
          name: "الأكورديون",
          comp: "TheAccordion",
        },
        {
          name: "النوافذ المنبثقة",
          comp: "ThePopup",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
/* imports */
@import "./assets/styles/_base.scss";
@import "./assets/styles/_colors.scss";

/* heading color */
h2 {
  color: $headingColor;
}
.container-fluid {
  .row {
    .col-lg-2 {
      background: #faf9f4;
      .side {
        p,
        img {
          padding: 0.5rem;
          color: $headingColor;
          font-weight: bold;
          cursor: pointer;
        }
      }
    }
  }
}
.comps {
  min-height: 100vh;
}
</style>
