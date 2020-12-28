<template>
  <div>
    <q-toolbar class="toolbarMenu text-white" style="back">
      <q-btn flat round dense icon="menu" class="q-mr-sm btnMenu" />
      <q-separator  vertical inset />
      <q-space />
      <q-btn stretch flat label="Sobre mi" />
      <q-btn stretch flat label="Portafolio" />
      <q-btn stretch flat label="Contacto" />
    </q-toolbar>
    <q-img

      class="imgPrincipal"
      src="https://besthqwallpapers.com/Uploads/18-5-2020/133234/thumb2-programming-laptop-in-hands-network-technologies-programming-concepts-website-development-concepts.jpg"
      basic
    />
    <div class="textMensajeCenter">
      <h2>Hola y Bienvenid@</h2>
      <h3 class="line anim-typewriter">Soy  {{ nombreUsuario }}<span>&#160;</span></h3>
      <p class="TextFuncion">Desarrollador web full stack</p>

      <q-btn class="btnCurriculum" label="Descargar CV" color="transparent" @click="inception = true" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'MainLayout',
  data () {
    return {
      nombreUsuario: 'Juan Ramírez Sánchez'
    }
  }
}
</script>
<style scoped>
.toolbarMenu {
   background: transparent !important;
    z-index: 99;
}
.imgPrincipal {
  position: absolute;
  top: 0px !important;
  height: 550px;
}
.btnMenu {
  display:none;
}
.textMensajeCenter {
  z-index:999;
  position: relative;
  text-align: center;
  color:#fff !important;
}
.TextFuncion {
  font-size: 32px;
}
.line {
      position: relative;
      top: 50%;
      width: 8em ;
      margin: 0 auto;
      border-right: 2px solid rgba(255, 255, 255, 0.75);
      font-size: 3.5em;
      text-align: center;
      white-space: nowrap;
      overflow: hidden;
      transform: translateY(-50%);
}
.anim-typewriter {
      animation: typewriter 1s  steps(30) 1s 1 normal both,
      blinkTextCursor 500ms steps(30) infinite normal;
      animation-duration: 4.5s;
      animation-iteration-count: infinite;
}
@keyframes typewriter {
      from {
            width: 0;
      }
     to {
            width: 13em;
            color:red !important;
      }
}

@keyframes blinkTextCursor {
      from  {
            border-right-color: rgba(255, 255, 255, 0.75);
            color:red !important;
      }
      to {
            border-right-color: transparent;
      }
}
.btnCurriculum{
  border-radius: 20px;
  border: 2px solid #fff;
  padding-left:15px !important;
  padding-right:15px !important;
}
</style>
