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
                <a class="smooth-menu" href="#home">Home</a>
              </li>
              <li>
                <a class="smooth-menu" href="#blog">Blog</a>
              </li>
              <li>
                <a class="smooth-menu" href="#services">Services</a>
              </li>
              <li>
                <a class="smooth-menu" href="#portfolio">Portfolio</a>
              </li>
              <li>
                <a class="smooth-menu" href="#about">About</a>
              </li>
              <li>
                <a class="smooth-menu" href="#contact">Contact</a>
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
              <a
                class="smooth-menu"
                href="#"
                @click.prevent="smoothScroll('home')"
              >
                <i class="fas fa-home"></i>
                <div class="menu-name">Home</div>
              </a>
            </li>
            <li>
              <a
                class="smooth-menu"
                href="#"
                @click.prevent="smoothScroll('blog')"
              >
                <i class="fas fa-file-alt"></i>
                <div class="menu-name">Blog</div>
              </a>
            </li>
            <li>
              <a
                class="smooth-menu"
                href="#"
                @click.prevent="smoothScroll('services')"
              >
                <i class="fas fa-cog"></i>
                <div class="menu-name">Services</div>
              </a>
            </li>
            <li>
              <a
                class="smooth-menu"
                href="#"
                @click.prevent="smoothScroll('portfolio')"
              >
                <i class="fas fa-briefcase"></i>
                <div class="menu-name">Portfolio</div>
              </a>
            </li>
            <li>
              <a
                class="smooth-menu"
                href="#"
                @click.prevent="smoothScroll('about')"
              >
                <i class="fas fa-user"></i>
                <div class="menu-name">About</div>
              </a>
            </li>
            <li>
              <a
                class="smooth-menu"
                href="#"
                @click.prevent="smoothScroll('contact')"
              >
                <i class="fas fa-comments"></i>
                <div class="menu-name">Contact</div>
              </a>
            </li>
          </ul>
        </div>
        <div class="logo">
          <a href="#" @click.prevent="smoothScroll('home')"
            ><img src="../assets/img/Logo1.png" alt="Logo"
          /></a>
        </div>
      </div>
    </header>
    <!-- End Header Fixed -->
  </div>
</template>

<script setup>
import { ref } from "vue";
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

function smoothScroll(target) {
  const element = document.getElementById(target);
  element.scrollIntoView({ behavior: "smooth" });
}
</script>

<style lang="scss" scoped></style>
