<template>
  <div class="navbar-navbar">
    <div class="navbar-logo">
      <img :alt="logoimage_alt" :src="logoimage_src" class="navbar-logoimage" />
      <span class="navbar-logotext">{{ logotext }}</span>
    </div>
    <div class="navbar-menulist">
      <a :href="link_c" target="_blank" rel="noreferrer noopener" class="thqLink navbar-textc">
        {{ text_c }}
      </a>
      <a :href="link_n" target="_blank" rel="noreferrer noopener" class="thqLink navbar-textn">
        {{ text_n }}
      </a>
      <a :href="link_g" target="_blank" rel="noreferrer noopener" class="thqLink navbar-textg">
        {{ text_g }}
      </a>
    </div>
    <div class="navbar-account"><app-button button="Sign Up"></app-button></div>
  </div>
</template>

<script>
import AppButton from './button'

export default {
  name: 'Navbar',
  props: {
    logotext: {
      type: String,
      default: 'CoinCap',
    },
    logoimage_src: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1579623261984-41f9a81d4044?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1000',
    },
    text_n: {
      type: String,
      default: 'News',
    },
    link_n: {
      type: String,
      default: 'news.com',
    },
    logoimage_alt: {
      type: String,
      default: 'image',
    },
    link_g: {
      type: String,
      default: 'GitHub.com',
    },
    text_c: {
      type: String,
      default: 'Cryptocurrencies',
    },
    text_g: {
      type: String,
      default: 'Github',
    },
    link_c: {
      type: String,
      default: 'crypto.com',
    },
  },
  components: {
    AppButton,
  },
}
</script>

<style scoped>
.navbar-navbar {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  padding: var(--dl-space-space-unit);
  position: relative;
  align-items: flex-start;
  flex-direction: row;
  background-color: var(--dl-color-gray-black);
}
.navbar-logo {
  top: 0px;
  left: 16px;
  right: auto;
  display: flex;
  flex-direction: row;
}
.navbar-logoimage {
  width: 32px;
  height: 32px;
  align-self: center;
  object-fit: cover;
  border-radius: var(--dl-radius-radius-round);
}
.navbar-logotext {
  color: var(--dl-color-gray-white);
  font-size: 16px;
  align-self: center;
  margin-left: var(--dl-space-space-halfunit);
}
.navbar-menulist {
  top: auto;
  left: 0px;
  right: 0px;
  width: 270px;
  bottom: 22px;
  margin: auto;
  display: flex;
  align-self: center;
  align-items: center;
  flex-direction: row;
  justify-content: center;
}
.navbar-textc {
  color: var(--dl-color-gray-white);
}
.navbar-textn {
  color: var(--dl-color-gray-white);
  margin-left: var(--dl-space-space-unit);
  margin-right: var(--dl-space-space-unit);
}
.navbar-textg {
  color: var(--dl-color-gray-white);
  margin-left: var(--dl-space-space-halfunit);
  margin-right: var(--dl-space-space-halfunit);
}
.navbar-account {
  display: flex;
  align-items: flex-start;
  flex-direction: row;
}
</style>
