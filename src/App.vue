<script>
import AppHeader from './components/partials/AppHeader.vue';
import AppFooter from './components/partials/AppFooter.vue';

import { Swiper, SwiperSlide } from 'swiper/vue';

// import styles bundle
import 'swiper/css';


import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Pagination, Navigation } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
    AppHeader,
    AppFooter
  },
  data() {
    return {
      socialProfessor: false,
      index: 0,
    }
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
    };
  },
  methods: {
    mouseUp(n) {
      this.index = n;
      this.socialProfessor = true
      console.log(this.socialProfessor)
    },
    mouseDown() {
      this.socialProfessor = false
      console.log(this.socialProfessor)
    }
  },
  mounted() {


    // init Swiper:

  }
}
</script>
<template>
  <AppHeader />

  <main id="site_main">
    <section id="jumbotron">
      <div class="container jumbo_container">
        <div class="jumbo_text">

          <h2>Corso di clown</h2>
          <p>
            Stai cercando una lavoro che ti porta a girare tutta l'europa e conoscere persone variegate, sei nel posto
            giusto!
          </p>
          <div class="search_container">
            <input type="search" name="text_user" id="text_user" placeholder="search">
            <button class="search_btn">
              <i class="fa-solid fa-magnifying-glass"></i>
            </button>
          </div>
        </div>
        <div class="jumbo_img">
          <img src="/images/billboard-img.png" alt="image of clown with pc">
        </div>



      </div>


    </section>


    <section id="banner_data">
      <div class="container container_data">
        <div class="banner_single">
          <h4>100+</h4>
          <span>MAGHI DEL CODICE</span>
        </div>

        <div class="banner_single">
          <h4>100+</h4>
          <span>MAGHI DEL CODICE</span>
        </div>

        <div class="banner_single">
          <h4>100+</h4>
          <span>MAGHI DEL CODICE</span>
        </div>

        <div class="banner_single">
          <h4>100+</h4>
          <span>MAGHI DEL CODICE</span>
        </div>
      </div>

    </section>

    <section id="who_are">
      <div class="container container_who_are">
        <div class="who_are_image">
          <img src="/images/about-img.jpg" alt="">
        </div>
        <div class="who_are_info">
          <h5 class="color_subtitle">Scopri di piu su di noi</h5>
          <h2>Chi Siamo</h2>
          <p>
            Benvenuti nel nostro magico mondo dove potresti trovare la tua strada! Offriamo corsi di circense,
            trapezista,
            giochelliere, domatore e sopratutto la nostra rinomata scuola di pagliacci. Interattivita nelle lezioni
            esperti nel settore del circo europeo.
          </p>
          <ul>
            <li>
              Esperti preparatori atletici e fisoterapisti per prepararvi atleticamente
            </li>
            <li>
              Corsi specifici ad singolo ruolo, coinvolgente per aiutare l'appredimento e la sicurezza
            </li>
            <li>
              Abbiamo vinto per la miglior scuola di pagliacci.
            </li>
          </ul>
          <button class="btn_primary">
            SCOPRI DI PIU
          </button>
        </div>
      </div>

    </section>


    <section id="category">

      <div class="container container_category">
        <div class="category_header">
          <div class="category_text">
            <h5 class="color_subtitle">Scegli la categoria di corsi dalla quale vuoi iniziare</h5>
            <h2>Categorie Popolari</h2>
          </div>

          <button class="btn_primary">
            GUARDA TUTTO
          </button>
        </div>

        <div class="categories_container">
          <div class="category_card" v-for="n in 6">
            <div class="category_icon">
              <i class="fa-solid fa-hippo"></i>
            </div>
            <div class="category_info">
              <h4>DOMATORE</h4>
              <span>20 corsi</span>
            </div>
          </div>


        </div>
      </div>

    </section>

    <section id="course">
      <div class="container">
        <h5 class="text_center color_subtitle">Alcuni dei nostri corsi online piu popolari</h5>
        <h2 class="text_center">Esplora I Corsi Online</h2>
        <div class="container_course">
          <div class="card_course" v-for="n in 8">
            <div class="card_top">

            </div>
            <div class="card_body">
              <div class="text_subtitle text_gray">
                <span>PAGLIACCIO</span>
                <span>
                  <i class="fa-regular fa-clock"></i>
                  1H 50M
                </span>
              </div>
              <div class="title">
                <h4>
                  Palloncini A Forma Di Cane
                </h4>

              </div>

            </div>
            <div class="card_foooter">
              By: Lorenzo Raffaeli
              <i class="fa-solid fa-star" style="color: #4cc083;" v-for="n in 5"></i>
            </div>
          </div>
        </div>
        <div class="btn_all_course">
          <button class="btn_primary">
            GUARDA TUTTI I CORSI
          </button>
        </div>

      </div>

    </section>

    <section id="feedback">
      <div class="container">
        <h5 class="text_center color_subtitle">Cosa dicono gli studenti</h5>
        <h2 class="text_center">Recensioni</h2>
        <swiper :spaceBetween="30" :navigation="true" :pagination="{
          clickable: true,
        }" :modules="modules" class="mySwiper">
          <swiper-slide v-for="n in 3">
            <p>
              "E stato divertente le interazioni con professionisti europei che mi ha indirizzato verso la mia
              strada"
            </p>
            <div class="user_feedback">
              <div class="user_img">
                <img src="/user-account.png" alt="">
              </div>
              <div class="user_info">
                <h4>Lorenzo Raffaeli</h4>
                <span>Stundetessa</span>
              </div>
            </div>
          </swiper-slide>
        </swiper>



      </div>

    </section>

    <section id="professor">
      <div class="container">
        <h5 class="text_center color_subtitle">Stalkera i nostri insegnanti</h5>
        <h2 class="text_center">I Nostri Insegnanti</h2>
        <div class="container_professor">
          <div class="card_professor" :class="[n == 5 ? 'card_important' : '']" v-for="n in 5" @mouseenter="mouseUp(n)"
            @mouseleave="mouseDown()">
            <div class="card_img">
              <img src="/recognitions.png" alt="">
              <div class="social_professor" v-show="this.socialProfessor && n == index">
                <ul>
                  <li>
                    <a href="#">
                      <i class="fa-brands fa-facebook"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="fa-brands fa-twitter"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="fa-brands fa-instagram"></i>
                    </a>
                  </li>
                  <li>
                    <a href="#">
                      <i class="fa-brands fa-linkedin"></i>
                    </a>
                  </li>
                </ul>

              </div>
            </div>

            <div class="card_body">
              <h4 class="card_title text_center">Francesco battista</h4>
              <p class="card_role text_center color_subtitle">Giocolliere</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="value_adder">
      <div class="container">
        <h5 class="text_center color_subtitle">Valori Aggiunti</h5>
        <h2 class="text_center">I Nostri Corsi Piacciono Perche...</h2>
        <ul>
          <li>Ridendo, l'apprendimento dell'arte del circo diventa un'esperienza divertente e piacevole</li>
          <li>I nostri insegnanti sono conosciuti in tutta europa per la loro maestria</li>
          <li>Niente paura, abbiamo dottori e fisoterapisti in caso di lesione</li>
          <li>Scuola di rinomata di pagliacci</li>
        </ul>
      </div>

    </section>

    <section id="accordion">
      <div class="container">
        <div class="card" v-for="n in 3">
          <div class="icon">
            <i class="fa fa-address-book" aria-hidden="true"></i>
          </div>
          <div class="accordion_item" :class="[n == 0 || n % 2 ? 'left_card' : '']">
            <div class="accordion_phone" :class="[n == 0 || n % 2 ? 'accordion_left_title' : 'accordion_title']">
              <h3>Primo Step</h3>
            </div>
            <div class="accordion_paragraph">
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis et iusto explicabo obcaecati hic
                doloribus
                possimus maxime exercitationem reprehenderit. Explicabo aliquam quisquam dolores id, dicta molestias ut
                error commodi excepturi.
              </p>
              <button class="btn_primary">
                REGISTRATI
              </button>

            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="newsletter">
      <div class="container">
        <div class="text_mewsletter">
          <h2>Iscriviti E Ottieni Il 20% Di Sconto Sul Tuo Primo Corso Online</h2>
          <h5 class="color_subtitle">Iscriviti alla nostra newsletter e non perderti mai nessuna offerta</h5>
        </div>

        <form action="" method="post">
          <input type="email" name="email" id="email" placeholder="lascia la tua email*">
          <button class="text_center btn_primary" type="submit">REGISTRATI</button>
        </form>
      </div>
    </section>

  </main>

  <AppFooter />


</template>

<style></style>
