<template>
  <div class="pagina">
    <header class="ImgHero">
      <div class="content-img">
        <img :src="hero"/>
      </div>
      <div :class="['content-frame', { 'is-animated': animated }]">
        <div class="cent">
          <div class="frame3">
            <div class="img-logo">
              <img :src="logo"/>
            </div>
            <h3>Este proyecto consiste en el rediseño del sitio web de CENT Mobile, un comparador de celulares, con el objetivo de reducir la tasa de deserción durante el proceso de comparación. Mi rol fue Product Designer, y el proyecto se desarrolló en un período de 4 semanas.</h3>
          </div>
          <img :src="phone">
        </div>
      </div>
    </header>
    <!-- Aparatado de De4sing Thinking-->
    <div class="body">
      <div class="desing-thinking">
        <h3 class="title">Design Thinking</h3><h3>
        Los usuarios presentaban dificultades para comparar los equipos seleccionados, lo que generaba frustración y aumentaba el abandono de la tarea. El principal objetivo del rediseño fue mejorar el flujo de comparación para hacerlo más claro, eficiente e intuitivo.
      </h3>
      </div>
    <div class="conteiner-steps">
      <div class="conteiner-steps-text">
        <img :src="numero1"/>
        <h3>En la etapa de <span class="highlight">empatizar</span> se desarrollaron user personas y user journey maps para comprender los puntos desfavorables y necesidades de los usuarios dentro de la plataforma.</h3>
      </div>
      <div class="carruselImg">
        <div class="carruselImg-track">
          <img :src="img"/>
          <img :src="img1"/>
          <img :src="img2"/>
          <img :src="img3"/>
        </div>
      </div>
    </div>
      <div class="conteiner-steps">
        <div class="conteiner-steps-text">
          <img :src="numero2"/>
          <h3>En la etapa de <span class="highlight">definir</span>, se identificó que el principal problema era un flujo de pasos deficiente para completar la tarea. Los usuarios no sabían cómo realizarla correctamente y, aun cuando lo lograban, no comprendían cómo lo habían hecho, lo que generaba frustración y abandono de la plataforma.</h3>
        </div>
        <div class="carruselImg">
          <div class="carruselImg-track">
            <img :src="img4"/>
            <img :src="img5"/>
          </div>
        </div>
      </div>
      <div class="conteiner-steps">
        <div class="conteiner-steps-text">
          <img :src="numero2"/>
          <h3>En la etapa de <span class="highlight">idear</span>, se creó un mapa de flujo que facilita el recorrido del usuario, junto con el diseño de botones y una interfaz más intuitiva, reduciendo opciones innecesarias para que el usuario pueda completar su camino sin distracciones.</h3>
        </div>
        <div class="imgUserFlow">
          <img :src="img6"/>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
import {ref, onMounted} from 'vue';
const animated =ref(false);
onMounted(() =>{
  setTimeout(() =>{
    animated.value=true;
  },200);
})

import hero from '../../assets/hero.png';
import numero1 from '../../assets/numero1.png';
import numero2 from '../../assets/numero2.png';
import numero3 from '../../assets/numero3.png';
import numero4 from '../../assets/numero4.png';
import img from '../../assets/img.png';
import img1 from '../../assets/img_1.png';
import img2 from '../../assets/img_2.png';
import img3 from '../../assets/img_3.png';
import img4 from '../../assets/img_4.png';
import img5 from '../../assets/img_5.png';
import img6 from '../../assets/img_6.png';
import logo from '../../assets/Logo.png';
import phone from '../../assets/iPhone 15 Pro - Black Flatten.png';
</script>

<style scoped>
.pagina {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;

  width: 100%;
  height: auto;

  background: #1d1d27;
}
.ImgHero {
  position: relative;
  width: 100%;
  height: auto;
  min-height: 652px;
}
.content-img {
  width: 100%;
  height: 100%;
  background: #1d1d27;

  min-height: 652px;
}
.content-img img{
  width: 100%;
  height: 100%;
  object-fit: cover;

  min-height: 652px;
}
.content-frame {
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  bottom: 0;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: auto;

  position: absolute;

  transform: translateY(100%);

  transition: transform 1.2s cubic-bezier(0.19,1,0.22,1);
  will-change: transform;

}
.content-frame.is-animated {
  transform: translateY(0);
}
.cent {
  display: flex;
  justify-content: center;
  align-items: center;
  width: auto;
  height: auto;

  gap: 20px;
  padding: 40px;
  background: #1d1d27;
}
.cent img {
  width: 201px;
  height: 413px;
}
.img-logo {
  width: 100%;
}

.img-logo img {
  width: 601px;
  max-width: 100%;
  height: auto;
  display: block;
}

.frame3 {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;

  width: auto;
  height: auto;

  gap: 10px;

}
.frame3 h3 {
  width: auto;
  max-width: 601px;
  height: auto;
  margin: 0;
}

/*Apartado Desing Thinkin*/
.body {
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: center;

  width: 100%;
  height: auto;

  gap: 20px;
  padding-inline: 40px;
  padding-top: 100px;
}
.desing-thinking {
  justify-items: center;
  max-width: 1000px;
}
.conteiner-steps {
  display: flex;
  flex-direction: column;
  justify-items: start;
  align-items: center;

  width: 100%;
  height: auto;

  padding: 20px;
  gap: 20px;
  background: #d9d9d9;
}
.conteiner-steps-text {
  display: flex;
  flex-direction: row;
  margin: 0;
}
.conteiner-steps-text h3 {
  color: #1d1d27;
}
.highlight{
  font-weight: 600; /* SemiBold */
  font-style: italic;
}
.conteiner-steps-text img{
  width: 26px;
  height: 27px;
}
.carruselImg {
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
  scrollbar-width: none;
  width: 1000px;
}
.carruselImg::-webkit-scrollbar {
  display: none;
}
.carruselImg-track {
  display: inline-flex;

  gap: 20px;
}
.carruselImg img {
  flex: 0 0 auto;
  height: 500px;
  object-fit: contain;
  scroll-snap-align: start;
  display: block;
}
.imgUserFlow {
  width: 100%;
  height: auto;
}
.imgUserFlow img{
  width: 100%;
  object-fit: contain;
}
</style>