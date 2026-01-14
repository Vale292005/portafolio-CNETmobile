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
import numero3 from '../../assets/numero3.png'
import userFlow from '../../assets/userFlow.png'
import numero4 from '../../assets/numero4.png'
const mislinks=[
  {texto:"Benchmarking-Comparador de Celulares",url:"https://docs.google.com/spreadsheets/d/1u_ppicMli-fzyXzI0t9cM1sIDzzB1vupe9ciQfys_7s/edit?usp=sharing"},
  {texto:"User Persona",url:"https://www.figma.com/board/2KGga2N3wx4sRHcnELcvPr/User-Persona?node-id=0-1&t=rJJ8ujbLBdoFw9Qe-1&fuid=1577445020502448024"},
  {texto:"User JourneyMap",url:"https://www.figma.com/board/vg8CurVffdUdWHx2hPckVc/User-Journey-Map?node-id=0-1&t=PM3OosJf8Aqkl72C-1&fuid=1577445020502448024"},
  {texto:"Diagrama de flujo",url:"https://www.figma.com/board/vg8CurVffdUdWHx2hPckVc/User-Journey-Map?node-id=0-1&t=PM3OosJf8Aqkl72C-1&fuid=1577445020502448024"},
  {texto:"Prototipo",url:"https://www.figma.com/board/vg8CurVffdUdWHx2hPckVc/User-Journey-Map?node-id=0-1&t=PM3OosJf8Aqkl72C-1&fuid=1577445020502448024"}
]
const micontacto=[
  {texto:"Linkedin",url:"https://www.linkedin.com/in/valeria-florez-paz-75ba0337b/"},
  {texto:"Github",url:"https://www.linkedin.com/in/valeria-florez-paz-75ba0337b/"}
]
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
            <img class="numero" :src="numero2" alt="02"/>
            <p class="h3">En la etapa de <b>definir</b>, se identificó que el principal problema era un flujo de pasos deficiente para completar la tarea. Los usuarios no sabían cómo realizarla correctamente y, aun cuando lo lograban, no comprendían cómo lo habían hecho, lo que generaba frustración y abandono de la plataforma.</p>
          </div>
          <div class="carrosel">
            <img class="tabla" :src="tabla1" alt="grafico">
            <img class="tabla" :src="tabla2" alt="grafico">
          </div>
        </div>
        <div class="contenedor">
          <div class="contenedorNumeroyTexto">
            <img class="numero" :src="numero3" alt="03"/>
            <p class="h3">En la etapa de <b>idear</b>, se creó un mapa de flujo que facilita el recorrido del usuario, junto con el diseño de botones y una interfaz más intuitiva, reduciendo opciones innecesarias para que el usuario pueda completar su camino sin distracciones.</p>
          </div>
          <div class="contenedorImg">
            <img class="userFlow" :src="userFlow" alt="userFlow"/>
          </div>
        </div>
        <div class="contenedorBlack">
          <div class="contenedorNumeroyTexto">
            <img class="numero" :src="numero4" alt="04"/>
            <p class="h3Black">En la etapa de <b>prototipar</b>, se diseñó la interfaz utilizando los colores principales de la página para el logo y los botones, aportando un aspecto tecnológico y coherente con la identidad de la marca.</p>
          </div>
          <div class="contenedorImg">
            <a href="https://www.figma.com/design/c9c14N0b7nE9twxRLOyMWI/CNET-mobile?node-id=20-274&t=QguBa9XnPy4J1Z1z-1" rel="noopener noreferrer">
              <img class="photo" :src="headerImg" alt="celular"/>
            </a>
          </div>
        </div>
        <div class="contenedorInfo">
          <div class="referencias">
            <p class="h3Black"><b>Referencias:</b></p>
            <ul class="lista-custom">
              <li v-for="link in mislinks" :key="link.texto">
                <a :href="link.url" target="_blanck" rel="noopener noreferrer">
                  {{link.texto}}
                </a>
              </li>
            </ul>
          </div>
          <div class="contacto">
            <p class="h3Black"><b>Contacto:</b></p>
            <ul class="lista-custom">
              <li v-for="link in micontacto" :key="link.texto">
                <a :href="link.url" target="_blank" rel="noopener noreferrer">
                  {{link.texto}}
                </a>
              </li>
            </ul>
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
  background: linear-gradient(180deg ,#1D1D27 86%,black 91%);
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

.contenedorImg{
  display: flex;
  justify-content: center;
  width: 100%;
}
.userFlow{
  flex-shrink: 0;
  height: 1500px;
  width: auto;
}

.contenedorBlack{
  width: calc(100%- 40px);
  margin: 0 auto;
  gap: 20px;
  padding: 20px;
  height: auto;
}
.h3Black{
  margin: 0;
  font-size: 22px;
  line-height: 1.2;
  color: #ffffff;
}


/* 1. Contenedor principal (ul) */
.lista-custom {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

/* 2. Todos los estados del enlace (a) para eliminar el azul y el morado */
.lista-custom li a,
.lista-custom li a:link,
.lista-custom li a:visited {
  color: #FFFFFF !important; /* Texto siempre blanco */
  text-decoration: none !important;
  font-family: 'Schibsted Grotesk', sans-serif;
  font-size: 1.1rem;
  font-weight: 500;
  transition: all 0.3s ease;
  display: inline-block;
}

/* 3. Efecto Hover (Rosa EA5FE9) */
.lista-custom li a:hover {
  color: #EA5FE9 !important; /* Tu color rosa */
  transform: translateX(8px); /* Se mueve a la derecha */
  text-decoration: underline !important;
}

/* 4. Estado activo (cuando haces clic) */
.lista-custom li a:active {
  color: #EA5FE9 !important;
}

.contenedorInfo{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 512px;
  width: auto;
  gap: 10px;
}
.referencias{
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
  width:100%;
}
.contacto{
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
  width: 100%;
}

</style>