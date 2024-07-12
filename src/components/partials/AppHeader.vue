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
        <nav class="container sidebar" role="navigation" aria-label="heading of the page">
            <div class="logo">
                <img src="../../../public/images/logo.jpg" alt="logo joker school" width="50px" role="img">
                <h1 class="color_subtitle">Joker school</h1>
            </div>
            <div class="btn_dropdown" style="transition: 1s ease-in-out;" @click="this.dropdown = !this.dropdown"
                v-show="this.dropdownActive">
                <button aria-roledescription="open to sidebar">
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
                                <a href="#" role="button" aria-label="go to page Home">
                                    HOME
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-label="go to page Corsi">
                                    CORSI
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-label="go to page Eventi">
                                    EVENTI
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-label="go to page Contatti">
                                    CONTATTI
                                </a>
                            </li>
                            <li>
                                <a href="#" role="button" aria-label="go to page registrati">
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
                        <a href="#" role="button" aria-label="go to page Home">
                            HOME
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="go to page Corsi">
                            CORSI
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="go to page Eventi">
                            EVENTI
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="go to page Contatti">
                            CONTATTI
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="go to page Registrati">
                            REGISTRATI
                        </a>
                    </li>
                </ul>
            </div>
            <div class="icons-header">
                <ul>
                    <li>
                        <a href="#" role="button"
                            aria-label="go to login or register, and if you logged enter your account">
                            <i class="fa-regular fa-circle-user" role="presentation"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="go to your favourites lesson and course">
                            <i class="fa-regular fa-heart" role="presentation"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="go to your cart">
                            <i class="fa-solid fa-bag-shopping" role="presentation"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#" role="button" aria-label="search course, professor or categgory">
                            <i class="fa-solid fa-magnifying-glass" role="presentation"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>

</template>

<style></style>