<template>
    <div class="md:flex md:items-center md:justify-between py-40 md:py-24">
        <div class="md:flex md:items-center">
            <img src="../assets/logo.png" alt="loidsemus avatar"
                 class="mx-auto md:mx-0 w-32 h-32 rounded-lg mb-8 md:mb-0">
            <a href="https://github.com/loidsemus"><h1
                    class="text-5xl text-gray-800 font-bold text-center md:text-left md:ml-8 md:wrap">loidsemus</h1></a>
        </div>
        <a href="https://github.com/loidsemus" class="hidden md:block"><img src="../assets/gtihub-mark.png" alt="GitHub"
                                                                            class="w-8 h-8 opacity-75 hover:opacity-100 duration-200"></a>
    </div>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
    @media (min-width: 768px) {
        .md\:wrap {
            max-width: 4.5ch !important;
            word-wrap: break-word !important;
            line-height: 1;
        }
    }
</style>