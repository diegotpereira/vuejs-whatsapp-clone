<template>
    <div class="barraLateral__item" v-bind:class="{ativa: ativaMensagem }">
        <div class="barraLateral__enviar_info">
            <div class="barraLateral__enviar_foto">
                <img v-bind:src="usuarioFoto" alt="">
            </div>
            <div class="barraLateral__enviar_conteudo">
                <span class="enviar_nome">{{ usuarioNome }}</span>
                <span class="enviar_mensagem">{{ ultimaMensagem }}</span>
            </div>
        </div>
        <div class="barraLateral__enviar_tempo">
            <span class="enviar_tempo"></span>
        </div>
    </div>
</template>
<script>
export default {
    name: 'BarraLateral',
    data() {
        return {
            
        }
    },
    props: [
        'usuarioNome', 'ultimaMensagem', 'ativaMensagem', 'usuarioFoto', 'ultimaMensagemTempo'
    ]
}
</script>
<style>
@import '../assets/css/lateralBarra.css';
@import '../assets/css/spans.css';
</style>