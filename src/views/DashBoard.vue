<template>
  <div class="flex flex-col">
    <nav class="flex items-center justify-between flex-wrap bg-teal-500 p-6">
  <div class="flex items-center flex-shrink-0 text-white mr-6">
    <span @click="mover('dashboard')" class="hover:cursor-pointer font-semibold text-xl tracking-tight">Auditanexo30</span>
  </div>
  <div class="block lg:hidden">
    <button class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white">
      <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
    </button>
  </div>
  <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
    <div class="text-sm lg:flex-grow">
      <span @click="mover('users')" class="hover:cursor-pointer block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
        Usuarios
      </span>
      <span class="hover:cursor-pointer block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4">
        Ordenes
      </span>
      <span class="hover:cursor-pointer block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white">
        Procesos
      </span>
    </div>
    <div>
      <span @click="salir" class="hover:cursor-pointer inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-teal-500 hover:bg-white mt-4 lg:mt-0">Cerrar sesión</span>
    </div>
  </div>
</nav>
<div class="flex flex-col">
    <span class="text-2xl font-semibold mx-auto mt-20">Alertas</span>
  </div>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router';
import { ref } from 'vue';
import axios from 'axios'


const router = useRouter();

const mover = (ruta) =>{
  router.push('/'+ruta);
}

const salir = () => {
  router.push('/');
}
</script>
