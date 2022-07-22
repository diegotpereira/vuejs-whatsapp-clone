<template>
  <div id="app">
    <div class="barraLateral">
      <CabecalhoBarraLateral />
      <div class="barraLateral__corpo">
        <BarraLateral />
      </div>
    </div>
    <div class="mensagemVisualizar">
      <div class="mensagemVisualizar__cabecalho">
        <div class="mensagemVisualizar__usuario">
          <img src="" alt="">
          <span></span>
        </div>
        <div class="mensagemVisualizar__cabecalho__icones">
          <font-awesome-icon class="mensagemVisualizar__cabecalho__icone" icon="fa-solid fa-magnifying-glass" />
          <font-awesome-icon class="mensagemVisualizar__cabecalho__icone" icon="fa-solid fa-ellipsis-vertical" />
        </div>
      </div>
      <div class="mensagemVisualizar__corpo">
        <CorpoMensagem />
      </div>
      <div class="mensagemVisualizar__footer">
        <div class="mensagemVisualizar__footer_icones">
          <font-awesome-icon class="mensagemVisualizar__footer_icone" icon="fa-solid fa-face-laugh-beam"/>
          <font-awesome-icon class="mensagemVisualizar__footer_icone" icon="fa-solid fa-paperclip "/>
        </div>
        <div class="mensagemVisualizar__entrada">
          <input type="text" name="" id="" placeholder="escreve uma mensagem">
        </div>
        <font-awesome-icon class="mensagemVisualizar__footer_icone" icon="fa-solid fa-microphone" />
      </div>
    </div>
  </div>
</template>

<script>
import CabecalhoBarraLateral from './components/CabecalhoBarraLateral.vue'
import BarraLateral from './components/BarraLateral.vue'
import CorpoMensagem from './components/CorpoVisualizacaoMensagem.vue'

export default {
  name: 'App',
  components: {
    CabecalhoBarraLateral,
    BarraLateral,
    CorpoMensagem
  }
}
</script>

<style>
@import 'assets/css/lateralBarra.css';
@import 'assets/css/visualizarMensagem.css';

#app {
  display: flex;
  padding: 10px 150px;
}
::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background: #111B21;
}
::-webkit-scrollbar-thumb {
  background: #202C33;
}
.active {
  background-color: #2A3942;
}
</style>
