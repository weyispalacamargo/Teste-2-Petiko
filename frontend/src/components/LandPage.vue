<script setup>
</script>

<template>
  <div>
    <img src="../assets/logo.jpg" alt="logo" class="logo" />
  </div>
  <div>
    "O humilde palete, uma peça de madeira aparentemente insignificante que
    desempenha um papel crucial no movimento global de mercadorias e
    suprimentos."
  </div>
  <br />
  <div>
    <router-link to="/form" custom v-slot="{ navigate }">
      <button @click="navigate" role="link">Faça já o seu pedido</button>
    </router-link>
  </div>
  <br />
  <div>
    A fabricação de paletes de madeira normalmente envolve cortar e montar
    tábuas de madeira para criar uma forma retangular ou quadrada, com espaços
    entre as tábuas para empilhadeiras ou outros equipamentos de manuseio para
    levantar o palete. As placas podem ser tratadas para maior durabilidade e
    para evitar apodrecimento ou infestação.
  </div>
  <br />
  <div>
    A fabricação de paletes de plástico envolve a moldagem de materiais
    plásticos na forma desejada usando calor e pressão. Paletes de plástico são
    conhecidos por sua durabilidade, resistência à umidade e longa vida útil.
  </div>
  <br />
  <div>
    A fabricação de paletes de metal envolve soldagem ou união de componentes de
    metal para criar uma estrutura robusta, geralmente com uma malha de metal ou
    superfície sólida no topo. Paletes de metal são conhecidos por sua
    resistência e durabilidade, tornando-os adequados para cargas pesadas e uso
    prolongado.
  </div>
  <br />
  <div>
    A fabricação de paletes também pode envolver personalização, como adicionar
    recursos ou dimensões específicas para atender aos requisitos de
    determinados setores ou aplicações.
  </div>
  <br />
  <div>
    <p>Reparo de paletes:</p>
    Nossa empresa fixa paletes quebrados ou danificados para prolongar sua vida
    útil e desmonta paletes antigos e recicla os materiais para uso em paletes
    novos ou outros produtos.
  </div>
  <div>
    <p>Coleta e entrega de paletes:</p>
    Nossa empresa oferece serviços de transporte para pegar paletes dos clientes
    e entregá-los nos locais desejados.
  </div>
  <br />
  <div>
    <h3>Nossos produtos:</h3>
    <div>
      <p>Palete de Madeira</p>
      <img src="../assets/palete-madeira.jpg" alt="" class="paleteMadeira" />
    </div>
    <br />
    <br />
    <div>
      <p>Palete de Plástico</p>
      <img src="../assets/palete-plastico.jpg" alt="" class="paletePlastico" />
    </div>
    <br />
    <br />
    <div>
      <p>Palete de Metal</p>
      <img src="../assets/palete-metal.jpg" alt="" class="paleteMetal" />
    </div>
  </div>
  <br />
  <footer>
    <h2>Pallets For Sale</h2>
    <br />
    <div>
      <div>Lorem ipsum dolor</div>
      <div>sitamet, SP 10290190</div>
    </div>
    <br />
    <div>
      <div>loremipsum@gmail.com</div>
      <div>(016)911223344</div>
    </div>
    <br />
  </footer>
</template>

<style scoped>
</style>