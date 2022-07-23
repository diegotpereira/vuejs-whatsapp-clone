<template>
  <div id="app">
    <div class="barraLateral">
      <CabecalhoBarraLateral />
      <div class="barraLateral__corpo">
        <BarraLateral 
        v-for="(mensagem, index) in indices" :key="index" 
        :ativaMensagem="index == ativoIndice"
        :usuarioFoto="mensagem.imagem" :usuarioNome="mensagem.usuario" 
        v-on:click.native="ativoIndice = index"
        :ultimaMensagem="mensagem.mensagens[0].conteudo"
        :ultimaMensagemTempo="mensagem.mensagens[0].tempo"
        
        />
      </div>
    </div>
    <div class="mensagemVisualizar">
      <div class="mensagemVisualizar__cabecalho">
        <div class="mensagemVisualizar__usuario">
          <img v-bind:src="indices[ativoIndice].imagem" alt="">
          <span>{{ indices[ativoIndice].usuario }}</span>
        </div>
        <div class="mensagemVisualizar__cabecalho__icones">
          <font-awesome-icon class="mensagemVisualizar__cabecalho__icone" icon="fa-solid fa-magnifying-glass" />
          <font-awesome-icon class="mensagemVisualizar__cabecalho__icone" icon="fa-solid fa-ellipsis-vertical" />
        </div>
      </div>
      <div class="mensagemVisualizar__corpo">
        <CorpoMensagem :conteudo="mensagem.conteudo" :tempo="mensagem.tempo" :enviar="mensagem.enviar"
        v-for="(mensagem, index_) in indices[ativoIndice].mensagens" :key="index_"/>
      </div>
      <div class="mensagemVisualizar__footer">
        <div class="mensagemVisualizar__footer_icones">
          <font-awesome-icon class="mensagemVisualizar__footer_icone" icon="fa-solid fa-face-laugh-beam"/>
          <font-awesome-icon class="mensagemVisualizar__footer_icone" icon="fa-solid fa-paperclip "/>
        </div>
        <div class="mensagemVisualizar__entrada">
          <input type="text" v-on:keyup.enter="enviarMensagem" placeholder="escreve uma mensagem" v-model="conteudoEnviar">
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

import indicesMensagens from './assets/js/mensagens'



export default {
  name: 'App',
  data() {
    return {
      indices: indicesMensagens,
      
      ativoIndice: 0,
      conteudoEnviar: ''
    }
  },
  components: {
    CabecalhoBarraLateral,
    BarraLateral,
    CorpoMensagem
  },
  methods: {
    enviarMensagem: function() {
      
      let tempoPresente = new Date().getHours() + ":" + new Date().getMinutes()
      
      let novaMensagem = {
        tempo: tempoPresente,
        conteudo: this.conteudoEnviar,
        enviar: true 
      }
      
      this.indices[this.ativoIndice]
      .mensagens.push(novaMensagem)

      this.conteudoEnviar = ''
    }
    
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

.active{
  background-color: #2A3942;
}
</style>
