<template>
  <div class="feedback">
    <div class="container feedback__container">
      <h1 class="title feedback__title">What people say about us</h1>
      <img src="../assets/img/round_168.png" alt="" class="feedback__photo">
      <p class="feedback__text">“ It’s official – I love this app, I couldn’t be without it now.”</p>
      <p class="feedback__author">- Ron Burgundy</p>
      <div class="feedback__selector-block">
        <div @click="selected_feedback = 0" class="feedback__selector" :class="selected_feedback === 0 ? 'feedback__selector_active': ''"></div>
        <div @click="selected_feedback = 1" class="feedback__selector" :class="selected_feedback === 1 ? 'feedback__selector_active': ''"></div>
        <div @click="selected_feedback = 2" class="feedback__selector" :class="selected_feedback === 2 ? 'feedback__selector_active': ''"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected_feedback: 0
    }
  }
}
</script>