<script setup>
import heroImage from '../../assets/hero.png'
import headerImg from '../../assets/iPhone 15 Pro - Black Flatten.png'
import headerLogo from '../../assets/Logo.png'
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
      </div>

      <div class="links">
      </div>
    </div>
  </section>
</template>
<style scoped>
.hero {
  width: 100%;
}
/* Imagen Superior*/
.heroImage img{
  width: 100%;
  height: auto;
  display: block;
}
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


</style>