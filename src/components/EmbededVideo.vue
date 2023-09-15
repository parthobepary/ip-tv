<template>
    <div class="">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/5BE1yrqkG9c?si=iEXE8PvWfGesbrYS"
            title="YouTube video player" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen></iframe>
    </div>
</template>
<script setup>

</script>
<style scoped>
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
    iframe {
        width: 100% !important;
        height:350px !important;
    }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
    iframe {
        width: 100% !important;
        height: 380px !important;
    }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
    iframe {
        width: 100% !important;
        height: 400px !important;
    }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
    iframe {
        width: 100% !important;
        height: 450px !important; 
    }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
    iframe {
        width: 100% !important;
        height:500px !important;
    }
}
</style>