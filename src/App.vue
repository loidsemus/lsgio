<template>
    <div class="w-screen px-8 md:px-16 lg:px-32">
        <Header/>
        <Projects/>
    </div>
</template>

<script>
    import Header from "./components/Header";
    import Projects from "./components/Projects";

    export default {
        name: 'App',
        components: {
            Header,
            Projects
        }
    }
</script>
