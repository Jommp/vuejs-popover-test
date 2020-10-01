<template>
   <div id="app">
      <div class="text-center">
         <VuePopover 
            :groupClass="'user-dropdown'" 
            :buttonClass="'user-menu-btn'"
            class="px-5"
            :position="'right-bottom'"
            :showTriangle="false">

            <template v-slot:button-content>
               <b-avatar size="40px"></b-avatar>
            </template>

            <template v-slot:popover-content >
               <div class="user-intro dropdown-option">
                  <b-avatar  size="60px" class="my-3"></b-avatar>
                  <div class="info">
                     <p>user.fullname</p>
                     <small>user.email</small>
                  </div>
               </div>
               <hr role="separator" aria-orientation="horizontal" class="popover-divider my-2">
               <ul>
                  <li class="dropdown-option">
                     <a href="#">
                        Mi Perfil
                        <b-badge class="ml-4">Actualiza tus datos!</b-badge>
                     </a>
                  </li>
                  <li class="dropdown-option">
                     <a href="#">Mis cursos</a>
                  </li>
                  <li class="dropdown-option">
                     <a href="#">Mis favoritos</a>
                  </li>
                  <li class="dropdown-option">
                     <a href="#">Mis certificados</a>
                  </li>
                  <b-dropdown-divider class="my-2"></b-dropdown-divider>
                  <li class="dropdown-option">
                     <a href="#">
                        Ayuda 
                     </a> 
                  </li>
                  <li class="dropdown-option">
                     <a href="#">
                        Cerrar Sesión
                     </a>
                  </li>
               </ul>
            </template>
         </VuePopover>
      </div>
      
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'
import VuePopover from './components/vuePopover.vue';

export default {
  name: 'App',
  components: {
    VuePopover,
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
