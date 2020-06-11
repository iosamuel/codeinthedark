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
      in the Dark (by IOSamuel) y una subscripcion a Platzi por 3 meses.
    </p>

    <ul>
      <li><img src="/images/platzi.jpg" alt="" /></li>
      <li><img src="" alt="" /></li>
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
        { name: "Yaroslay Bravo ", img: "", twitter: "" },
        { name: "Andres Felipe Pinchao Ramirez", img: "", twitter: "" },
        { name: "Laura Guzmán", img: "", twitter: "" },
        { name: "Joan Manuel Serna Leiton", img: "", twitter: "" },
        { name: "Luis Fernando Delgado Arboleda", img: "", twitter: "" },
        { name: "Camilo Andrés Gil Ballen", img: "", twitter: "" },
        { name: "Kathlen Montalvo Mendoza", img: "", twitter: "" },
        { name: "Fiorella Effio Saldivar", img: "", twitter: "" },
        { name: "Lenin Campoverde", img: "", twitter: "" },
        { name: "Jesús cruz dominguez", img: "", twitter: "" },
        { name: "Jorge Ivan Morales Obando", img: "", twitter: "" },
        { name: "Carlos Viteri", img: "", twitter: "" },
        { name: "Santiago Munguía López", img: "", twitter: "" },
        { name: "Diego Ignacio Ruiz Poblete", img: "", twitter: "" },
        { name: "María Fernanda Hernández Vargas ", img: "", twitter: "" },
        { name: "William Eduardo Velazquez Amarra ", img: "", twitter: "" },
        { name: "Alfredo Martínez", img: "", twitter: "" },
        { name: "Andrés Corral", img: "", twitter: "" },
        { name: "Jhon Michael García ", img: "", twitter: "" },
        { name: "Pablo", img: "", twitter: "" },
        { name: "Juan José López lira ", img: "", twitter: "" },
        { name: "José Barrios ", img: "", twitter: "" },
        { name: "Ernesto Román ", img: "", twitter: "" },
        { name: "Nicolas Molina", img: "", twitter: "" },
        { name: "Yan Arlex Vallejo Rosas", img: "", twitter: "" },
        { name: "Horacio Herrera García", img: "", twitter: "" },
        { name: "Jorge Betancur ", img: "", twitter: "" },
        { name: "Efrén Martinez rodriguez", img: "", twitter: "" }
      ],
      open: true
    };
  }
};
</script>

<style lang="scss" src="./styles/app.scss"></style>
