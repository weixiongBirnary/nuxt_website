<template>
    <div :editable="blok" class="util__flex-eq">
        {{ blok.name }}
    </div>
</template>

<script>
export default {
    props: ['blok']
}
</script>