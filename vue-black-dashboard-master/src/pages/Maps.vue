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
       <span> Nos últimos anos, houve um aumento de pesquisas focadas na eficácia do uso de videogames como recursos digitais educacionais que podem contribuir para o processo de aprendizagem em diferentes níveis, o que também subsidiou o desenvolvimento de jogos educacionais. No entanto, esses jogos são principalmente visuais e não acessíveis a pessoas com algum tipo de deficiência visual. Este artigo tem como objetivo descrever o design, implementação e avaliação de uma versão acessível do jogo educacional In Search of the Holy Degree, com base no EduGameAccess - um conjunto de recomendações que integra aspectos educacionais, de jogabilidade e de acessibilidade para pessoas com deficiência visual.

O número de pesquisas relacionadas à utilização de videogames como recurso educacional vem crescendo nos últimos anos porém a maioria dos jogos são visuais de modo que as pessoas com algum tipo de deficiência visual não podem utilizar. Deste modo, o presente artigo visa descrever aspectos de implementação e design de uma versão acessível do jogo educacional In Search of the Holy Degree, com base no EduGameAccess.
</span>
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
        <span>Como os jogos surgiram como uma das formas mais populares de entretenimento, eles também provaram ser bons recursos educacionais. No entanto, como essa mídia geralmente se concentra nos aspectos visuais, as pessoas com deficiência visual geralmente não conseguem utilizá-las. Assim, o objetivo deste estudo é propor uma solução de design de um jogo de memória multiplataforma que atinja pessoas com e sem deficiência visual. Para isso, são analisados ​​estudos sobre soluções de design para jogos de memória acessíveis em diferentes plataformas. É apresentada uma proposta de design, baseada nessas soluções, bem como nas diretrizes de acessibilidade e jogabilidade. Finalmente, um protótipo de baixa fidelidade é usado para testar a interação de um jogador com deficiência visual.
Os jogos surgiram como uma plataforma de entretenimento mas eles também já provaram ser bons recursos educacionais. Muitos dos jogos utilizam os aspectos visuais, isso faz com que pessoas com deficiência visual não possam jogar. Assim, o objetivo deste estudo é propor uma solução de design de um jogo de memória multiplataforma que atinja pessoas com e sem deficiência visual.
</span>
      </card>
    </div>
    <div >
      <card>
        <base-alert type="danger">
          <span>2. CARDOSO, F. C.; OTSUKA, J. L.Visualização da Informação na análise de dados coletados a partir de jogos: um 
            Mapeamento Sistemático In: Simpósio Brasileiro de Jogos e Entretenimento Digital, 2018, Foz do Iguaçu. Anais do SBGames
           2018 (Proceedings of SBGames 2018),2018.
          </span>
        </base-alert>
        <span> Este artigo apresenta um mapeamento sistemático com a intenção de identificar o estado da arte na área de Visualização da  Informação aplicada em jogos. Foram analisados neste estudo 32 trabalhos com intuito de fazer um levantamento de quais informações, gêneros de jogos e técnicas foram mais utilizadas nos trabalhos que compõem este estudo, para que seja possível analisar os dados coletados dos jogadores.
No presente trabalho foram analisados 32 trabalhos com o intuito identificar o estado da arte na área de Visualização da  Informação aplicada em jogos.
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
