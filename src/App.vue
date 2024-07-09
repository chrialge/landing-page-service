<script>
import AppHeader from './components/partials/AppHeader.vue';
import AppFooter from './components/partials/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />

  <main id="site_main">
    <section id="jumbotron">
      <div class="container jumbo_container">
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

        </div>
        <div class="who_are_info">
          <span>Scopri di piu su di noi</span>
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
        <span>Scegli la categoria di corsi dalla quale vuoi iniziare</span>
        <h3>Categorie Popolari</h3>
        <button class="btn_primary">
          GUARDA TUTTO
        </button>
        <div class="categories_container">
          <div class="category_card">
            <div class="category_icon">
              
            </div>
            <div class="category_info"></div>
          </div>
        </div>
      </div>

    </section>
  </main>

  <AppFooter />


</template>

<style></style>
