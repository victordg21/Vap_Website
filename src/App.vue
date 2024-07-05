<script>
  export default {
    data() {
    return {
      countdown: '',
      interval: null,
    }
  },
  methods: {
    scrollToSection() {
      const section = document.getElementById('sales');
      if (section) {
        window.scrollTo({
          top: section.offsetTop,
          behavior: 'smooth'
        });
      }
    },
    goToLink() {
      window.location.href = 'https://pay.kiwify.com.br/VEpZ3T9';
    },
    updateCountdown() {
      const now = new Date();
      let nextSunday = new Date();
      nextSunday.setDate(now.getDate() + (7 - now.getDay()) % 7);
      nextSunday.setHours(0, 0, 0, 0);

      const timeDifference = nextSunday - now;

      if (timeDifference > 0) {
        const days = Math.floor(timeDifference / (1000 * 60 * 60 * 24));
        const hours = Math.floor((timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((timeDifference % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((timeDifference % (1000 * 60)) / 1000);
        
        this.countdown = `${days.toString().padStart(2, '0')}:${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
      } else {
        this.countdown = '00:00:00:00';
      }
    },
  },
  mounted() {
    this.updateCountdown();
    this.interval = setInterval(this.updateCountdown, 1000); // Atualiza a cada segundo
  },
  beforeDestroy() {
    clearInterval(this.interval);
  },
  }
</script>

<template>
  <header class="centralize">
    <img class="header-image" src="./assets/clock.png" alt="">
      <h1 class="text-header span-yellow">Essa oferta terminará em {{countdown}}</h1>
  </header>
  <section class="Section1 padding-section centralize">
    <div class="container">
      <h2 class="font-bold font-size-bigger">O que você precisa para <span class="span-yellow">superar a procrastinação, a ansiedade e a inconstância </span>nos estudos para o vestibular é <span class="span-yellow">dominar os 4 princípios da Alta Performance</span></h2>
      <h3 class="span-yellow font-size-tablet">Te convido a assistir o vídeo abaixo, onde eu vou te mostrar o verdadeiro mapa da aprovação e tudo que é necessário para você extrair o máximo dos seus estudos.</h3>
      <div class="centralize">
        <iframe class="video-vap" src="https://www.youtube.com/embed/JxvDjBeZnZw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <button @click="scrollToSection" class="button">Quero garantir meu acesso!</button>
    </div>
  </section>
  <section class="Section2-New padding-section centralize">
    <div class="container">
      <div class="first-informations">
        <h2 class="first-informations_text font-card_first-informations_text">Se você acha que “só estudar é suficiente”... <span class="font-bold span-yellow">Veja o resultado de quem decidiu dominar os princípios e aplicar o VAP na sua preparação</span>:</h2>
        <p class="font-large second-informations_text"><span class="span-yellow font-size-vest font-bold">+200 vestibulandos</span> <br>atendidos no último ano</p>
      </div>
      <div class="grid-testimonial">
        <div class="card-white">
          <div class="card-up-information">
            <img class="card-testimonial_image" src="./assets/depoimento-1.jpeg" alt="">
            <h3 class="card-name-color">Yasmin S. Cruz</h3>
          </div>
          <p class="">Enquanto li os conteúdos, consegui ver muito da minha realidade nos anos de cursinho, a forma errada de lidar com algumas emoções e a falta de práticas que poderiam ter melhorado muito meu rendimento. Eu pude sentir de novo uma pontinha de esperança na minha aprovação.</p>
        </div>
        <div class="card-white">
          <div class="card-up-information">
            <img class="card-testimonial_image" src="./assets/depoimento-2.jpeg" alt="">
            <h3 class="card-name-color">M. Clara Campos</h3>
          </div>
          <p class="">O VAP foi como um tapa na cara e um abraço ao mesmo tempo. Tenho certeza que aplicar todas as técnicas e os ensinamentos no meu dia a dia vai me dar não só qualidade nos estudos mas também na vida.</p>
        </div>
        <div class="card-white">
          <div class="card-up-information">
            <img class="card-testimonial_image" src="./assets/depoimento-3.jpeg" alt="">
            <h3 class="card-name-color">João Victor Novais</h3>
          </div>
          <p class="">Se eu tivesse o VAP antes meu ano teria sido muito mais fácil. Os conteúdos me ajudaram a compreender melhor o momento que estou passando como vestibulando. É quase uma terapia em textos!</p>
        </div>
        <div class="card-white">
          <div class="card-up-information">
            <img class="card-testimonial_image" src="./assets/depoimento-4.jpeg" alt="">
            <h3 class="card-name-color">Marcela Toscano</h3>
          </div>
          <p class="">Quando entrei no VAP senti que tinha “saído de uma caverna”. Impressionante como ninguém tinha me ensinado essas coisas antes. Hoje posso dizer que estou mais segura e confiante com minha preparação.</p>
        </div>
      </div>
    </div>

  </section>
  <section class="Section2 padding-section centralize">
    <div class="container">
      <h2 class="font-size-bigger font-bold">As 4 trilhas do VAP</h2>
      <div class="grid-informations">
        <div class="card">
          <div class="card-blue">
            <img class="image_card-blue" src="./assets/Força emocional.png" alt="">
          </div>
          <div class="card-gray">
            <p class="font-card-start">Lide com a ansiedade, os sentimentos ruins e as pressões internas e extemas.</p>
            <p class="font-bold align-end font-card-end">Força Emocional</p>
          </div>
        </div>
        <div class="card">
          <div class="card-blue">
            <img class="image_card-blue" src="./assets/Amadurecimento e motivação.png" alt="">
          </div>
          <div class="card-gray">
            <p class="font-card-start">Choques de realidade. Doses de ânimo. Tudo o que vooe precisa para virar gente e dar o máximo nos estudos.</p>
            <p class="font-bold align-end font-card-end">Amadurecimento e Motivação</p>
          </div>
        </div>
        <div class="card">
          <div class="card-blue">
            <img class="image_card-blue" src="./assets/Neurociência da aprendizagem.png" alt="">
          </div>
          <div class="card-gray">
            <p class="font-card-start">Estude conforme evidências científicas. Maximize seu aprendizado e alcance a aprovação.</p>
            <p class="font-bold align-end font-card-end">Neurociência da Aprendizagem</p>
          </div>
        </div>
        <div class="card">
          <div class="card-blue">
            <img class="image_card-blue" src="./assets/Produtividade e gestão de tempo.png" alt="">
          </div>
          <div class="card-gray">
            <p class="font-card-start">Domine seu tempo, pare de procrastinar e se torne produtivo de verdade.</p>
            <p class="font-bold align-end font-card-end">Gestão de Tempo</p>
          </div>
        </div>
      </div>
      <button @click="scrollToSection" class="button">Quero garantir meu acesso!</button>
      <div class="items-section">
        <div class="items-grid">
          <img class="grid-photo-mockup" src="./assets/Mockup 1.png" alt="">
          <div class="items-text">
            <h3 class="font-large">O que você <span class="span-yellow">vai encontrar?</span></h3>
            <p class="padding-bottom" ><span class="bullet">•</span> Conteúdo em texto, rápido e prático.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Organizado no Notion.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Técnicas de controle emocional.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Técnicas de antiprocrastinação.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Métodos de estudo baseados em neurociência.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Doses de ânimo e motivação.</p>
          </div>
          <img class="grid-photo-mockup" src="./assets/Mockup 2.png" alt="">
          <div class="items-text">
            <h3 class="font-large">O que você <span class="span-red">não vai encontrar?</span></h3>
            <p class="padding-bottom" ><span class="bullet">•</span> Aulas chatas e cheias de enrolação.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Mais um cronograma inútil.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Conteúdos desnecessários.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Templates que você nunca usa.</p>
          </div>
          <img class="grid-photo-mockup" src="./assets/Mockup 3.png" alt="">
          <div class="items-text">
            <h3 class="font-large">Para quem <span class="span-yellow">é?</span></h3>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer ser aprovado sem perder a cabeça.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer dominar o medo e a ansiedade.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer ser constante.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem não tem tempo para ver aulas enormes.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer ser produtivo de verdade.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer se tornar uma pessoa melhor.</p>
          </div>
          <img class="grid-photo-mockup" src="./assets/Mockup 4.png" alt="">
          <div class="items-text">
            <h3 class="font-large">Para quem <span class="span-red">não é?</span></h3>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem acredita que "é só estudar que passa".</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer continuar estagnado.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer passar anos estudando sem resultado.</p>
            <p class="padding-bottom" ><span class="bullet">•</span> Quem quer ser refém das emoções.</p>
          </div>
        </div>
        <div class="centralize">
          <button @click="scrollToSection" class="button">Quero garantir meu acesso!</button>
        </div>
      </div>
    </div>
  </section>
  <section class="Section4-New padding-section centralize">
    <div class="container">
      <h2 class="font-size-bigger">Se você está em ano de vestibular, sentindo-se  <span class="span-yellow">inseguro, estagnado e improdutivo</span> ou enfrenta problemas com <span class="span-yellow"a>ansiedade e desânimo…</span></h2>
      <p class="font-size-medium">Eu vou te entregar um ambiente de desenvolvimento para fazer seu estudo render de verdade. <span class="span-yellow">Basta você pôr em prática para:</span></p>
      <div class="points-arrow top">
        <svg xmlns="http://www.w3.org/2000/svg" width="auto" height="auto" fill="#E5B30C" class="bi bi-arrow-right" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8"/>
        </svg>
        <p class="points-arrow_text">Vencer a procrastinação, gerenciar o próprio tempo e conseguir estudar com constância e equilíbrio;</p>
      </div>
      <div class="points-arrow">
        <svg xmlns="http://www.w3.org/2000/svg" width="auto" height="auto" fill="#E5B30C" class="bi bi-arrow-right" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8"/>
        </svg>
        <p class="points-arrow_text">Melhorar drasticamente seu rendimento nos estudos, por meio de métodos e técnicas neurocientíficas;</p>
      </div>
      <div class="points-arrow">
        <svg xmlns="http://www.w3.org/2000/svg" width="auto" height="auto" fill="#E5B30C" class="bi bi-arrow-right" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8"/>
        </svg>
        <p class="points-arrow_text">Superar a ansiedade e a insegurança e alcançar seu ápice de produtividade, usando as emoções ao seu favor.</p>
      </div>
      <div class="points-arrow">
        <svg xmlns="http://www.w3.org/2000/svg" width="auto" height="auto" fill="#E5B30C" class="bi bi-arrow-right" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8"/>
        </svg>
        <p class="points-arrow_text">Retomar a sua confiança na aprovação e estudar com ânimo e motivação.</p>
      </div>
      <p class="font-size-medium top">Cada trilha no VAP propõe um caminho prático, rápido e seguro para você alcançar a verdadeira Alta Performance nos estudos e conquistar a aprovação, sem enrolação e sem conteúdos desnecessários.</p>
      <button @click="scrollToSection" class="button">Quero garantir meu acesso ao VAP!</button>
    </div>
  </section>
  <section id="sales"class="Section3 padding-section centralize">
    <div class="container">
      <h3>COMPRE AGORA COM <span class="span-red">MAIS DE 80% DE DESCONTO</span></h3>
      <h2 class="font-bold font-size-bigger-2">Aproveite o <span class="span-yellow">preço exclusivo</span> de lançamento</h2>
      <img class="price-image" src="./assets/Preço.png" alt="">
      <div>
        <button @click="goToLink" class="button">Quero garantir meu acesso!</button>
      </div>
      <p>Compre na oferta de lançamento e <span class="span-yellow">garanta todas as atualizações até o Enem.</span></p>
    </div>
  </section>
  <section class="Section4 padding-section centralize">
    <div class="display-grid-photo container">
      <img class="grid-photo" src="./assets/Foto1.png" alt="">
      <div class="grid-text">
        <h2 class="h2-title font-bold font-size-bigger">Quem sou eu?</h2>
        <p class="font-size-medium">Davi Belo de Carvalho</p><br><br>
        <p class="font-size-medium">Terapeuta no maior cursinho pré-vestibular do seu estado.</p><br><br>
        <p class="font-size-medium">Davi Belo já atendeu mais de 200 vestibulando e gerenciou intervenções em grupo, palestras e momentos de espiritualidade com uma série de estudantes.</p><br><br>
        <p class="font-size-medium">Depois de ter escutado e ajudado muitos alunos e pacientes vestibulandos, decidiu condensar as principais necessidades e problemas que percebeu e solucionou no VAP.</p>
      </div>
    </div>
  </section>
</template>

<style scoped>

*{
  font-family: Helvetica, sans-serif;
  font-weight: 500;
}

.font-bold{
  font-weight: bold;
}

.span-yellow{
  color: #E5B30C;
}

.span-red{
  color:#B53535;
}

.images-section-1{
  width: 30px;
  padding-right: 20px;
  padding-bottom: 10px;
}

.font-large{
  font-size: 32px;
  margin: 0;
  padding-bottom: 15px;
}

.font-size-bigger{
  font-size: 44px;
}

.font-size-vest{
  font-size: 44px;
}

.font-size-bigger-2{
  font-size: 50px;
}

.bi-arrow-right{
  height: 20px;
  width: 20px;
}

.bi-arrow-right{
  width: 20px;
  height: 20px
}

.font-size-medium{
  font-size: 24px;
}

header{
  background-color: #B53535;
}

.header-image{
  width: 40px;
  padding: 10px 20px 10px 0;
}

.first-informations{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 100px;
}

.first-informations_text{
  text-align: left;
  margin: auto;
}

.second-informations_text{
  text-align: right;
}

.container {
  max-width: 1200px;
  width: 100%;
}

.video-vap{
  width: 800px;
  height: 450px;
}

.centralize{
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.Section1, .Section3{
  background-color: #101010;
  color: white;
}

.Section4-New{
  background-color: #fff;
  color: black
}

.Section2-New{
  background-color: #B53535;
  color: #eee;
}

.price-image{
  width: 350px;
}

.padding-bottom{
  padding-bottom: 5px;
}

.bullet{
  font-size: 10px;
}

p, .align-end{
  margin: 0;
}

.points-arrow{
  display: flex;
  gap: 20px;
  padding-bottom: 16px;
}

.points-arrow_text{
  font-weight: 400;
  font-size: 20px;
  text-align: left;
}

.top{
  padding-top: 60px;
}

.font-card_first-informations_text{
  font-weight: 400;
  font-size: 17px;

}

.font-card-start{
  font-weight: 400;
  font-size: medium;
}

.font-card-end{
  font-weight: 500;
  font-size: 18px;
}

button{
  margin: 2rem;
  padding: 10px 25px;
  border-radius: 20px;
  border: none;
  font-weight: 500;
  font-size: large;
  color: #101010 !important;
  background-color: #E5B30C;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.display-grid-photo{
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 2rem;
}

.grid-photo{
  width: 100%;
}

.grid-photo-mockup{
  width: 80%;
  margin: auto;
}

.grid-text{
  text-align: left;
}

.padding-section{
  padding: 2rem 0;
}

.h2-title{
  margin-top: 0;
}

.items-section{
  background-color: #eee;
  width: 90%;
  margin: 0 auto;
  border-radius: 20px;
  text-align: left;
}

.items-grid{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  padding: 2rem;
}

.items-text{
  margin: auto;
  list-style-type: disc;
}

.grid-informations{
  max-width: 800px;
  margin: 0 auto;
}

.grid-informations, .grid-testimonial{ 
  padding-top: 40px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
}

.card-testimonial_image{
  background-color: gray;
  border-radius: 50%;
  width: 12%
}

.card-up-information{
  display: flex;
  gap: 20px;
  padding-bottom: 10px;
}

.card-white{
  text-align: left;
  padding: 20px 15px;
  background-color: white;
  border-radius: 6px;
  color: rgb(74, 67, 67);
}

.card-name-color{
  color: black;
}

.card {
  position: relative; 
  height: 200px; 
}

.image_card-blue, .image-card-testimonial{
  width: 100%;
}

.card-blue {
  position: absolute;
  width: 33.3%;
  height: 100%;
  border-radius: 20px;
  left: 0;
  top: 0;
}

.font-size-tablet{
  text-transform: uppercase;
}

.card-gray {
  position: absolute;
  text-align: left;
  background-color: #eee;
  width: 66.6%;
  height: 60%;
  border-radius: 20px;
  padding: 1rem;
  top: 50%;
  left: 25%; 
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

@media (max-width: 655px) and (min-width: 435px){
  .grid-informations{
    padding-bottom: 100px;
  }

  .card{
    padding-bottom: 120px;
  }
}

@media (max-width: 1080px) and (min-width: 656px){

  .container{
    width: 90%;
  }
  .first-informations{
  display: block;
  gap: 100px;
  }
  .second-informations_text{
  text-align: center;
  padding-top: 30px;
}



.card-white{
  margin-bottom: 30px;
}

.grid-testimonial{
    display: block;
  }

  .video-vap{
    width: 600px;
    height: 350px;
  }

  .font-size-bigger{
    font-size: 30px;
  }

  .font-size-tablet{
  text-transform:none;
}
}

@media (max-width: 655px){

  .container{
    width: 90%;
  }

  .grid-informations, .grid-testimonial{
    display: block;
  }

  .card{
    margin-bottom: 20px;
  }

  .font-size-tablet{
  text-transform: none;
}


.card-testimonial_image{
  background-color: gray;
  border-radius: 50%;
  width: 20%
}

.first-informations{
  display: block;
  gap: 100px;
  }

  .second-informations_text{
  text-align: center;
  padding-top: 30px;
}

.video-vap{
    width: 300px;
    height: 180px;
  }

  .font-size-bigger{
    font-size: 20px;
  }

  .font-size-tablet{
  text-transform:none;
  font-size: 15px;
  padding: 20px 0;
}

  
.images-section-1{
  width: 25px;
  padding-right: 5px;
  padding-bottom: 10px;
}

.card-white{
  margin-bottom: 30px;
}

.text-first-section{
  font-size: 15px;
}

.header-image{
  padding: 10px 0 10px 0;
}

header{
  padding: 0 50px;
}

.display-grid-photo{
  display: block;
  gap: 2rem;
}

.grid-photo{
  width: 75%;
}

.grid-text{
  width: 70%;
  margin: 0 auto;
  padding-top: 20px;
}

.bi-arrow-right{
  width: 40px;
  margin: auto;
}


.items-grid{
  display: flex;
  flex-direction: column;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  padding: 2rem;
}


}

</style>
