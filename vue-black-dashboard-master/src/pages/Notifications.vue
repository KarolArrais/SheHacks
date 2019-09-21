<template>

  <div class="row">
    <h1>
          Serviços de extensão do LOA
        </h1>
    <div >
      <card>
        <h4 slot="header">Serviço comunitário:</h4>
        <base-alert type="info">
          <span>- Parcerias com escolas públicas para ensino de programação básica</span>
        </base-alert>
        <base-alert type="info">
          <span>- Jogos e brincadeiras direcionados para inclusão de alunos com deficiências visuais.</span>
        </base-alert>
      </card>
    </div>

    <div >
      <card>
        <h4 slot="header">Projetos de Extensão:</h4>
        <base-alert type="info">
          <span>- GT-REMAR: facilitação e ampliação na construção e o reuso de recursos educacionais abertos, 
            por meio da plataforma web (REMAR), que oferece ferramentas para compartilhamento e a customização 
            de jogos educacionais abertos, para diferentes plataformas, além do compartilhamento com grupos e o
             acompanhamento de progresso de participantes nos jogos.</span>
        </base-alert>
        <base-alert type="info">
          <span>- PROEXT: desenvolvido o Programa de Formação e Desenvolvimento de Recursos Educacionais Abertos 
            (Edital PROEXT 2014/MEC-SESu), que tem como foco o desenvolvimento de recursos educacionais abertos, 
            em especial jogos educacionais para cursos técnicos e de graduação presenciais e a distância nas áreas 
            de Química, Enfermagem e Música. </span>
        </base-alert>
      </card>
    </div>
    <!--
    <div class="col-md-12">
      <card>
        <div class="places-buttons">
          <div class="row">
            <div class="col-md-6 ml-auto mr-auto text-center">
              <h4 class="card-title">
                Notifications Places
                <p class="category">Click to view notifications</p>
              </h4>
            </div>
          </div>
          <div class="row">
            <div class="col-lg-8 ml-auto mr-auto">
              <div class="row">
                <div class="col-md-4">
                  <base-button type="primary" block @click="notifyVue('top', 'left')">Top Left</base-button>
                </div>
                <div class="col-md-4">
                  <base-button type="primary" block @click="notifyVue('top', 'center')">Top Center</base-button>
                </div>
                <div class="col-md-4">
                  <base-button type="primary" block @click="notifyVue('top', 'right')">Top Right</base-button>
                </div>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-lg-8 ml-auto mr-auto">
              <div class="row">
                <div class="col-md-4">
                  <base-button type="primary" block @click="notifyVue('bottom', 'left')">Bottom Left</base-button>
                </div>
                <div class="col-md-4">
                  <base-button type="primary" block @click="notifyVue('bottom', 'center')">Bottom Center</base-button>
                </div>
                <div class="col-md-4">
                  <base-button type="primary" block @click="notifyVue('bottom', 'right')">Bottom Right</base-button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </card>
    </div> -->
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
