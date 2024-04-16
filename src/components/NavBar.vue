<template>
  <v-toolbar height="80" color="#ffffff" :elevation="5">
      <v-toolbar-title class="text-h5"><strong style="color: #D80000;">ECG</strong><span style="color: #763B3B;"> ONLINE</span></v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-sm-and-down ">
          <v-btn v-for="item in menu" :key="item.icon" :to="item.link" flat color="#763B3B">{{ item.title }}</v-btn>
      </v-toolbar-items>

      <!-- PARA CELULAR

    <v-menu class="hidden-md-and-up">
      <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>
      <v-list>
        <v-list-tile v-for="item in menu" :key="item.icon">
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
           </v-list-tile-content>
        </v-list-tile>   
      </v-list>
    </v-menu> 
  
  -->

  </v-toolbar>
</template>

<script setup>

import { ref } from 'vue';

const menu = ref([
  { icon: 'home', title: 'Inicio', link: '/inicio' },
  { icon: 'info', title: 'Telemedicina', link: '/telemedicina' },
  { icon: 'warning', title: 'Equipe', link: '/equipe' },
  { icon: 'warning', title: 'Modalidades', link: '/modalidades' }
]);

</script>

<style scoped>

.font-nave{
font-size: x-large;
}
.v-toolbar-title {
  color: #D80000
}

.v-toolbar {
  padding-left: 20%;
  padding-right: 20%;
}
</style>
