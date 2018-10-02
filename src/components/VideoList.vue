<template>
    <ul>
        VideoList
        {{ videos.length }}
    </ul>
</template>

<script>
    export default {
        name: "VideoList",
        // Accept props as an array or as an object with slight type validation
        props: {
            videos: Array
        }
    };
</script>

<style>
</style>