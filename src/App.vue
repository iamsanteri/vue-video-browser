<template>
    <div>
        <SearchBar></SearchBar>
    </div>
</template>

<script>
    // Remember to import components to the housing component
    import SearchBar from "./components/SearchBar";

    export default {
        name: "App",
        // Let Vue know that you will have component within the template!
        components: {
            SearchBar
        }
    };
</script>