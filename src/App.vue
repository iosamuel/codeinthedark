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
        <img src="/images/gndx.jpg" alt="LeonidasEsteban" />
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
              href="https://www.youtube.com/channel/UCw05fUBPwmpu-ehXFMqfdMw"
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
      pierdes en cada ronda, las Finales seran entre los 3 ultimos
      participantes.
    </p>

    <ul>
      <li><h4>Eliminatorias</h4></li>
      <li>15 min</li>
      <li>HTML/CSS</li>
      <li>No previews</li>
      <li>One champion</li>
    </ul>

    <ul>
      <li><h4>Finales</h4></li>
      <li>30 min</li>
      <li>HTML/CSS</li>
      <li>No previews</li>
      <li>One champion</li>
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

    <div class="players">
      <span
        v-for="player in players"
        :key="player.name"
        :class="{ lost: player.lost }"
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
        { name: "Yaroslay Bravo ", lost: false },
        { name: "Andres Felipe Pinchao Ramirez", lost: false },
        { name: "Laura Guzmán", lost: false },
        { name: "Joan Manuel Serna Leiton", lost: false },
        { name: "Luis Fernando Delgado Arboleda", lost: false },
        { name: "Diego Torres", lost: false },
        { name: "Kathlen Montalvo Mendoza", lost: false },
        { name: "Fiorella Effio Saldivar", lost: false },
        { name: "Jesús cruz dominguez", lost: false },
        { name: "Jorge Ivan Morales Obando", lost: false },
        { name: "Alejandro Villagran", lost: false },
        { name: "Santiago Munguía López", lost: false },
        { name: "Diego Ignacio Ruiz Poblete", lost: false },
        { name: "María Fernanda Hernández Vargas ", lost: false },
        { name: "William Eduardo Velazquez Amarra ", lost: false },
        { name: "Alfredo Martínez", lost: false },
        { name: "Andrés Corral", lost: false },
        { name: "Jhon Michael García ", lost: false },
        { name: "Pablo", lost: false },
        { name: "Juan José López lira ", lost: false },
        { name: "José Barrios ", lost: false },
        { name: "Ernesto Román ", lost: false },
        { name: "Nicolas Molina", lost: false },
        { name: "Yan Arlex Vallejo Rosas", lost: false },
        { name: "Horacio Herrera García", lost: false },
        { name: "Jorge Betancur ", lost: false },
        { name: "Efrén Martinez rodriguez", lost: false },
        { name: "Jerson Alexander Morocho Basante", lost: false },
        { name: "Juan Martinez", lost: false },
        { name: "Rubén salgado", lost: false },
        { name: "Roberto Barbosa", lost: false },
        { name: "Erifranck nuñez", lost: false }
      ],
      open: false
    };
  }
};
</script>

<style lang="scss" src="./styles/app.scss"></style>
