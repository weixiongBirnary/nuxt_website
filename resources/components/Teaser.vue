<template>
  <div v-editable="blok" class="teaser">
    {{ blok.headline }}
    <component  v-if="slider" :blok="slider" :is="slider.component"></component>
    <div class="teaser_pag">
        <button
            v-for="(blok, index) in blok.body"
            :key="index"
            @click="changeCurrentImage(index)"
            class="teaser_pag-dot"
            :class="{ 'teaser_pag-dot--current': currentIndex == index }"
        ></button>
    </div>
  </div>
</template>

<script>
export default {
  props: ['blok'],
  data() {
      return {
          currentIndex: 0
      }
  },
  computed: {
      slider() {
          let slider = this.blok.body.filter(( slider, index ) => {
              return this.currentIndex == index
          });
          if(slider.length) return slider[0];
          return null
      }
  },
  methods: {
      changeCurrentImage(index) {
          this.currentIndex = index;
      }
  }

}
</script>

<style lang="scss" >
    .teaser_pag {
        width: 100%;
        margin: 30px 0;
        text-align: center;
    }
    .teaser_pag-dot {
        text-indent: -999999px;
        border: 0;
        border-radius: 50%;
        height: 16px;
        width: 16px;
        background-color: #ccc;
        cursor: pointer;
        padding: 0;
        margin: 5px 6px;
        -webkit-appearance: none;

        &--current {
            background-color: #000;
        }

    }

</style>