<template>
  <div id="app">
    <header>
      <!--logo-->
      <img src="./assets/imgs/logo.svg" class="logo" />

      <!--icons-->
      <ul class="icons">
        <li>
          <a href="#"><img src="./assets/imgs/facebook.svg" /></a>
        </li>
        <li>
          <a href="#"><img src="./assets/imgs/instagram.svg" /></a>
        </li>
        <li>
          <a href="#"><img src="./assets/imgs/twitter.svg" /></a>
        </li>
        <li>
          <a href="https://www.youtube.com/watch?v=XKd-qdNNko4"><img src="./assets/imgs/youtube.svg" /></a>
        </li>
      </ul>
    </header>

    <!--info-->
    <section>
      <div class="informations">
        <div class="texts">
          <h3>HAYAO MIYAZAKI</h3>
          <h1>
            SPIRITED <br />
            AWAY
          </h1>
          <p>
            Chihiro arrives in a magical world dominated by <br />
            a witch. Those who disobey her are turned into animals.
          </p>
        </div>

        <!--buttons-->
        <div class="buttons">
          <form action="https://www.netflix.com/title/60023642">
            <button type="submit" class="watch-movie">
              <img src="./assets/imgs/play.svg" />
              <p>WATCH NOW</p>
            </button>
          </form>

          <button type="submit" class="watch-trailer">
            <p>WATCH THE TRAILER</p>
          </button>
        </div>
      </div>

      <!--images-->
      <div class="images">
        <img class="img1" src="./assets/imgs/image1.svg" />
        <img class="img2" src="./assets/imgs/image2.svg" />
      </div>
    </section>

    <section class="movies">
      <h2>MORE MOVIES:</h2>
      <div class="moreMovies">
        <div class="movieTotoro cards-movies">
          <img src="./assets/imgs/totoro.png" />
          <h3>My Neighbor Totoro</h3>
        </div>
        <div class="movieCastelo cards-movies">
          <img src="./assets/imgs/castelo.jpg" />
          <h3>Howl's Moving Castle </h3>
        </div>
        <div class="movieVidas cards-movies">
          <img src="./assets/imgs/vidas.jpg" />
          <h3>Kaze Tachinu</h3>
        </div>
        <div class="movieMundo cards-movies">
          <img src="./assets/imgs/mundo.jpg" />
          <h3>The Secret World of Arrietty</h3>
        </div>
        <div class="movieGatos cards-movies">
          <img src="./assets/imgs/gatos.jpg" />
          <h3>The Cat Returns</h3>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: 0;
}

#app {
  background: linear-gradient(rgb(98, 141, 116), #1a4855);
  width: 100%;
  height: 100%;
}

body::-webkit-scrollbar {
  width: 15px;
}

body::-webkit-scrollbar-track {
  background: rgb(34, 33, 30); 
}

body::-webkit-scrollbar-thumb {
  background-color: rgb(88, 133, 90); 
  border-radius: 20px;  
  border: 3px solid rgb(34, 33, 30); 
}

header {
  height: 132px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  width: 128px;
  height: 65px;
  margin-left: 145px;
  margin-top: 31px;
}

.icons {
  list-style-type: none;
  display: flex;
  margin-top: 50px;
  margin-right: 155px;
}

.icons li {
  padding: 18px;
  transition: 0.5s;
}

.icons li:hover {
  transform: scale(1.2);
}

section {
  display: flex;
}

.informations {
  margin-left: 145px;
  margin-top: 54px;
}

.texts {
  font-family: Poppins;
  color: #f9f9f9;
}

.texts h3 {
  font-weight: 800;
  font-size: 20px;
}

.texts h1 {
  margin-top: 8px;
  font-weight: 800;
  font-size: 68px;
  line-height: 68px;
}

.texts p {
  margin-top: 18px;
  font-weight: 200;
}

.buttons {
  display: flex;
  margin-top: 58px;
  -webkit-transform: skew(-25deg);
  transform: skew(-25deg);
}

