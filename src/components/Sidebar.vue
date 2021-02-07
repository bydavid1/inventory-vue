<template>
  <div
    v-if="configData.mainLayoutType == 'vertical-menu'"
    v-bind:class="[
      'main-menu',
      'menu-fixed',
      'menu-accordion',
      'menu-shadow',
      configData.theme === 'light' ? 'menu-light' : 'menu-dark',
    ]"
    data-scroll-to-active="true"
  >
    <div class="navbar-header">
      <ul class="nav navbar-nav flex-row">
        <li class="nav-item mr-auto">
          <a class="navbar-brand" href="/">
            <div class="brand-logo">
              <img src="assets/media/logos/logo-light.png'" class="logo" alt="" />
            </div>
            <h2 class="brand-text mb-0" v-if="configData.templateTitle">
              {{ configData.templateTitle }}
            </h2>
            <h2 class="brand-text mb-0" v-else>
              MOKPOS
            </h2>
          </a>
        </li>
        <li class="nav-item nav-toggle">
          <a class="nav-link modern-nav-toggle pr-0" data-toggle="collapse">
            <i class="bx bx-x d-block d-xl-none font-medium-4 primary"></i>
            <i
              class="toggle-icon bx bx-disc font-medium-4 d-none d-xl-block primary"
              data-ticon="bx-disc"
            ></i>
          </a>
        </li>
      </ul>
    </div>
    <div class="shadow-bottom"></div>
    <div class="main-menu-content">
      <ul
        class="navigation navigation-main"
        id="main-menu-navigation"
        data-menu="menu-navigation"
        data-icon-style="lines"
      >
        <li class="nav-item">
          <a class="nav-link" href="home">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="desktop"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Dashboard</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="suppliers">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="list"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Propiedades</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="products">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="thumbnails-big"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Inventario</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="customers">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="users"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Clientes</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="sales">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="shoppingcart"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Ventas</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="purchases">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="us-dollar"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Compras</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="kardex">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="truck"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Kardex</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="home">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="pie-chart"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Reportes</span>
          </a>
        </li>
      </ul>
    </div>
  </div>

  <div
    v-else
    v-bind:class="[
      'header-navbar',
      'navbar-expand-sm',
      'navbar',
      'navbar-horizontal',
      'navbar-light',
      ' navbar-without-dd-arrow',
      configData.navbarType === 'navbar-static' ? 'navbar-sticky' : '',
    ]"
    role="navigation"
    data-menu="menu-wrapper"
  >
    <div class="navbar-header d-xl-none d-block">
      <ul class="nav navbar-nav flex-row">
        <li class="nav-item mr-auto">
          <a class="navbar-brand" href="/">
            <div class="brand-logo">
              <img src="assets/media/logos/logo-light.png" class="logo" alt="" />
            </div>
            <h2 class="brand-text mb-0" v-if="configData.templateTitle">
              {{ configData.templateTitle }}
            </h2>
            <h2 class="brand-text mb-0" v-else>
              MOKPOS
            </h2>
          </a>
        </li>
        <li class="nav-item nav-toggle">
          <a class="nav-link modern-nav-toggle pr-0" data-toggle="collapse">
            <i class="bx bx-x d-block d-xl-none font-medium-4 primary toggle-icon"></i>
          </a>
        </li>
      </ul>
    </div>
    <div class="shadow-bottom"></div>
    <!-- Horizontal menu content-->
    <div class="navbar-container main-menu-content" data-menu="menu-container">
      <ul
        class="nav navbar-nav"
        id="main-menu-navigation"
        data-menu="menu-navigation"
        data-icon-style="filled"
      >
        <li class="nav-item sidebar-group-active active">
          <a class="nav-link" href="home">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="desktop"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Dashboard</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="suppliers">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="list"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Propiedades</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="products">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="thumbnails-big"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Inventario</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="customers">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="users"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Clientes</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="sales">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="shoppingcart"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Ventas</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="purchases">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="us-dollar"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Compras</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="kardex">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="truck"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Kardex</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="home">
            <i
              class="menu-livicon livicon-evo-holder"
              data-icon="pie-chart"
              style="visibility: visible; width: 60px;"
            >
            </i>
            <span>Reportes</span>
          </a>
        </li>
      </ul>
    </div>
    <!-- /horizontal menu content-->
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  computed: {
    configData() { return this.$store.state.configData; },
  },
};
</script>
