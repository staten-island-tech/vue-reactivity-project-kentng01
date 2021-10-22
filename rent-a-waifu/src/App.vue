<template>

  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
  
</template>

<style lang="scss">


:root {
    --black: #131313;
    --light-black: #232323;
    --white: #fff;
    --off-white: #f0f1f6;
    --dark-grey: #1a2f41;
    --grey: #252c30;
    --lightGrey: #f2f4f6;
    --background-primary: var(--light-black);
    --skill-background: var(--black);
    --card-background: var(--light-black);
    --card-text: var(--white);
    --background-secondary: var(--dark-grey);
    --text-primary: var(--white);
    --text-secondary: var(--black);
    --modal-background: var(--black);
    --modal-text: var(--white);
    --student-text: var(--white);
    --link-text: var(--white);
    --nav-line: var(--white);
    --header-btn: var(--white);
    --footer-icon: var(--light-black);
    --h1: 7.594rem;
    --h2: 5.063rem;
    --h3: 3.375rem;
    --h4: 2.25rem;
    --h5: 1.5rem;
    --smallText: 0.8rem;
    --level-1: 0 1px 3px 0 rgba(0,0,0,0.1),0 1px 2px 0 rgba(0,0,0,0.06);
    --level-1-white: 0 1px 3px 0 hsla(0,0%,100%,0.1),0 1px 2px 0 hsla(0,0%,100%,0.06);
    --level-2: 0 4px 6px -1px rgba(0,0,0,0.1),0 2px 4px -1px rgba(0,0,0,0.06);
    --level-2-white: 0 4px 6px -1px hsla(0,0%,100%,0.06),0 2px 4px -1px hsla(0,0%,100%,0.1);
    --level-3: 0 10px 15px -3px rgba(0,0,0,0.1),0 4px 6px -2px rgba(0,0,0,0.05);
    --level-4: 0 20px 25px -5px rgba(0,0,0,0.1),0 10px 10px -5px rgba(0,0,0,0.04);
    --containerPadding: 2.5%;
    --headerHeight: 3rem;
    --borderRadius: 10px
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

</style>
