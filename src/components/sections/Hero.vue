<script setup>
import heroImage from '../../assets/hero.png'
import headerImg from '../../assets/iPhone 15 Pro - Black Flatten.png'
import headerLogo from '../../assets/Logo.png'
import numero1 from'../../assets/numero1.png'
import numero2 from'../../assets/numero2.png'
import userPersona1 from '../../assets/userPersona1.png'
import userPersona2 from '../../assets/userPersona2.png'
import tabla1 from '../../assets/tabla1.png'
import tabla2 from '../../assets/tabla2.png'

</script>

<template>

  <section class="hero">

    <!--Imagen superior -->
    <div class="heroImage">
      <img class="bg" :src="heroImage"/>
    </div>

    <!--header-->
    <div class="headerSection">
      <header class="header">
        <div class="frame">
          <img class="logo" :src="headerLogo" alt="Logo"/>
          <p class="text"><b>CNET</b> es un portal global de noticias y reseñas tecnológicas. En este proyecto se realizó un rediseño <b>UX/UI</b> de la sección de <b>comparativa de celulares</b>, con el objetivo de mejorar el flujo de navegación y la <b>interacción del usuario</b> en la versión móvil.</p>
        </div>
        <img class="photo" :src="headerImg" alt="Foto CNET en movil" />
      </header>

      <div class="body">
        <div class="contenedor">
          <div class="contenedorNumeroyTexto">
            <img class="numero" :src="numero1" alt="01"/>
            <p class="h3">En la etapa de <b>empatizar</b> se desarrollaron user personas y user journey maps para comprender los puntos desfavorables y necesidades de los usuarios dentro de la plataforma.</p>
          </div>
          <div class="carrosel">
            <img class="carrosel1" :src="userPersona1" alt="userPersona1"/>
            <img class="carrosel2" :src="userPersona2" alt="userPersona2"/>
          </div>
        </div>
        <div class="contenedor">
          <div class="contenedorNumeroyTexto">
            <img class="tabla1" :src="numero2" alt="02"/>
            <p class="h3">En la etapa de <b>definir</b>, se identificó que el principal problema era un flujo de pasos deficiente para completar la tarea. Los usuarios no sabían cómo realizarla correctamente y, aun cuando lo lograban, no comprendían cómo lo habían hecho, lo que generaba frustración y abandono de la plataforma.</p>
          </div>
          <div class="carrosel">
            <img class="tabla" :src="tabla1" alt="grafico">
            <img class="tabla" :src="tabla2" alt="grafico">
          </div>
        </div>
      </div>

      <div class="links">
      </div>
    </div>
  </section>
</template>
<style scoped>
/* Importación desde Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Schibsted+Grotesk:ital,wght@0,400..900;1,400..900&display=swap');
.hero {
  width: 100%;
}
/* Imagen Superior*/
.heroImage img{
  width: 100%;
  height: auto;
  display: block;
}
/* headerSeccion*/
/* Seccion con fondo*/
.headerSection{
  background: #1D1D27;
  width: 100%;
}
.header{
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  height: 670px;

  display:flex;
  align-items: center;
  justify-content: center;
  gap: clamp(40px, 9vw, 120px);

  color: aliceblue;
}

/*Bloque de texto*/
.frame{
  width: 600px;
  height: 490px;

  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  gap: 24px;
}

/*Logo*/
.logo{
  width: 100%;
  height: auto;
  object-fit: contain;
}

/*Testp*/
.text{
  font-size: 1.1rem;
  line-height: 1.7;
  opacity: 0.9;
}

/*Photo*/
.photo {
  width: clamp(180px, 21vw, 254px);
  height: clamp(360px, 43vw, 521px);
  object-fit: cover;
  border-radius: 20px;
}


/*body*/
.contenedor{
  width: calc(100%- 40px);
  margin: 0 auto;
  background: #D9D9D9;
  padding: 20px;
  margin-left: 20px;
  margin-right: 20px;
  gap: 20px;
}
/*texto superior*/
.contenedorNumeroyTexto{
  display: flex;
  align-items: flex-start;
  gap: 10px;
  justify-content: flex-start;
  font-family: 'Schibsted Grotesk',sans-serif;
  margin-bottom: 20px;
}
.numero{
  width: 30px;
  height: 30px;
  flex-shrink: 0;
}
.h3{
  margin: 0;
  font-size: 22px;
  line-height: 1.2;
  color: #1d1d27;
}
/* carroselUserPersonas*/
.carrosel{
  display: flex;
  gap: 20px;
  overflow-x: auto;
  scroll-behavior: smooth;

  scrollbar-width: none;
  -ms-overflow-style: none;
}
.carrosel::-webkit-scrollbar{
  display: none;
}
.carrosel img{
  flex-shrink: 0;
  width: auto;
  height: 600px;
  object-fit: contain;
}

</style>