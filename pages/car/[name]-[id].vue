<script setup>
    const route= useRoute();
    if(route.params.make ) {
        console.log(route.params.make );
    }
    useHead({
        title: toTitleCase(route.params.name)
    })
    definePageMeta({
        layout: 'custom'
    })

    function toTitleCase(str) {
        return str.replace(
            /\w\S*/g,
            function (txt) {
                return txt.charAt(0).toUpperCase()
            }
        )
    }
</script>
<template>
    <!-- CAR DETAIL PAGE -->
    
        <div>
            <!-- CAR HERO -->
            <DetailHero />
            <!-- CAR HERO -->
        </div>

        <!-- CAR ATTRIBUTES -->
        <DetailAttributes />
        <!-- CAR ATTRIBUTES -->

        <!-- CAR DESCRISPTION -->
        <DetailDescription />
        <!-- CAR DESCRISPTION -->

        <!-- CAR CONTACT -->
        <DetailContact />
        <!-- CAR CONTACT -->


    <!-- CAR DETAIL PAGE   -->
</template>