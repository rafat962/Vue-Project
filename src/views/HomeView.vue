<script setup>
import Hero from "../components/Hero.vue";
import HomeCards from "../components/HomeCards.vue";
import JobListings from "../components/JobListings.vue";
</script>

<template>
    <Navebar />
    <Hero title="Become a Hero" subtitle="Find your dream job today" />
    <HomeCards />
    <JobListings limit="3" showButton="true" />
</template>
