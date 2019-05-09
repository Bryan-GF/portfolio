<script>
import fontawesome from "@fortawesome/fontawesome";
import {faBars} from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

fontawesome.library.add(faBars);

export default {
  name: 'Nav',
  props: {
    
  },
  components: {
      FontAwesomeIcon
  },
   rules: {
        'no-console': 0,
    },
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
      activeDropdown: false
    }
  },
  mounted () {
  window.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    onScroll: function () {
      // Get the current scroll position
      const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop
      // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      if (currentScrollPosition < 0) {
        return
      }
      if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 20) {
        return
      }
      // Here we determine whether we need to show or hide the navbar
      this.showNavbar = currentScrollPosition < this.lastScrollPosition;
      this.activeDropdown = false;
      // Set the current scroll position as the last scroll position
      this.lastScrollPosition = currentScrollPosition
    },
    scrollChange: function(type) {
      if(type === 'projects') {
        window.scrollTo(0, 550);
      } else if (type === 'contact') {
        window.scrollTo(0, 6000);
      } else if (type === 'projectsDesktop') {
        window.scrollTo(0, 800);
      } else {
        window.scrollTo(0, 6000);
      }

    }
  }
}
</script>

<template>
  <div class="navbar-wrapper">
    <div class="navbar"
        :class="{ 'navbar--hidden': !showNavbar }">
      <div class='logo'>
          <h2>Bryan</h2>
      </div>
      <div class='navMain'>
          <span @click="scrollChange('projectsDesktop')">Projects</span>
          <span class="downloadBoks" onclick="window.open('Bryan_Garcia-Felix_Resume.pdf')">Resume</span>
          <span @click="scrollChange('contactDesktop')">Contact</span>
          <font-awesome-icon icon="bars" v-on:click="activeDropdown = !activeDropdown"/>
      </div>
    </div>
    <div class="dropdown" :class="{'dropdown-hidden': !activeDropdown}">
      <p @click="scrollChange('projects')" v-bind:style="{ borderTop: '2px solid black' }">Projects</p>
      <p class="downloadBoks" onclick="window.open('Bryan_Garcia-Felix_Resume.pdf')">Resume</p>
      <p @click="scrollChange('contact')">Contact</p>
    </div>
  </div>
</template>

<style lang="less">



.navbar {
    display: flex;
    position: fixed;
    align-items: center;
    height: 90px;
    box-shadow: 0 0px 40px 0 rgba(0, 0, 0, .1);
    background: white;
    transform: translate3d(0, 0, 0);
    transition: 0.2s all ease-out;
    width: 100%;

    h2 {
        font-family: 'Pacifico', cursive;
        margin: 0;
    }

}

.navbar.navbar--hidden {
  box-shadow: none;
  transform: translate3d(0, -100%, 0);
}

.navbar-wrapper {
  .dropdown-hidden {
    display: none;
  }

  .dropdown {
    width: 100%;
    position: fixed;
    margin-top: 90px;
    z-index: 10;
    p {
      background: white;
      margin: 0;
      padding: 1rem 1rem 1rem 1.5rem;
      border-bottom: 2px solid black;
      border-left: 2px solid black;
      border-right: 2px solid black;
      font-weight: bold;
      &:hover {
        cursor: pointer;
        background: #F2F2F2;
        color: #ED202E;
      }
    }
  }
}


.logo {
    width: 25%;
    font-size: 1.25rem;
    padding: .5rem;
    margin: 0 2.5rem 0 1rem;
    &:hover {
        cursor: pointer;
    }
}

.navMain {
    width: 75%;
    display: flex;
    justify-content: flex-end;
    padding: 0 1rem 0 1rem;
    span {
        margin-right: 1rem;
        padding: 1rem;
        font-size: 1.25rem;
        font-weight: 700; 
        display: none;
        &:hover {
            cursor: pointer;
            color: #ED202E;
        }
    } 
    svg {
      width: 30px !important;
      height: 30px;
    }
}

@media screen and (min-width: 765px) {
  .logo {
    margin-left: 2.5rem;
  }
  .navMain {
    span {
      display: block;
    }
    svg {
      display: none;
    }
  }
}


</style>