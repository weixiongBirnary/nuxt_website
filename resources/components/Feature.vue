<template>
    <div :editable="blok" class="feature util__flex-eq">
        <img :src="blok.logo" class="feature--img">
        <p class="feature--name">{{ blok.name }}</p>
        <p class="feature--text">{{ blok.text }}</p>
    </div>
</template>

<script>
export default {
    props: ['blok']
}
</script>
 <style lang="scss">
 .feature {
     text-align: center;
     padding: 30px 10px 100px;
     

     &--name{
        font-weight: bold;
     }
 }

 </style>