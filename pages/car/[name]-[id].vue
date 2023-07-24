<script setup>

    const route= useRoute();
    const { toTitleCase }= useUtilities();
    if(route.params.make ) {
        console.log(route.params.make );
    }
    useHead({
        title: toTitleCase(route.params.name)
    })
    definePageMeta({
        layout: 'custom'
    })
</script>
<template>
    <!-- CAR DETAIL PAGE -->
    
    <div>
        <!-- CAR HERO -->
        <DetailHero />
        <!-- CAR HERO -->        

        <!-- CAR ATTRIBUTES -->
        <DetailAttributes />
        <!-- CAR ATTRIBUTES -->

        <!-- CAR DESCRISPTION -->
        <DetailDescription />
        <!-- CAR DESCRISPTION -->

        <!-- CAR CONTACT -->
        <DetailContact />
        <!-- CAR CONTACT -->
    
    </div>
    <!-- CAR DETAIL PAGE   -->
</template>