<template>
    <div>
        <h1 class="text-xl text-gray-700 font-bold mb-4">Highlighted projects</h1>
        <div class="flex flex-col lg:flex-row justify-between space-y-8 space-x-0 lg:space-y-0 lg:space-x-8 mb-16">
            <Project name="Configurator" description="A tool that allows you to edit plugin configuration
            file in a GUI, directly from within your Minecraft server."
                     link="#"/>
            <Project name="luid" description="An all-purpose (not really) Discord bot."
                     link="https://github.com/loidsemus/luid"/>
            <Project name="swecref" description="Sweclockers market improvements"
                     link="#"/>
        </div>

        <h1 class="text-xl text-gray-700 font-bold mb-4">The rest
            <span v-if="loading" class="text-gray-500"> is loading...</span></h1>
        <div class="flex flex-col lg:flex-row justify-between">
        </div>
    </div>
</template>

<script>
    import Project from "./Project";

    export default {
        name: "Projects",
        components: {
            Project
        },
        data() {
            return {
                loading: true
            }
        },
    }
</script>