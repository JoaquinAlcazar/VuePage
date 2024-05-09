<template>
    <img :src=image alt="imagen de {{title}}">
    <p>{{title}}</p>
    <p>{{description}}</p>
</template>

<script>
export default {
    name:"Show-Image",
    props: {
        image: null,
        title: null,
        description: null
    }
}
</script>