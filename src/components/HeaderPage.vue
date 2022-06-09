<template>
  <div class="container">
    <div class="logo">
      <img src="../assets/images/logo.svg" alt="" />
    </div>
    <nav>
      <button class="buger-button" @click="toggleMenu = !toggleMenu">
        <img
          src="../assets/images/icon-hamburger.svg"
          alt=""
          v-show="toggleMenu"
        />
        <img
          src="../assets/images/icon-close.svg"
          alt=""
          v-show="!toggleMenu"
        />
      </button>
      <div class="menu" :class="{ hide: toggleMenu }">
        <ul>
          <li :class="{ open: product }">
            <button @click="product = !product">
              Product
              <img
                src="../assets/images/icon-arrow-light.svg"
                alt=""
                class="desktop"
              />
              <img
                src="../assets/images/icon-arrow-dark.svg"
                alt=""
                class="mobile"
              />
            </button>
            <ul :class="{ open: product }">
              <li><button>Overview</button></li>
              <li><button>Pricing</button></li>
              <li><button>Marketplace</button></li>
              <li><button>Features</button></li>
              <li><button>Integrations</button></li>
            </ul>
          </li>
          <li :class="{ open: company }">
            <button @click="company = !company">
              Company
              <img
                src="../assets/images/icon-arrow-light.svg"
                alt=""
                class="desktop"
              />
              <img
                src="../assets/images/icon-arrow-dark.svg"
                alt=""
                class="mobile"
              />
            </button>
            <ul :class="{ open: company }">
              <li><button>About</button></li>
              <li><button>Team</button></li>
              <li><button>Blog</button></li>
              <li><button>Careers</button></li>
            </ul>
          </li>
          <li :class="{ open: connect }">
            <button @click="connect = !connect">
              Connect
              <img
                src="../assets/images/icon-arrow-light.svg"
                alt=""
                class="desktop"
              />
              <img
                src="../assets/images/icon-arrow-dark.svg"
                alt=""
                class="mobile"
              />
            </button>
            <ul :class="{ open: connect }">
              <li><button>Contact</button></li>
              <li><button>Newsletter</button></li>
              <li><button>LinkedIn</button></li>
            </ul>
          </li>
        </ul>
        <div class="buttons">
          <button>Login</button>
          <button>Sign Up</button>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggleMenu: true,
      product: false,
      company: false,
      connect: false,
    };
  },
};
</script>
