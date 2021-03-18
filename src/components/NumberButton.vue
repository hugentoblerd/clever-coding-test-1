<template>
    <div class="content">
        <a href="#" @click="$emit('update-number', number)">{{ number }}</a>
    </div>
</template>

<script>
export default {
  props: ['number']
}
</script>

<style scoped>
a {
    display: inline-block;
    padding: 0.5em 1.3em;
    border: 0.16em solid #000000;
    margin: 0.4em auto;
    box-sizing: border-box;
    text-decoration: none;
    font-weight: 400;
    color: #000000;
}
a:hover {
    background-color: #dedede;
}
.active > a {
    border-color: #ff7003;
}

/* --- Tablet and Desktop --- */
@media all and (min-width: 768px) {
    a {
        margin: 0 0.3em 0.3em 0;
    }
}
</style>
