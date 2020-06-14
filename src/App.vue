<template>
  <section class="upper">
    <h1>Code <span>in the</span> Dark</h1>
    <img src="/images/cool.png" />
  </section>

  <section class="content">
    <h3>Que es</h3>
    <p>
      Code in the Dark - es una competencia de front-end (HTML y CSS), originada
      en Tictail, donde cada participante compite para implementar el diseño de
      un sitio web dado solo un screenshot.
      <br />El truco está en que no se puede previsualizar lo que el
      desarrollador hace durante la implementación, ni se pueden usar
      herramientas de medida. <br />El ganador será decidido por la audiencia!
    </p>
  </section>

  <section class="content">
    <h3>Organiza</h3>
    <div class="hosts">
      <div class="hosts__host">
        <img src="/images/pp.jpg" alt="IOSamuel" />
        <h4>Samuel Burbano</h4>
        <span>Host</span>
        <ul class="icons">
          <li>
            <a
              href="https://www.twitter.com/iosamuel"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.youtube.com/channel/UCTvtM8ZisSrp9rii77D85Zw"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-youtube"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.twitch.tv/iosamuel"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitch"></i>
            </a>
          </li>
        </ul>
      </div>

      <div class="hosts__host">
        <img src="/images/nani.jpg" alt="Daniela Quiroga" />
        <h4 data-egg="Futura esposa de @IOSamuel">Daniela Quiroga</h4>
        <span>Co-Host</span>
        <ul class="icons">
          <li>
            <a
              href="https://twitter.com/nani_kika"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.youtube.com/nanikika"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-youtube"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.twitch.tv/nani_kika"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitch"></i>
            </a>
          </li>
        </ul>
      </div>

      <div class="hosts__host">
        <img src="/images/leonidas.jpg" alt="LeonidasEsteban" />
        <h4>Leonidas Esteban</h4>
        <span>Co-Host</span>
        <ul class="icons">
          <li>
            <a
              href="https://twitter.com/LeonidasEsteban"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.youtube.com/leonidasesteban"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-youtube"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.twitch.tv/leonidasesteban"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitch"></i>
            </a>
          </li>
        </ul>
      </div>

      <div class="hosts__host">
        <img src="/images/gndx.jpg" alt="Oscar Barajas" />
        <h4>Oscar Barajas</h4>
        <span>Co-Host</span>
        <ul class="icons">
          <li>
            <a
              href="https://twitter.com/gndx"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.youtube.com/c/oscarbarajas"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-youtube"></i>
            </a>
          </li>
          <li>
            <a
              href="https://www.twitch.tv/gndxdev"
              target="_blank"
              rel="noreferer noopener"
            >
              <i class="fab fa-twitch"></i>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>

  <section class="content">
    <img class="content__image" src="/images/iosamuel.png" alt="IOSamuel" />
    <h3>Rules</h3>
    <p>
      Sera una competencia single-elimination, lo que quiere decir que ganas o
      pierdes en cada ronda. Cada ronda seran grupos de 4 programadores y solo 1
      avanza.
    </p>

    <ul>
      <li><h4>Eliminatorias</h4></li>
      <li>15 min</li>
      <li>HTML/CSS</li>
      <li>No previews</li>
      <li>Single-elimination</li>
    </ul>

    <ul>
      <li><h4>Finales</h4></li>
      <li>30 min</li>
      <li>HTML/CSS</li>
      <li>No previews</li>
      <li>1 Campeon</li>
    </ul>
  </section>

  <section class="content">
    <h3>Rewards</h3>
    <p>
      El ganador de la competencia se llevara una Camiseta con la copa de Code
      in the Dark (by IOSamuel), una subscripcion a Platzi por 3 meses y un pack
      de 10 stickers.
    </p>

    <ul>
      <li><img src="/images/vic-pengu.png" alt="Victory" /></li>
      <li><img src="/images/platzi.jpg" alt="Platzi" /></li>
    </ul>
  </section>

  <section class="content">
    <h3>Players</h3>
    <p>
      Estos son los competidores! <br />Esta lista se ira actualizando a medida
      que avance la competencia.
    </p>

    <div class="palet">
      <p><span class="color--won">Gano</span></p>
      <p><span class="color--lost">Perdio</span></p>
      <p><span class="color--playing">Participando</span></p>
    </div>
    <div class="players">
      <span
        v-for="player in players"
        :key="player.name"
        :class="{ won: player.won, playing: player.playing }"
      >
        {{
          player.name
            .split(" ")
            .slice(0, 1)
            .join(" ")
        }}
        <br />
        {{
          player.name
            .split(" ")
            .slice(1, 2)
            .join(" ")
        }}
      </span>
    </div>

    <p class="status">
      El registro está
      <span :class="{ open, closed: !open }">
        {{ open ? "abierto" : "cerrado" }}
      </span>
      <template v-if="open">
        :
        <a
          href="https://docs.google.com/forms/d/e/1FAIpQLScsWgdo1x5wPKYnUMSBokZBom4dZybDl5T8HtEv_HfANfj5SQ/viewform?usp=sf_link"
        >
          Click Aquí
        </a>
      </template>
    </p>
  </section>

  <section class="content when">
    <h3>Cuando</h3>
    <p>
      Empezaremos con la fase Eliminatoria los siguientes días:
    </p>

    <br />

    <p>
      <span class="date">
        <i class="fas fa-calendar-alt"></i> Sábado 13/06/2020
      </span>
      <br />
      <span class="date">
        <i class="fas fa-clock"></i> 3pm COT - UTC/GMT-5
      </span>
    </p>

    <br />
    <hr />
    <br />

    <p>
      <span class="date">
        <i class="fas fa-calendar-alt"></i> Domingo 14/06/2020
      </span>
      <br />
      <span class="date">
        <i class="fas fa-clock"></i> 3pm COT - UTC/GMT-5
      </span>
    </p>

    <br />

    <p>
      Puedes estar pendiente en los canales de transmision.
    </p>

    <ul class="icons">
      <li>
        <a
          href="https://www.twitter.com/iosamuel"
          target="_blank"
          rel="noreferer noopener"
        >
          <i class="fab fa-twitter"></i>
        </a>
      </li>
      <li>
        <a
          href="https://www.youtube.com/channel/UCTvtM8ZisSrp9rii77D85Zw"
          target="_blank"
          rel="noreferer noopener"
        >
          <i class="fab fa-youtube"></i>
        </a>
      </li>
      <li>
        <a
          href="https://www.twitch.tv/iosamuel"
          target="_blank"
          rel="noreferer noopener"
        >
          <i class="fab fa-twitch"></i>
        </a>
      </li>
    </ul>
  </section>

  <div class="iosamuel">
    <a href="https://iosamuel.dev/">
      <img src="/images/iosamuel-logo.png" alt="IOSamuel" />
    </a>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      players: [
        { name: "Yan Arlex Vallejo" },
        { name: "Juan Martinez" },
        { name: "Jhon Garcia", won: true },
        { name: "Joan Serna" },
        { name: "William Velazquez" },
        { name: "Alejandro Villagran" },
        { name: "Nicolas Arias" },
        { name: "Horacio Herrera", won: true },
        { name: "Erifranck Nuñez" },
        { name: "Efrén Martinez", won: true },
        { name: "Juan López" },
        { name: "José Barrios" },
        { name: "Jorge Ivan" },
        { name: "Diego Torres" },
        { name: "Kath Montalvo" },
        { name: "Fiorella Effio", won: true },
        { name: "Jerson Alexander", playing: true },
        { name: "Andrés Felipe", playing: true },
        { name: "Sergio Estrella", playing: true },
        { name: "Diego Aguilera", playing: true }
      ],
      open: false
    };
  }
};
</script>

<style lang="scss" src="./styles/app.scss"></style>
