<template>

  <div class="row">
    <h1>
          Publicações dos membros
        </h1>
    <div >
      <h4 slot="header">2019:</h4>
      <card>
        <base-alert type="danger">
          <span>1. VALÉRIO NETO, L.; FONTOURA JUNIOR, P. H. F.; BORDINI, R. A.; OTSUKA, J. L. Design 
            and Implementation of an Educational Game Considering Issues for Visual Impaired People Inclusion. 
            In: 18th IEEE International Conference on Advanced Learning Technologies (ICALT 2019), 2019.
          </span>
        </base-alert>
      </card>
    </div>

    <h4 slot="header">2018:</h4>
    <div >
      <card>
        <base-alert type="danger">
          <span>1. MORANO, T.; OTSUKA, J. L.; FONTOURA JUNIOR, P. H. F.Design and development of a memory game 
            solution for players with and without visual impairment In: Simpósio Brasileiro de Informática na 
            Educação, 2018, Fortaleza. Proceedings of the XXIX Brazilian Symposium on Computers in Education (SBIE), 2018.</span>
        </base-alert>
        <base-alert type="danger">
          <span>2. CARDOSO, F. C.; OTSUKA, J. L.Visualização da Informação na análise de dados coletados a partir de jogos: um 
            Mapeamento Sistemático In: Simpósio Brasileiro de Jogos e Entretenimento Digital, 2018, Foz do Iguaçu. Anais do SBGames
           2018 (Proceedings of SBGames 2018),2018.
          </span>
        </base-alert>
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
