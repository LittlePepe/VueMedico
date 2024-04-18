<template>
    <div id="telemedicina" data-aos="fade-down" data-aos-delay="100" class="custom-text">
        <h1 class="custom-font" style="color: #763B3B; margin-bottom: 4vh;">Telemedicina</h1>
        <h3 class="custom-font" style="text-align: center;">Você já ouviu falar de um sistema de Telemedicina? Atualmente, este termo é usado para
            definir um sistema on-line de troca de informações médicas e análise de resultados de diferentes exames.
            Estes exames são avaliados e entregues de forma digital, dando apoio para a medicina tradicional e
            funcionando de forma mais rápida e eficaz. Quer conhecer mais sobre o que é Telemedicina?</h3>
        <h5 class="custom-font" style="margin-top: 4vh;">Saiba mais</h5>
        <div class="vertical-line"></div>
    </div>
</template>

<script setup>

import { onMounted } from 'vue';
    import AOS from "aos";

    onMounted(async () =>{
        AOS.init();
    })
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');

.custom-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 100vh;
    margin: 0 auto;
}

.custom-font {
    font-family: "Inter", sans-serif;
    font-weight: normal;
}

.vertical-line {
  height: 100px; 
  width: 2px; 
  background-color: #AE1613;
  margin: 0 auto; 
  margin-top: 7vh;
  margin-bottom: 12vh;
}
</style>