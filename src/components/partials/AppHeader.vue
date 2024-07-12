<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            dropdown: false,
            dropdownActive: false

        }
    },
    methods: {

    },
    mounted() {
        if (innerWidth <= 1000) {
            this.dropdownActive = true;
        }
    }
}
</script>

<template>

    <header id="site_header">
        <nav class="container sidebar" role="navigation">
            <div class="logo">
                <img src="../../../public/images/logo.jpg" alt="image of logo of joker school" width="50px">
                <h1 class="color_subtitle">Joker school</h1>
            </div>
            <div class="btn_dropdown" style="transition: 1s ease-in-out;" @click="this.dropdown = !this.dropdown"
                v-show="this.dropdownActive">
                <button aria-roledescription="open dropdown">
                    <i class="fa-solid fa-ellipsis-vertical" role="presentation"></i>
                </button>
            </div>
            <Transition>
                <div class="dropdown" v-if="this.dropdown" aria-haspopup="true" :aria-expanded="this.dropdownActive">
                    <button type="button" class="btn_close" @click="this.dropdown = !this.dropdown"
                        style="transition: 1s ease-in-out;" aria-label="close"
                        aria-roledescription="button close dropdown">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                    <div class="link-header" aria-label="dropdown" aria-roledescription="dropdown with list of page">
                        <ul>
                            <li>
                                <a href="#" role="button" aria-roledescription="page Home">
                                    HOME
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-roledescription="page Corsi">
                                    CORSI
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-roledescription="page Eventi">
                                    EVENTI
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-roledescription="page Contatti">
                                    CONTATTI
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-roledescription="page registrati">
                                    REGISTRATI
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </Transition>
            <div class="link-header" v-if="this.dropdownActive === false">
                <ul>
                    <li>
                        <a href="#" role="button" aria-roledescription="page Home">
                            HOME
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-roledescription="page Corsi">
                            CORSI
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-roledescription="page Eventi">
                            EVENTI
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-roledescription="page Contatti">
                            CONTATTI
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-roledescription="page Registrati">
                            REGISTRATI
                        </a>
                    </li>
                </ul>
            </div>
            <div class="icons-header">
                <ul>
                    <li>
                        <a href="#" role="button" aria-label="login">
                            <i class="fa-regular fa-circle-user" role="presentation"></i>
                        </a>
                    </li>
                    <li>
                        <a href="" role="button" aria-label="favourite">
                            <i class="fa-regular fa-heart" role="presentation"></i>
                        </a>
                    </li>
                    <li>
                        <a href="" role="button" aria-label="cart">
                            <i class="fa-solid fa-bag-shopping" role="presentation"></i>
                        </a>
                    </li>
                    <li>
                        <a href="" role="button" aria-label="search">
                            <i class="fa-solid fa-magnifying-glass" role="presentation"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>

</template>

<style></style>