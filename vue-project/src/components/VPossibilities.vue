<script setup>

import Swiper from "swiper";
import { onMounted } from "vue";
import { Pagination } from "swiper/modules";

const possibilities = [
    {
        img: {
            src: '/socity.svg',
            alt: 'society',
        },
        name: 'Общение с классом',
        description: 'Видеосвязь Чат с классом'
    },
    {
        img: {
            src: '/classes.svg',
            alt: 'classes',
        },
        name: 'Проведение занятий',
        description: 'Презентация файлов Демонстрация экрана'
    },
    {
        img: {
            src: '/attend.svg',
            alt: 'attend',
        },
        name: 'Посещаемость',
        description: 'Автоматическое отслеживание присутствующих'
    },
    {
        img: {
            src: '/history.svg',
            alt: 'history',
        },
        name: 'История занятий',
        description: 'Материалы урока'
    }
]

onMounted(()=>{
    const swiper = new Swiper(".possibilities__swiper", {
        modules: [Pagination],
        slidesPerView: 1,
        spaceBetween: 30,
        pagination: {
            el: ".swiper-pagination",
            clickable: true,
        },
        breakpoints: {
            768: {
                slidesPerView: 2,
            },
            1200: {
                slidesPerView: 4,
            },
        },
    });
})


</script>

<template>
    <section class="possibilities">
        <div class="container">
            <h2>Возможности</h2>
            <div class="swiper possibilities__swiper">
                <div class="swiper-wrapper">
                    <div class="swiper-slide" 
                        v-for="(item, index) in possibilities" 
                        :key="index"
                    >
                        <div class="possibilities__card"
                            :class="{
                                'possibilities__card1': index % 2 == 0,
                                'possibilities__card2': index % 2 != 0,
                            }"
                        >
                            <div class="possibilities__card-icon">
                                <img :src="item.img.src" :alt="item.img.alt">
                            </div>
                            <div class="possibilities__card-name">{{ item.name }}</div>
                            <p>{{ item.description }}</p>
                        </div>
                    </div>
                </div>
                <div class="swiper-pagination"></div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.possibilities{
    .swiper-pagination{
        position: relative;
        bottom: 0;
        margin-top: 10px;
    }
    .possibilities__swiper{
        z-index: 0;
    }
    
}
</style>