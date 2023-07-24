<script setup>
    const route= useRoute();
    const { toTitleCase }= useUtilities();
    if(route.params.make ) {
        console.log(route.params.make );
    }
    useHead({
        title: `${
            route.params.make ? toTitleCase(route.params.make) : 'Cars'
        } in ${route.params.city}`
    })

    definePageMeta({
        layout: 'custom'
    })
  
</script>
<template>
    <!-- CARS PAGE -->

        <div class="mt-32 flex">
            <!-- CAR SIDE BAR -->
            <CarSideBar />
            <!-- CAR SIDE BAR -->

            <!-- CAR CARDS -->
            <NuxtPage />
            <!-- CAR CARDS -->
        </div>
    <!-- CARS PAGE -->
</template>