<template>
    <div class="content">
        <button @click="$emit('update-number', number)">{{ number }}</button>
    </div>
</template>

<script>
export default {
  props: ['number']
}
</script>

<style scoped>
.content {
    width: 50px;
}
</style>
