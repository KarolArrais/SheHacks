<template>

  <div class="row">
    <h1>
          BUSCA DE PARCERIA
        </h1>
    <div >
      <h4 slot="header">OFERTA DE EXPERTISE:</h4>
      <card>
        <base-alert type="danger">
          <span><b>Breve descritivo: </b> Estamos disponíveis para colaborar no desenvolvimento de jogos educativos e 
            preparação de equipes para atuação no mesmo campo.
          </span>
          <br>
          <span><b>É possível fazer colaboração à distância (S/N)? </b> Sim
          </span>
          <br>
          <span><b>Pesquisador responsável:</b> Profa. Dra. Joice Lee Otsuka - email@exemplo.br.
          </span>
          <br>
          <span><b>Período de colaboração:</b> de MM/ANO até MM/ANO.
          </span>
          <br>
          <span><b>Caso tenha interesse, preencha abaixo:</b>
          </span>
        </base-alert>
        <span>[Link para CV Lattes] <br> 
[Nome sobrenome] <br> 
[E-mail]
          </span>
      </card>
    </div>

Período de colaboração: de MM/ANO até MM/ANO. 
Caso tenha interesse, preencha abaixo: 
Link para CV Lattes. 
Nome sobrenome. 
E-mail.


    
    
  </div>
</template>
<script>
  import NotificationTemplate from './Notifications/NotificationTemplate';
  import { BaseAlert } from '@/components';

  export default {
    components: {
      BaseAlert
    },
    data() {
      return {
        type: ["", "info", "success", "warning", "danger"],
        notifications: {
          topCenter: false
        }
      };
    },
    methods: {
      notifyVue(verticalAlign, horizontalAlign) {
        const color = Math.floor(Math.random() * 4 + 1);
        this.$notify({
          component: NotificationTemplate,
          icon: "tim-icons icon-bell-55",
          horizontalAlign: horizontalAlign,
          verticalAlign: verticalAlign,
          type: this.type[color],
          timeout: 0
        });
      }
    }
  };
</script>
<style>
</style>
