<template>
    <div class="flex flex-col justify-between duration-200 rise w-full lg:w-1/3 bg-white shadow-lg hover:shadow-xl rounded-lg p-6">
        <div class="mb-8">
            <h3 class="text-gray-700 text-xl">{{name}}</h3>
            <p class="leading-tight text-gray-600">{{description}}</p>
        </div>
        <div>
            <a class="bg-gray-200 hover:bg-gray-300 rounded-md px-4 py-2" v-bind:href="link">GitHub</a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Project",
        props: {
            name: String,
            description: String,
            link: String
        }
    }
</script>

<style scoped>
    .rise:hover {
        -moz-transform: translate(0px, -4px);
        -webkit-transform: translate(0px, -4px);
        -o-transform: translate(0px, -4px);
        -ms-transform: translate(0px, -4px);
        transform: translate(0px, -4px);
    }
</style>