<template>

  <div class="row">
    <h1>
                Diário de Laboratório
        </h1>
        <h4> Postagens sobre o dia a dia no laboratória em linguagem acessível para a comunidade. </h4>
    <div >
      <h4 slot="header">Autor: Mariana Zagatti </h4>
      <h4 slot="header">E-mail: marizagatti@ufscar.br </h4>
      <h4 slot="header">Data: 21/09/2019 </h4>

      <card>
          <span>[ ---------      Inserir texto com até 1500 caracteres    --------- ]
          </span>
      </card>
      <card>
          <span>[ ---------      Inserir vídeo com até 1m30seg    --------- ]
          </span>
      </card>
    </div>

    
    
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
