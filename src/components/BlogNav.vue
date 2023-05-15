<template>
  <div>
    <header id="home">
      <!-- Start Navigation -->
      <nav
        class="navbar mobile-sidenav onepage-menu mobile-nav-only attr-border navbar-sticky navbar-default validnavs navbar-fixed dark no-background"
      >
        <div
          class="container d-flex justify-content-between align-items-center"
        >
          <!-- Start Header Navigation -->
          <div class="navbar-header">
            <button
              type="button"
              class="navbar-toggle"
              data-target="#navbar-menu"
              @click="collapseNav"
            >
              <i class="fa fa-bars"></i>
            </button>
            <a class="navbar-brand" href="index.html">
              <img src="../assets/img/Logo2.png" class="logo" alt="Logo" />
            </a>
          </div>
          <!-- End Header Navigation -->

          <!-- Collect the nav links, forms, and other content for toggling -->
          <div
            class="collapse navbar-collapse collapse-mobile"
            id="navbar-menu"
            :class="collapseClass"
          >
            <img src="../assets/img/Logo2.png" alt="Logo" />
            <button
              type="button"
              class="navbar-toggle"
              data-target="#navbar-menu"
              @click="collapseNav"
            >
              <i class="fa fa-times"></i>
            </button>

            <ul
              class="nav navbar-nav navbar-right"
              data-in="fadeInDown"
              data-out="fadeOutUp"
            >
              <li>
                <router-link to="/">
                  <div class="menu-name">Home</div>
                </router-link>
              </li>
              <li>
                <a class="smooth-menu" href="#blog">Blog</a>
              </li>
            </ul>
          </div>
          <!-- /.navbar-collapse -->

          <!-- Main Nav -->
        </div>
        <!-- Overlay screen for menu -->
        <div class="overlay-screen"></div>
        <!-- End Overlay screen for menu -->
      </nav>
      <!-- End Navigation -->
    </header>
    <!-- End Header -->

    <!-- Start Header Fixed 
      ============================================= -->
    <header class="header-fixed">
      <div class="f-flex">
        <div class="logo">
          <a href="#home"><img src="../assets/img/Logo1.png" alt="Logo" /></a>
        </div>
        <div class="menu">
          <ul class="nav">
            <li>
              <router-link to="/">
                <i class="fas fa-home"></i>
                <div class="menu-name">Home</div>
              </router-link>
            </li>
            <li>
              <a class="smooth-menu" href="#blog">
                <i class="fas fa-file-alt"></i>
                <div class="menu-name">Blog</div>
              </a>
            </li>
          </ul>
        </div>
        <div class="logo">
          <a href="#home"><img src="../assets/img/Logo1.png" alt="Logo" /></a>
        </div>
      </div>
    </header>
    <!-- End Header Fixed -->
  </div>
</template>

<script setup>
const boolNav = ref(false);
const collapseClass = ref("");
const collapseNav = () => {
  if (boolNav.value) {
    collapseClass.value = "";
  } else {
    collapseClass.value = "show";
  }
  boolNav.value = !boolNav.value;
};
</script>

<style lang="scss" scoped></style>
