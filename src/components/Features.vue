<template>
  <div class="features" id="features">
    <div class="container">
      <h1 class="title features__title">Heading Feature title goes here</h1>
      <p class="features__text">Duis bibendum diam non erat facilaisis tincidunt. Fusce leo neque, lacinia at tempor vitae, porta at arcu. Vestibulum varius non dui at pulvinar. Ut egestas orci in quam sollicitudin aliquet.</p>
      <div class="features__feature-block">
        <div class="features__list-features">
          <div class="features__feature"
            :class="selected_feature_index == 0 ? 'features__feature_selected' : ''"
            @click="selected_feature_index = 0">
            <img src="../assets/img/like.png" alt="" class="features__feature-icon">
            <p class="features__feature-name">Heading title one</p>
          </div>
          <div class="features__feature"
            :class="selected_feature_index == 1 ? 'features__feature_selected' : ''"
            @click="selected_feature_index = 1">
            <img src="../assets/img/work.png" alt="" class="features__feature-icon">
            <p class="features__feature-name features__feature-name_selected">Heading title one</p>
          </div>
          <div class="features__feature"
            :class="selected_feature_index == 2 ? 'features__feature_selected' : ''"
            @click="selected_feature_index = 2">
            <img src="../assets/img/leaf.png" alt="" class="features__feature-icon">
            <p class="features__feature-name">Heading title one</p>
          </div>
          <div class="features__feature"
            :class="selected_feature_index == 3 ? 'features__feature_selected' : ''"
            @click="selected_feature_index = 3">
            <img src="../assets/img/window.png" alt="" class="features__feature-icon">
            <p class="features__feature-name">Heading title one</p>
          </div>
          <div class="features__feature"
            :class="selected_feature_index == 4 ? 'features__feature_selected' : ''"
            @click="selected_feature_index = 4">
            <img src="../assets/img/umbrella.png" alt="" class="features__feature-icon">
            <p class="features__feature-name">Heading title one</p>
          </div>
        </div>
        <div class="features__scroll"></div>
        <div class="features__preview-block">
          <img :src="features[selected_feature_index]" alt="" class="features__feature-icon-preview">
          <h2 class="features__feature-title">Heading Feature title goes here</h2>
          <p class="features__feature-description">Nunc accumsan hendrerit nunc, ac venenatis magna facilisis quis. Ut sit amet mi ac neque sodales facilisis. Nullam tempus fermentum lorem nec interdum. Ut id orci id sapien imperdiet vehicula. Etiam quis dignissim ante. Donec convallis tincidunt ligula, ac luctus mi interdum a.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import like from '../assets/img/like.png'
import work from '../assets/img/work2.png'
import leaf from '../assets/img/leaf.png'
import window from '../assets/img/window.png'
import umbrella from '../assets/img/umbrella.png'

export default {
  data() {
    return {
      selected_feature_index: 1,
      features: [
        like,
        work,
        leaf,
        window,
        umbrella,
      ]
    }
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context('../assets/', false, /\.png$/)
      return images('./' + pet + ".png")
    }
  }
}
</script>