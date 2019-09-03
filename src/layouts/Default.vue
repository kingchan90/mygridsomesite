<template>
  <div class="layout">
    <!-- <header class="header">
      <strong>
        <g-link to="/">{{ $static.metaData.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about">About</g-link>
      </nav>
    </header>-->
    <app-header></app-header>
    <main>
      <slot />
    </main>
    <app-footer></app-footer>
    <app-loader></app-loader>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>
<script>
import Header from "../components/Header";
import Loader from "../components/Loader";
import Footer from "../components/Footer";
export default {
  components: {
    appHeader: Header,
    appLoader: Loader,
    appFooter: Footer
  }
};
</script>
<style>
@include fontFace("Poppins", "../../assets/fonts/Poppins-Regular");
@include fontFace("icomoon", "../../assets/fonts/icomoon");
</style>
