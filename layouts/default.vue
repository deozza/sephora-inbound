<template>
  <div class="layout">
    <section class="flex-column">
      <img src="~/assets/img/logo.svg" alt="logo sephora" />
      <div class="flex-row flex-around">
        <p>Maquillage</p>
        <p>Parfum</p>
        <p>Soin visage</p>
        <p>Corp & bain</p>
        <p>Cheveux</p>
        <p class="text-danger">Sephora collection</p>
        <p>Nouveautés</p>
        <p>Marques</p>
        <p>Bons plans</p>
        <p>Cadeaux</p>
        <p class="text-success">Good for</p>
      </div>
    </section>
    <section class="content">
      <Nuxt />
    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  name: 'DefaultLayoutVue',
})
</script>

<style scoped>
div.layout > section.flex-column > img {
  margin: 24px 0;
  width: 250px;
}

div.layout > section.flex-column > div.flex-row {
  width: 70%;
}

div.layout > section.flex-column > div.flex-row > p {
  text-transform: uppercase;
  font-size: 13px;
  font-weight: bold;
}

div.layout > section.flex-column > div.flex-row > p.text-danger {
  color: #d92282;
}

div.layout > section.flex-column > div.flex-row > p.text-success {
  color: #2a9941;
}

div.layout > section.content {
  min-height: calc(100vh - 72px);
  padding: 36px 23% 0 18%;
}

@media only screen and (max-width: 1024px) {
  div.layout > section.flex-column > div.flex-row {
    display: none;
  }

  div.layout > section.content {
    padding: 36px 6% 0 1%;
  }
}
</style>
