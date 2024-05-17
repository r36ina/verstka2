<script setup>

import VHeader from "@/components/VHeader.vue";
import VPromo from "@/components/VPromo.vue";
import VClass from "@/components/VClass.vue";
import VHistory from "@/components/VHistory.vue";
import VPossibilities from "@/components/VPossibilities.vue";
import VIdea from "@/components/VIdea.vue";
import VReviews from "@/components/VReviews.vue";
import VFooter from "@/components/VFooter.vue";
</script>

<template>
    <div class="body_wrapper">
        <v-header></v-header>

        <main>
            <v-promo></v-promo>
            <v-class></v-class>
            <v-history></v-history>
            <v-possibilities></v-possibilities>
            <v-idea></v-idea>
            <v-reviews></v-reviews>
        </main>

        <v-footer></v-footer>
    </div>
</template>

<style scoped>

</style>
