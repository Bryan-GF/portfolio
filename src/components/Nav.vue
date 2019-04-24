<template>
  <div class="navbar"
      :class="{ 'navbar--hidden': !showNavbar }">
    <div class='logo'>
        <h2>Bryan</h2>
    </div>
    <div class='navMain'>
        <span>Projects</span>
        <span>Resume</span>
        <span>Contact</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  props: {
    
  },
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0
    }
  },
  mounted () {
  window.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    onScroll () {
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
      this.showNavbar = currentScrollPosition < this.lastScrollPosition
      // Set the current scroll position as the last scroll position
      this.lastScrollPosition = currentScrollPosition
    }
  }
}
</script>

<style lang="less">


h2 {
    font-family: 'Pacifico', cursive;
    margin: 0;
}

.navbar {
    display: flex;
    position: fixed;
    justify-content: space-between;
    align-items: center;
    height: 90px;
    box-shadow: 0 0px 40px 0 rgba(0, 0, 0, .1);
    background: white;
    transform: translate3d(0, 0, 0);
    transition: 0.2s all ease-out;
    width: 100%;
}

.navbar.navbar--hidden {
  box-shadow: none;
  transform: translate3d(0, -100%, 0);
}

.logo {
    width: 25%;
    font-size: 1.25rem;
    padding: 1rem;
    margin: 0 1.5rem 0 1.5rem;
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
        &:hover {
            cursor: pointer;
            color: #ED202E;
        }
    } 
}


</style>