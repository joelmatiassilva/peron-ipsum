<template>
  <div id="app">
    <header class="header">
      <h1 class="title">PERON IPSUM</h1>
      <p class="subtitle">Ahora podés tener tu lorem ipsum peronista</p>
    </header>
    <content class="content">
      <div class="peron-img"><button class="button" v-on:click="generar(lorem)">GENERAR</button></div>
      <div class="lorem-container"></div>
    </content>

    <footer class="footer">
        <p class="design">Designed (lol) and developed by <a href="http://www.github.com/camila-ng">Camila González</a></p>
    </footer>
  </div>
</template>

<script>
import './assets/style.css'

export default {
  name: 'App',

  data() {
    return {
      lorem: ['El Justicialismo ha dejado de ser la causa de un hombre para ser la causa del pueblo, y por ella sí valdría la pena darlo todo, incluso la vida','El Justicialismo necesita apóstoles y para ser apóstol hay que estar dispuesto a ser héroe, y solamente los fanáticos de amor por una causa son capaces de morir por un ideal','El Justicialismo ha dejado de ser la causa de un hombre para ser la causa del pueblo, y por ella sí valdría la pena darlo todo, incluso la vida','Gobernar es fácil, lo difícil es conducir','La verdadera democracia es aquella donde el gobierno hace lo que el pueblo quiere y defiende un solo interés: el del pueblo','Yo llevo en mis oídos la más maravillosa música, que, para mí, es la palabra del pueblo argentino','Quien me quiera seguir, que me siga y quien me quiera acompañar, que me acompañe','Para conducir a un pueblo la primera condición es que uno haya salido del pueblo, que sienta y piense como el pueblo. Quien se dedica a la conducción debe ser profundamente humanista: el conductor siempre trabaja para los demás, jámas para él','No hay peor cosa que un bruto con inquietudes','La única verdad es la realidad']
    }
  },
  components: {

  },
  methods: {
    generar: (lorem) => { 
      let content = document.querySelector('.lorem-container');
      var newLorem = [];
      for (var i = 0; i < 10; i++) {
        var randomLorem = lorem[Math.floor(Math.random() * lorem.length)];
        newLorem.push(randomLorem);

        content.style.backgroundColor = '#84a9ac';
        content.innerText = newLorem.join(' ')
       
      }
    }
  }
}
</script>