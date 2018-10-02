<template>
    <div>
        <SearchBar @termChange="onTermChange"></SearchBar>
        <VideoList></VideoList>
    </div>
</template>

<script>
    // Remember to import components to the housing component
    // Three steps: 
    // 1. Add component import with relative path in <script> tags
    // 2. Add component to the template of the parent
    // 3. Add component to the components object of export default
    
    import axios from "axios";
    import SearchBar from "./components/SearchBar";
    import VideoList from "./components/VideoList";
    const API_KEY = "AIzaSyA1MoOT1Ml5d3-zpGNZs2UYcehCq5skPPE";

    export default {
        name: "App",
        // Let Vue know that you will have component within the template!
        components: {
            SearchBar,
            VideoList
        },
        methods: {
            onTermChange(searchTerm) {
                axios.get("https://www.googleapis.com/youtube/v3/search", {
                    params: {
                        key: API_KEY,
                        type: "video",
                        part: "snippet",
                        q: searchTerm
                    }
                }).then(response => console.log(response));
            }
        }
    };
</script>