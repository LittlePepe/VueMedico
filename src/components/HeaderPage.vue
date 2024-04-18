<template >
  <v-app id="inicio">
    <v-container class="header-container" fill-height align-center>
      <v-row align="center" no-gutters>
        <v-col cols="12" sm="6" class="text-center">
          <h1 class="textostyle" style="font-weight: bold; margin-bottom: 20px;">VENHA FAZER PARTE</h1>
          <h1 class="textostyle mb-10">Somos uma central de laudos que atende clínicas e médicos do mundo inteiro através de um dos melhores sistemas de Telemedicina disponíveis. Quer fazer parte?</h1>
          <v-btn @click="scrollToElement('telemedicina')" flat outlined height="6vh" color="white" rounded class="custom-button">Saiba mais<v-icon right style="color:#AE1613">mdi-menu-down</v-icon></v-btn>
        </v-col>
        <v-col cols="12" sm="6" class="text-center">
          <h1 class="textostyle">LOGO</h1>
        </v-col>
      </v-row>
    </v-container>
    <div data-aos="fade-down" data-aos-delay="50" class="vertical-line"></div>
  </v-app>

</template>

<script setup>
import { onMounted } from 'vue';
import AOS from "aos";

onMounted(async () =>{
    AOS.init();
});

const scrollToElement = (id) => {
  const element = document.getElementById(id);
  if (element) {
    const topOffset = element.getBoundingClientRect().top;
    window.scrollBy({ top: topOffset - 200, behavior: 'smooth' });
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');

.header-container {
  background-color: #AE1613;
  display: flex;
  padding: 10vh;
  padding-left: 20vh;
  height: 90vh;
  max-width: 300vh;
  margin: 0%;
}

.textostyle {
  color: white;
  font-family: "Inter", sans-serif;
  font-size: 3vh;
  font-weight: 300;
}

.custom-button {
  font-size: 20px !important;
  font-weight: 800;
  color: #AE1613 !important;
}

.vertical-line {
  height: 100px; 
  width: 2px; 
  background-color: #AE1613;
  margin: auto; 
  margin-top: 12vh;
  margin-bottom: 5vh;
}
</style>
