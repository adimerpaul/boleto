<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Footer from "./components/Footer.vue";
import Header from "./components/Header.vue";
import { ref } from 'vue';
const peliculas = ref([
  {
    id: 1,
    title: 'Alone',
    image: '/assets/images/movie/movie01.jpg',
    rating: 88,
    ratingPublic: 89,
    genre: 'Action'
  },
  {
    id: 2,
    title: 'Mars',
    image: '/assets/images/movie/movie02.jpg',
    rating: 56,
    ratingPublic: 62,
    genre: 'Adventure'
  },
  {
    id: 3,
    title: 'Venus',
    image: '/assets/images/movie/movie03.jpg',
    rating: 78,
    ratingPublic: 80,
    genre: 'Drama'
  },
  {
    id: 4,
    title: 'Horror Night',
    image: '/assets/images/movie/movie04.jpg',
    rating: 90,
    ratingPublic: 95,
    genre: 'Horror'
  }
])
</script>

<template>
  <Header />
  <!-- ==========Movie-Section========== -->
  <section class="movie-section padding-top padding-bottom">
    <div class="container">
      <div class="tab">
        <div class="section-header-2">
          <div class="left">
            <h2 class="title">movies</h2>
            <p>Be sure not to miss these Movies today.</p>
          </div>
          <ul class="tab-menu">
            <li class="active">
              now showing
            </li>
            <li>
              coming soon
            </li>
            <li>
              exclusive
            </li>
          </ul>
        </div>
        <div class="tab-area mb-30-none">
          <div class="tab-item active">
            <div class="owl-carousel owl-theme tab-slider">
              <div class="item" v-for="pelicula in peliculas" :key="pelicula.id">
                <div class="movie-grid">
                  <div class="movie-thumb c-thumb">
                    <a href="#0">
                      <img :src="pelicula.image" :alt="pelicula.title">
                    </a>
                  </div>
                  <div class="movie-content bg-one">
                    <h5 class="title m-0">
                      <a :href="`#${pelicula.title}`">{{ pelicula.title }}</a>
                    </h5>
                    <ul class="movie-rating-percent">
                      <li>
                        <div class="thumb">
                          <img src="/assets/images/movie/tomato.png" alt="movie">
                        </div>
                        <span class="content">{{ pelicula.rating }}%</span>
                      </li>
                      <li>
                        <div class="thumb">
                          <img src="/assets/images/movie/cake.png" alt="movie">
                        </div>
                        <span class="content">{{ pelicula.ratingPublic }}%</span>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie02.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">mars</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie03.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">venus</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie04.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">horror night</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
            </div>
          </div>
          <div class="tab-item">
            <div class="owl-carousel owl-theme tab-slider">
              AAAAAAAAAAAAAAAAAAAAAA
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie01.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">alone</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie02.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">mars</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie03.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">venus</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie04.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">horror night</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
            </div>
          </div>
          <div class="tab-item">
            <div class="owl-carousel owl-theme tab-slider">
              BBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBB
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie01.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">alone</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie02.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">mars</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie03.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">venus</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
<!--              <div class="item">-->
<!--                <div class="movie-grid">-->
<!--                  <div class="movie-thumb c-thumb">-->
<!--                    <a href="#0">-->
<!--                      <img src="/assets/images/movie/movie04.jpg" alt="movie">-->
<!--                    </a>-->
<!--                  </div>-->
<!--                  <div class="movie-content bg-one">-->
<!--                    <h5 class="title m-0">-->
<!--                      <a href="#0">horror night</a>-->
<!--                    </h5>-->
<!--                    <ul class="movie-rating-percent">-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/tomato.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                      <li>-->
<!--                        <div class="thumb">-->
<!--                          <img src="/assets/images/movie/cake.png" alt="movie">-->
<!--                        </div>-->
<!--                        <span class="content">88%</span>-->
<!--                      </li>-->
<!--                    </ul>-->
<!--                  </div>-->
<!--                </div>-->
<!--              </div>-->
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- ==========Movie-Section========== -->
  <Footer />
</template>

<!--<style scoped>-->
<!--.logo {-->
<!--  height: 6em;-->
<!--  padding: 1.5em;-->
<!--  will-change: filter;-->
<!--  transition: filter 300ms;-->
<!--}-->
<!--.logo:hover {-->
<!--  filter: drop-shadow(0 0 2em #646cffaa);-->
<!--}-->
<!--.logo.vue:hover {-->
<!--  filter: drop-shadow(0 0 2em #42b883aa);-->
<!--}-->
<!--</style>-->
