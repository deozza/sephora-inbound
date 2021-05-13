<template>
  <div>
    <section class='form'>
      <div class='flex-column'>
        <BaseHeader html-type='h1'>Luxe, mode & beauté : quels risques pour ma santé ?</BaseHeader>
        <BaseParagraph>Les clefs pour rester belle en restant respectueuse de son corps</BaseParagraph>
        <BaseHeader html-type='h2'>Rendez-vous le 20 Mai de 18h30 à 20h!</BaseHeader>
      </div>
      <div class='flex-row flex-around'>
        <img src='~/assets/img/element5-digital-ceWgSMd8rvQ-unsplash.jpg' alt='webinar'>
        <form action=''>
          <ul>
            <BaseInput v-for="(input,index) in inputs" :key="index" :input="input"/>
          </ul>
          <div class='flex-column'>
            <BaseButton visual-type='success'>Je m'inscris !</BaseButton>
          </div>
        </form>
      </div>
    </section>
    <section class='info'>
      <div class='flex-column'>
        <div class='content'>
          <div class='flex-column'>
            <BaseHeader html-type='h2' visual-type='dark'>Au programme de cet événement : </BaseHeader>
          </div>
          <ol>
            <li>Les composants à bannir</li>
            <li>Les composants pour se rebooster</li>
            <li>Une routine saine pour un corps sain</li>
            <li>Quel budget ?</li>
          </ol>
        </div>

      </div>
    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import BaseHeader from '~/components/Atoms/Typography/Header/BaseHeader.vue'
import BaseParagraph from '~/components/Atoms/Typography/Paragraph/BaseParagraph.vue'
import BaseButton from '~/components/Atoms/Button/BaseButton.vue'
import BaseInput from '~/components/Atoms/Input/BaseInput.vue'
import BaseInputModele from '~/components/Atoms/Input/BaseInputModele'

export default defineComponent({
  name: 'IndexPage',
  layout: 'landing',
  components: {
    BaseHeader,
    BaseParagraph,
    BaseButton,
    BaseInput,
  },
  setup() {
    const nameInput: BaseInputModele = new BaseInputModele('text', 'name', 'name', 'Nom', true)
    const firstnameInput: BaseInputModele = new BaseInputModele('text', 'firstname', 'firstname', 'Prénom', true)
    const emailInput: BaseInputModele = new BaseInputModele('email', 'email', 'email', 'Email', true)
    const inputs = {
      name: nameInput,
      firstname: firstnameInput,
      email: emailInput,
    }

    return {
      inputs,
    }
  },
})
</script>

<style scoped>
section.form > div.flex-row {
  width: 100%;
}
section.form > div.flex-row > img,
section.form > div.flex-row > form{
  width: 50%;
}

section.info {
  background-color: black;
}

section.info > div.flex-column > div.content{
  width: 50%;
  color: white
}

section.info > div.flex-column > div.content > ol > li {
  margin: 12px 0;
  list-style: decimal;
}


</style>
