<template>
    <div class="barraLateral__item">
        <div class="barraLateral__enviar_info">
            <div class="barraLateral__enviar_foto">
                <img src="" alt="">
            </div>
            <div class="barraLateral__enviar_conteudo">
                <span class="enviar_nome"></span>
                <span class="enviar_mensagem"></span>
            </div>
        </div>
        <div class="barraLateral__enviar_tempo">
            <span class="enviar_tempo"></span>
        </div>
    </div>
</template>
<script>
export default {
    name: 'BarraLateral'
}
</script>
<style>
@import '../assets/css/lateralBarra.css';
@import '../assets/css/spans.css';
</style>