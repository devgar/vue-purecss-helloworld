<template>
  <div id="app">
    <app-header id="app-header"></app-header>
    <hello></hello>
    <app-footer id="app-footer"></app-footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader'
import AppFooter from './components/AppFooter'
import Hello from './components/Hello'

export default {
  name: 'app',
  components: {
    AppHeader,
    AppFooter,
    Hello
  }
}
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  * {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }

  /*
  * -- BASE STYLES --
  * Most of these are inherited from Base, but I want to change a few.
  */
  html {
    position: relative;
    min-height: 100%;
  }

  body {
    line-height: 1.7em;
    color: #7f8c8d;
    font-size: 13px;
    margin: 50px 0 40px; /* top = header height && bottom = footer height */
  }

  h1,
  h2,
  h3,
  h4,
  h5,
  h6,
  label {
    color: #34495e;
  }

  .pure-img-responsive {
    max-width: 100%;
    height: auto;
  }

  /*
  * -- LAYOUT STYLES --
  * These are some useful classes which I will need
  */
  .l-box {
    padding: 1em;
  }

  .l-box-lrg {
    padding: 2em;
    border-bottom: 1px solid rgba(0,0,0,0.1);
  }

  .is-center {
    text-align: center;
  }

  /*
  * -- PURE FORM STYLES --
  * Style the form inputs and labels
  */
  .pure-form label {
    margin: 1em 0 0;
    font-weight: bold;
    font-size: 100%;
  }

  .pure-form input[type] {
    border: 2px solid #ddd;
    box-shadow: none;
    font-size: 100%;
    width: 100%;
    margin-bottom: 1em;
  }

  /*
  * -- PURE BUTTON STYLES --
  * I want my pure-button elements to look a little different
  */
  .pure-button {
    background-color: #1f8dd6;
    color: white;
    padding: 0.5em 2em;
    border-radius: 5px;
  }

  a.pure-button-primary {
    background: white;
    color: #1f8dd6;
    border-radius: 5px;
    font-size: 120%;
  }

  /* This is the class used for the main content headers (<h2>) */
  .content-head {
    font-weight: 400;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin: 1em 0 1em;
  }

  /* This is a modifier class used when the content-head is inside a ribbon */
  .content-head-ribbon {
    color: white;
  }

  /* This is the class used for the content sub-headers (<h3>) */
  .content-subhead {
    color: #1f8dd6;
  }
    .content-subhead i {
        margin-right: 7px;
    }

  /* This is the class used for the dark-background areas. */
  .ribbon {
    background: #2d3e50;
    color: #aaa;
  }

  /*
  * -- TABLET (AND UP) MEDIA QUERIES --
  * On tablets and other medium-sized devices, we want to customize some
  * of the mobile styles.
  */
  @media (min-width: 48em) {

    /* We increase the body font size */
    body {
        font-size: 16px;
    }
    /* We want to give the content area some more padding */
    .content {
        padding: 1em;
    }

    /* We remove the border-separator assigned to .l-box-lrg */
    .l-box-lrg {
        border: none;
    }

  }

</style>