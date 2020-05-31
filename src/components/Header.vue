<template>
    <div class="md:flex md:items-center py-40 md:py-16">
        <img src="../assets/logo.png" alt="loidsemus avatar" class="mx-auto md:mx-0 w-32 h-32 rounded-lg mb-8 md:mb-0">
        <h1 class="text-5xl text-gray-800 font-bold text-center md:text-left md:ml-8 wrap">loidsemus</h1>
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
    @media (min-width: 768px) {
        .wrap {
            max-width: 4.5ch !important;
            word-wrap: break-word;
            line-height: 1;
        }
    }
</style>