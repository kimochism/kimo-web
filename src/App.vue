<template>
  <div id="ContainerDaddy">
    <div id="modal-stack"></div>

    <div id="main-load">
      <div class="loading">
        <div class="loading-letter">K</div>
        <div class="loading-letter">I</div>
        <div class="loading-letter">M</div>
        <div class="loading-letter">O</div>
        <div class="loading-letter">気</div>
        <div class="loading-letter">持</div>
        <div class="loading-letter">ち</div>
      </div>
    </div>

    <MessageBar />
    <Menu />

    <router-view></router-view>

    <Footer />
    <MessageBar />
  </div>
</template>

<script>
import Menu from "./views/shared/menu/component.vue";
import MessageBar from "./views/shared/message-bar/component.vue";
import Footer from "./views/shared/footer/component.vue";

export default {
  name: "App",
  
  components: {
    Menu,
    MessageBar,
    Footer,
  }
};
</script>

<style>

#main-load {
    position:fixed;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.7);
    display:flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.loading {
  display: flex;
  flex-direction: row;
}

.loading-letter {
  font-size: 60px;
  font-weight: normal;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: white;
  animation-name: bounce;
  animation-duration: 2s;
  animation-iteration-count: infinite;
}

.loading-letter:nth-child(2) {
  animation-delay: .1s; 
}
.loading-letter:nth-child(3) {
  animation-delay: .2s;
}
.loading-letter:nth-child(4) {
  animation-delay: .3s; 
}
.loading-letter:nth-child(5) {
  animation-delay: .4s;
}
.loading-letter:nth-child(6) {
  animation-delay: .5s; 
}
.loading-letter:nth-child(7) {
  animation-delay: .6s;
}

@keyframes bounce {
  0% {
    transform: translateY(0px)
  }
  40% {
    transform: translateY(-40px);
  }
  80%,
  100% {
    transform: translateY(0px);
  }
}

.md-theme-default a:not(.md-button):hover{
  text-decoration: none !important;
}

#ContainerDaddy{
  background-color: transparent;
}

.md-theme-default a:not(.md-button){
  color: black;
}
.md-theme-default a:not(.md-button):hover{
  color: black;
  text-decoration: none;
}

* {
  outline: none !important;
}

/* width */
::-webkit-scrollbar {
  width: 10px !important;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1 !important;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #888 !important;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555 !important;
}

html {
  margin: 0px;
  padding: 0px;
  overflow-x: hidden;
}

body {
  margin: 0px;
  padding: 0px;
  font-family: "Kumbh Sans", sans-serif !important;
  text-rendering: optimizeLegibility !important;
  font-weight: 400;
  font-style: normal;
  overflow-x: hidden !important;
}

.custom-toast {
 border-radius: 0px !important;
 padding: 20px !important;
}

.error {
  background: red !important;
}

.success {
  background: #00ae7c !important;
}

</style>