button p {
  font-family: Poppins;
  color: #f9f9f9;
  -webkit-transform: skew(25deg);
  transform: skew(25deg);
  font-size: 15px;
}

button {
  width: 220px;
  height: 45px;
}

.watch-movie {
  display: inline-flex;
  background: #658e76;
  padding: 8px 35px 8px 30px;
  margin-right: 13px;
  cursor: pointer;
}

.watch-movie:hover {
  transform: scale(1.05);
  transition: all ease 0.5s;
}

.watch-movie img {
  -webkit-transform: skew(25deg);
  transform: skew(25deg);
  margin-right: 10px;
}

.watch-trailer {
  border: 2px solid #658e76;
  background: transparent;
  cursor: pointer;

  /* Animation -----*/
  overflow: hidden;
  position: relative;
}

/* Animation -----*/
.watch-trailer:after {
  background: #fff;
  content: "";
  height: 9.68rem;
  left: -4.68rem;
  opacity: 0.2;
  position: absolute;
  top: -3.125rem;
  transform: rotate(35deg);
  transition: all 850ms cubic-bezier(0.19, 1, 0.22, 1);
  width: 3.125rem;
  z-index: -10;
}

.watch-trailer:hover:after {
  left: 120%;
  transition: all 850ms cubic-bezier(0.19, 1, 0.22, 1);
}

/*-------- Images --------*/
.images {
  margin-left: 50px;
  display: flex;
  margin-top: -40px;
  z-index: 1;
}

.img1 {
  margin-left: 60px;
  margin-right: -20rem;
  width: 400px;
  animation: float 9s ease-in-out infinite;
}

@keyframes float {
  0% {
    transform: scale(1.7);
    transform: translate(0, 0rem);
  }
  50% {
    transform: scale(1.7);
    transform: translate(0, 2.18rem);
  }
  100% {
    transform: scale(1.7);
    transform: translate(0, -0rem);
  }
}

.img2 {
  margin-left: 70px;
  width: 400px;
  height: auto;
  animation: float 8s ease-in-out infinite;
}

@keyframes float {
  0% {
    transform: scale(1.7);
    transform: translate(0, 0rem);
  }
  50% {
    transform: scale(1.7);
    transform: translate(0, 2.18rem);
  }
  100% {
    transform: scale(1.7);
    transform: translate(0, -0rem);
  }
}

.movies {
  display: flex;
  flex-direction: column;
}

.movies h2 {
  font-family: Poppins;
  font-weight: 400;
  color: #fff;
  margin-left: 130px;
  margin-top: 50px;
  margin-bottom: 20px;
  font-weight: 700;
}

.moreMovies {
  display: flex;
  width: 80%;
  color: rgb(218, 218, 218);
  font-family: Poppins;
  margin-bottom: 80px;
  margin-left: 130px;
}

.moreMovies .movieTotoro,
.movieCastelo,
.movieVidas,
.movieMundo,
.movieGatos {
  display: flex;
  align-items: center;
  flex-direction: column;
  
}


.movieCastelo,
.movieVidas{
  margin-left: 18px;
}

.movieMundo,
.movieGatos{
  margin-left: 10px;
}

.movieTotoro img,
.movieCastelo img,
.movieVidas img,
.movieMundo img,
.movieGatos img {
  width: 200px;
  height: 280px;
  border-radius: 5px;
  margin-bottom: 5px;
  transition: 0.2s;
  opacity: 1;
  cursor: pointer;
  box-shadow: 10px 5px 5px rgb(37, 37, 37);
}

.movieTotoro img:hover{
  opacity: 0.7;
}
.movieCastelo img:hover{
  opacity: 0.7;
}
.movieVidas img:hover{
  opacity: 0.7;
}
.movieMundo img:hover{
  opacity: 0.7;
}
.movieGatos img:hover{
  opacity: 0.7;
}

.movieTotoro h3,
.movieCastelo h3,
.movieVidas h3,
.movieMundo h3,
.movieGatos h3 {
  font-weight: 300;
  text-align: center;
  font-size: 16px;
}
</style>
