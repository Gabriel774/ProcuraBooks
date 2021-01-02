<template>
  <div id="contato">
    <h1 class="titletxt">Onde Estamos/Contato</h1>
    <br />
    <v-expansion-panels style="z-index: 0">
      <v-expansion-panel>
        <v-expansion-panel-header>Localização</v-expansion-panel-header>
        <v-expansion-panel-content
          style="text-align: center; display: flex; flex-direction: column"
        >
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d14631.833095019545!2d-46.58047672279239!3d-23.534003132152897!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce5ee7acdd50f5%3A0x3eeaf24eff368507!2zVGF0dWFww6ksIFPDo28gUGF1bG8gLSBTUA!5e0!3m2!1spt-BR!2sbr!4v1608579107092!5m2!1spt-BR!2sbr"
            width="600"
            height="450"
            id="mapa"
            frameborder="0"
            allowfullscreen=""
            aria-hidden="false"
            tabindex="0"
            style="text-align: center"
          >
          </iframe>
        </v-expansion-panel-content>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-header>Contato Empresarial</v-expansion-panel-header>
        <v-expansion-panel-content
          style="text-align: center; display: flex; flex-direction: column"
        >
          <p class="subtxt">
            Telefone 1: +55(11)2439-6401 <br />
            Telefone 2: +55(11)91242-4220 <br />
          </p>
        </v-expansion-panel-content>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-header>Contato Comercial</v-expansion-panel-header>
        <v-expansion-panel-content
          style="text-align: center; display: flex; flex-direction: column"
        >
          <p class="subtxt">
            Telefone 1: +55(11)2549-8731 <br />
            Telefone 2: +55(11)94914-6720 <br />
            E-mail: contato@procurabooks.com.br
          </p>
        </v-expansion-panel-content>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-header
          >Perguntas Frequentes</v-expansion-panel-header
        >
        <v-expansion-panel-content
          style="text-align: center; display: flex; flex-direction: column"
        >
          <p class="subtxt">
            P - Qual o horário de funcionamento? <br />
            R - das 8:00 até 19:30.
          </p>
          <p class="subtxt">
            P - Onde posso saber se o título que eu quero está disponível?
            <br />
            R - Ligue pelo nosso telefone Comercial: Telefone 1:
            +55(11)2549-8731, Telefone 2: +55(11)94914-6720.
          </p>
          <p class="subtxt">
            P - Posso reservar ou encomendar títulos pelo telefone? <br />
            R - Sim.
          </p>
          <p class="subtxt">
            P - Como é tabelado os valores de títulos? <br />
            R - Por raridade e estado de conservação.
          </p>
          <p class="subtxt">
            P - Posso pedir a entrega de títulos em minha residência? <br />
            R - Sim, porém somente em São Paulo - SP, cheque a aba Entrega
            Domiciliar para mais detalhes.
          </p>
        </v-expansion-panel-content>
      </v-expansion-panel>
      <v-expansion-panel>
        <v-expansion-panel-header>Entrega Domiciliar</v-expansion-panel-header>
        <v-expansion-panel-content
          style="text-align: center; display: flex; flex-direction: column"
        >
          <p class="subtxt">
            Para a entrega domicilar, nos contate por um dos meios
            disponibilazados na aba "Contato Comercial" e nós informe o título
            desejado, Após isso forneça seu endereço e nome, a entrega é feita
            de um a dois dias.
          </p>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#contato {
  margin-top: 35px;
  margin-right: 12%;
  margin-left: 12%;
}
#mapa {
  border: 0;
  border-radius: 20px;
}
.titletxt {
  font-family: "Oswald", sans-serif;
  padding-left: 10px;
  font-size: 28pt;
  border-left: solid 5px;
  border-left-color: #ff8331;
}
.subtxt {
  font-family: "Noto Sans", sans-serif;
  font-size: 15pt;
}
@media (max-width: 720px) {
  #mapa {
    width: 95%;
    height: 350px;
  }
  .subtxt {
    font-size: 14pt;
  }
}
</style>