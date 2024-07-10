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
        <nav class="container sidebar">
            <div class="logo">
                <img src="../../../public/images/logo.png" alt="">
            </div>
            <div class="btn_dropdown" @click="this.dropdown = !this.dropdown" v-show="this.dropdownActive">
                <button>
                    <i class="fa-solid fa-ellipsis-vertical"></i>
                </button>
            </div>

            <div class="dropdown" v-if="this.dropdown">
                <button type="button" class="btn_close" @click="this.dropdown = !this.dropdown">
                    <i class="fa-solid fa-xmark"></i>
                </button>
                <div class="link-header">
                    <ul>
                        <li>
                            <a href="#">
                                HOME
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                CORSI
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                EVENTI
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                CONTATTI
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                REGISTRATI
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="link-header" v-if="this.dropdownActive === false">
                <ul>
                    <li>
                        <a href="#">
                            HOME
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            CORSI
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            EVENTI
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            CONTATTI
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            REGISTRATI
                        </a>
                    </li>
                </ul>
            </div>
            <div class="icons-header">
                <ul>
                    <li>
                        <a href="#">
                            <i class="fa-regular fa-circle-user"></i>
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <i class="fa-regular fa-heart"></i>
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <i class="fa-solid fa-bag-shopping"></i>
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <i class="fa-solid fa-magnifying-glass"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </nav>
    </header>

</template>

<style></style>