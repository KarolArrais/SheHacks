<template>
  <div class="wrapper">
    <side-bar>
      <template slot="links">
        <sidebar-link to="/dashboard" :name="$t('LOA')" icon="tim-icons icon-pin"/>
        <sidebar-link to="/icons" :name="$t('Membros')" icon="tim-icons icon-single-02"/>
        <sidebar-link to="/maps" :name="$t('Artigos')" icon="tim-icons icon-align-center"/>
        <sidebar-link to="/notifications" :name="$t('Extensão/serviços')" icon="tim-icons icon-world"/>
        <sidebar-link to="/profile" :name="$t('Diário de Lab')" icon="tim-icons icon-atom"/>
        <sidebar-link to="/table-list" :name="$t('Colaboração')" icon="tim-icons icon-puzzle-10"/>
      </template>
    </side-bar>
    <div class="main-panel">
      <top-navbar></top-navbar>

      <dashboard-content @click.native="toggleSidebar">

      </dashboard-content>

      <content-footer></content-footer>
    </div>
  </div>
</template>
<style lang="scss">
</style>
<script>
import TopNavbar from "./TopNavbar.vue";
import ContentFooter from "./ContentFooter.vue";
import DashboardContent from "./Content.vue";
import MobileMenu from "./MobileMenu";
export default {
  components: {
    ContentFooter,
    DashboardContent,
    MobileMenu
  },
  methods: {
    toggleSidebar() {
      if (this.$sidebar.showSidebar) {
        this.$sidebar.displaySidebar(false);
      }
    }
  }
};
</script>
