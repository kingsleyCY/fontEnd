<template>
  <div>
    <a href="#navigation" class="nav-trigger">
      Menu<span></span>
    </a>
    <main>
      <section class="intro"></section>
    </main>
    <nav class="nav-container" id="navigation">
      <header>
        <h2>Navigation</h2>
      </header>
      <ul class="nav">
        <li><a href="javascript:;">About</a></li>
        <li><a href="javascript:;">Services</a></li>
        <li><a href="javascript:;">Portfolio</a></li>
        <li><a href="javascript:;">Clients</a></li>
        <li><a href="javascript:;">Contact</a></li>
      </ul>
    </nav>
    <div class="overlay"></div>
  </div>
</template>

<script>
  export default {
    name: "main-back",
    mounted() {
      var navTrigger = document.getElementsByClassName('nav-trigger')[0];
      var body = document.getElementsByTagName('body')[0];

      navTrigger.addEventListener('click', toggleNavigation);

      function toggleNavigation(event) {
        event.preventDefault();
        body.classList.toggle('nav-open');
      }
    }
  }
</script>

<style scoped lang="scss" type="text/scss">
  main {
    position: relative;
    z-index: 1;
    height: 100vh;
    overflow: hidden;
    box-shadow: 0 0 50px #000;
    transition: transform .3s;
  }
  .nav-open main {
    transform: translateX(-8%) scale(.8);
  }
  .intro {
    width: 100%;
    height: 100vh;
    background: url('https://peterlloyd.photography/img/hero.jpg') no-repeat center center;
    background-size: cover;
  }
  .nav-trigger {
    position: fixed;
    z-index: 4;
    top: 3.5%;
    right: 3.5%;
    width: 44px;
    height: 44px;
    overflow: hidden;
    color: transparent;
    white-space: nowrap;
    text-indent: 100%;
  }
  .nav-trigger span,
  .nav-trigger span::before,
  .nav-trigger span::after {
    position: absolute;
    width: 36px;
    height: 4px;
    background: #f6f8f8;
  }
  .nav-trigger span {
    top: calc(50% - 2px);
    left: calc(50% - 18px);
    transition: background .3s;
  }
  .nav-trigger span::before,
  .nav-trigger span::after {
    content: '';
    top: 0;
    left: 0;
    transition: background .3s, transform .3s;
  }
  .nav-trigger span::before {
    transform: translateY(-12px);
  }
  .nav-trigger span::after {
    transform: translateY(12px);
  }
  .nav-trigger:hover span,
  .nav-trigger:hover span::before,
  .nav-trigger:hover span::after {
    background: white;
  }
  .nav-open .nav-trigger span::before,
  .nav-open .nav-trigger span::after {
    background-color: #333
  }
  .nav-open .nav-trigger span {
    background: transparent;
  }
  .nav-open .nav-trigger span::before {
    transform: rotate(-45deg);
  }
  .nav-open .nav-trigger span::after {
    transform: rotate(45deg);
  }
  .overlay {
    position: fixed;
    z-index: 2;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #748479;
    opacity: 0;
    visibility: hidden;
    transition: opacity .5s, visibility .5s;
  }
  .nav-open .overlay {
    opacity: .6;
    visibility: visible;
  }
  .nav-container {
    position: fixed;
    z-index: 3;
    width: 20%;
    max-width: 300px;
    height: 100%;
    top: 0;
    right: 0;
    padding: 30px 20px;
    background-color: hsla(60, 6%, 35%, .95);
    overflow: auto;
    transform: translateZ(0);
    transform: translateX(100%);
    transition: transform .5s cubic-bezier(.83, .14, .33, 1.05);
  }
  .nav-open .nav-container {
    transform: translateX(0);
  }
  .nav-container h2 {
    margin: 1.5em 0;
    font-size: 1.6rem;
    font-weight: bold;
    text-transform: uppercase;
    color: #333;
  }
  .nav {
    list-style-type: none;
    padding: 0;
    color: #fff;
  }
  .nav a {
    display: block;
    padding: .4em 0;
    font-size: 2.5rem;
    font-weight: bold;
    font-family: serif;
    text-decoration: none;
    color: #f6f8f8;
    transform: translateZ(0);
  }
  .nav-open .nav a {
    animation: slide-links .4s .2s backwards;
  }
  .nav-open .nav li:nth-of-type(2) a {
    animation-delay: .3s;
  }
  .nav-open .nav li:nth-of-type(3) a {
    animation-delay: .4s;
  }
  .nav-open .nav li:nth-of-type(4) a {
    animation-delay: .5s;
  }
  .nav-open .nav li:nth-of-type(5) a {
    animation-delay: .6s;
  }
  @keyframes slide-links {
    0% {
      opacity: 0;
      transform: translateX(80px);
    }
    100% {
      opacity: 1;
      transform: translateX(0);
    }
  }
</style>