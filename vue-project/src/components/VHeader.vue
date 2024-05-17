<script setup>

import { ref } from 'vue';

const menuOpen = ref(false);
const toggleMenu = () => {
    menuOpen.value = !menuOpen.value; 
};

</script>

<template>
    <header>
        <nav class="navigation">
            <div class="container">
                <div class="navigation__wrap">
                    <img src="/logo.svg" alt="" class="navigation__logo">
                    <button class="burger" :class="{'open': menuOpen}" @click="toggleMenu">
                        <span></span>
                        <span></span>
                        <span></span>
                    </button>
                        <ul class="navigation__list">
                        <li class="navigation__list-item">
                            <a href="" class="navigation__list-item-link">Возможности</a>
                        </li>
                        <li class="navigation__list-item">
                            <a href="" class="navigation__list-item-link">Как это работает?</a>
                        </li>
                        <li class="navigation__list-info">
                            г Сургут, ул Базовая, д. 34, офис 10 <br> ОГРН 1238600001200 <br> ИНН 8602309464
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<style scoped>

</style>