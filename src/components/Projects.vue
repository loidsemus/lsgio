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
            <span v-if="loading" class="text-gray-500"> is loading...</span>
            <span v-else-if="errored" class="text-gray-500"> couldn't be loaded from GitHub :(</span>
            <span v-else class="text-gray-500"> from GitHub, recent first</span>
        </h1>
        <ul v-if="!loading" class="space-y-8 mb-8">
            <li v-for="repo in repos" :key="repo.id">
                <a :href="repo.html_url"><h3 class="text-gray-700 text-xl">
                    <span class="text-gray-500" v-if="repo.fork">forked: </span>
                    {{repo.name}}
                    <span class="text-gray-500" v-if="repo.language"> / {{repo.language}}</span>
                </h3></a>
                <p class="leading-tight text-gray-600">{{repo.description}}</p>
            </li>
        </ul>
        <div class="flex flex-col lg:flex-row justify-between">
        </div>
    </div>
</template>

<script>
    import axios from "axios"
    import Project from "./Project";

    export default {
        name: "Projects",
        components: {
            Project
        },
        data() {
            return {
                loading: true,
                errored: false,
                repos: []
            }
        },
        mounted() {
            axios.get("https://api.github.com/users/loidsemus/repos?sort=pushed")
                .then(response => {
                    this.repos = response.data
                })
                .catch(() => this.errored = true)
                .finally(() => this.loading = false)
        }
    }
</script>