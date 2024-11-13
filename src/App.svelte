<script>
  // Array para guardar la data de cada slide
  const slides = [
    "Texto slide 1. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 2. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 3. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 4. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 5. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 6. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 7. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 8. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 9. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 10. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 11. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 12. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 13. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 14. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 15. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 16. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 17. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 18. Fusce quis augue et tortor interdum bibendum. Nam dolor elit",
    "Texto slide 19. Fusce quis augue et tortor interdum bibendum. Nam dolor elit"
  ];

  // Función para inicializar el componente de Flourish y tomar el script que nos permite hacer el scrolly gratis!
  import { onMount } from 'svelte';

  onMount(() => {
    const script = document.createElement('script');
    script.src = "https://cdn.flourish.rocks/flourish-scrolly-v3.1.0.min.js";
    script.type = "text/javascript";
    script.onload = () => initFlourishScrolly();
    document.body.appendChild(script);
  });
</script>

<section id="header">
  <img src="./public/images/worldcuplogo.png" alt="World Cup Logo" class="logo">
  <h1 id="main_title">
    Uno por uno, quiénes son los jugadores con más chances de jugar en el Mundial
  </h1>
</section>

<div class="texto_container">
  <p class="texto_parrafo">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget mi eu nulla porta fringilla. Curabitur quis tincidunt purus. Duis nec neque et augue dictum blandit a eget neque. Phasellus tempor, metus et finibus pretium, eros est sagittis orci, vitae pellentesque nisl lectus et velit. Praesent fringilla mauris vitae magna sollicitudin, sit amet tincidunt dolor facilisis. Fusce quis augue et tortor interdum bibendum. Nam dolor elit, posuere nec tortor non, molestie congue justo. Praesent nisl arcu, consectetur sed hendrerit eget, interdum ac nisi. Vestibulum tempor mattis purus. Aliquam tempus neque sed velit convallis tempor. Cras sodales nunc lorem. Nulla pharetra malesuada consequat. Nulla elementum odio non mauris mollis suscipit. Praesent consectetur nunc eget ex varius blandit. Sed id facilisis tellus.
  </p>
  <p class="texto_parrafo">
    Fusce congue eget eros vel ornare. Aenean non interdum tellus, nec dignissim diam. Mauris nisi nisl, vulputate nec commodo in, aliquet in enim. Etiam fringilla sapien quis quam faucibus, in consectetur tortor finibus. Nunc ultrices congue ipsum vel aliquet. Mauris molestie tempor finibus. Praesent mattis ac elit sed pulvinar. Aliquam augue elit, posuere ac tellus et, dignissim pharetra mi. Aenean auctor rhoncus ex eu ornare. Quisque bibendum felis at dapibus malesuada. Sed nec turpis consequat orci ornare commodo quis quis dolor. Nullam tincidunt id lectus a tristique. Praesent ultrices ipsum eget sem euismod sagittis. Morbi quis pharetra neque. Donec id est eget nunc scelerisque accumsan.
  </p>
</div>

<div class="texto_container">
  <h2 class="subtitulo">Los posibles elegidos de Scaloni</h2>
</div>

<!-- Contenedor de la story de flourish (scrolly)-->
<div id="my-wrapper">
  <div class="flourish-embed" data-src="story/2041907" data-url="https://flo.uri.sh/story/2041907/embed" data-height="100vh">
    <script src="https://public.flourish.studio/resources/embed.js"></script>
  </div>

  <!-- Iteramos sobre las distintas slides del componente de Flourish -->
  {#each slides as slide, index}
    <p>
      {slide}
      <a href={"#story/2041907/slide-" + (index + 1)}></a>
    </p>
  {/each}
</div>

<div class="texto_container">
  <p class="texto_parrafo">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget mi eu nulla porta fringilla. Curabitur quis tincidunt purus. Duis nec neque et augue dictum blandit a eget neque. Phasellus tempor, metus et finibus pretium, eros est sagittis orci, vitae pellentesque nisl lectus et velit. Praesent fringilla mauris vitae magna sollicitudin, sit amet tincidunt dolor facilisis. Fusce quis augue et tortor interdum bibendum. Nam dolor elit, posuere nec tortor non, molestie congue justo. Praesent nisl arcu, consectetur sed hendrerit eget, interdum ac nisi. Vestibulum tempor mattis purus. Aliquam tempus neque sed velit convallis tempor. Cras sodales nunc lorem. Nulla pharetra malesuada consequat. Nulla elementum odio non mauris mollis suscipit. Praesent consectetur nunc eget ex varius blandit. Sed id facilisis tellus.
  </p>
  <p class="texto_parrafo">
    Fusce congue eget eros vel ornare. Aenean non interdum tellus, nec dignissim diam. Mauris nisi nisl, vulputate nec commodo in, aliquet in enim. Etiam fringilla sapien quis quam faucibus, in consectetur tortor finibus. Nunc ultrices congue ipsum vel aliquet. Mauris molestie tempor finibus. Praesent mattis ac elit sed pulvinar. Aliquam augue elit, posuere ac tellus et, dignissim pharetra mi. Aenean auctor rhoncus ex eu ornare. Quisque bibendum felis at dapibus malesuada. Sed nec turpis consequat orci ornare commodo quis quis dolor. Nullam tincidunt id lectus a tristique. Praesent ultrices ipsum eget sem euismod sagittis. Morbi quis pharetra neque. Donec id est eget nunc scelerisque accumsan.
  </p>
</div>



<style>
html {
  font-family: Inter, sans-serif;
  line-height: 1.5;
  font-weight: 400;
}

a {
  font-weight: 500;
  color: #646cff;
  text-decoration: inherit;
}
a:hover {
  color: #535bf2;
}

body {
  margin: 0;
  min-width: 320px;
  min-height: 100vh;
}

#my-wrapper {
  margin: auto;
  max-width: 1280px;
}

#header {
  max-width: 800px;
  text-align: center;
  margin: 50px auto;
}
#main_title {
  font-size: 3em;
  line-height: 1.1;
}

.volanta {
  display: inline-block;
  padding: 5px 10px;
  background-color: black;
  color: white;
  margin-bottom: 10px;
}
.subtitulo {
  font-size: 1.5em;
  text-align: center;
}
#bajada {
  margin: 40px auto;
}
.texto_container {
  max-width: 700px;
  padding: 0 20px;
  margin: auto;
  margin-bottom: 100px;
  text-align: left;
}
.texto_parrafo {
  margin: 50px auto;
}

.fl-scrolly-step {
  background-color: rgba(0, 0, 0, 0.7) !important;
  color: white !important;
  max-width: 400px !important;
}

footer {
  margin-top: 100px;
  padding: 60px;
  background-color: #f2f2f2;
  text-align: center;
}

.footer_container {
  display: flex;
  justify-content: space-between;
  max-width: 800px;
  margin: auto;
}

.logo {
  max-width: 100px; 
  height: auto;
}
</style>