<template>
  <section>
    <div class='flex-column'>
      <div class='flex-row flex-around'>
        <div class='flex-column'>
          <BaseHeader html-type='h1' visual-type='dark'>Tout connaitre des composants de nos derniers produits</BaseHeader>
          <BaseParagraph visual-type='dark'>30 pages pour vous guider dans votre prochain choix de cosmétiques</BaseParagraph>
          <BaseParagraph visual-type='dark'>et vous aider à vous faire belle sans nuire à votre santé</BaseParagraph>
        </div>
        <form action=''>
          <ul>
            <BaseInput v-for="(input,index) in inputs" :key="index" :input="input"/>
          </ul>
          <div class='flex-column'>
            <BaseButton visual-type='success'>Je le veux !</BaseButton>
          </div>
        </form>
      </div>


    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import BaseHeader from '~/components/Atoms/Typography/Header/BaseHeader.vue'
import BaseButton from '~/components/Atoms/Button/BaseButton.vue'
import BaseInput from '~/components/Atoms/Input/BaseInput.vue'
import BaseInputModele from '~/components/Atoms/Input/BaseInputModele'
import BaseParagraph from '~/components/Atoms/Typography/Paragraph/BaseParagraph.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    BaseHeader,
    BaseParagraph,
    BaseButton,
    BaseInput,
  },
  layout: 'landing',
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
section {
  height: calc(100vh - 72px);
  background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url("~/assets/img/laura-chouette-uedyzm50WTQ-unsplash.jpg") no-repeat center center fixed;
  background-size: cover;
  overflow: hidden;
  color: white;
}

section > div.flex-column {
  height: 100%;
}

section > div.flex-column > div.flex-row{
  width: 100%;
  height: 100%;
}

section > div.flex-column > div.flex-row > form,
section > div.flex-column > div.flex-row > div {
  width: 50%;
}

p {
  margin-bottom: 6px;
}

</style>
