<template>
  <article>
    <div class="flex-row flex-left breadcrumb">
      <p>Accueil</p>
      <p>/</p>
      <p>Maquillage-Teint</p>
      <p>/</p>
      <p>Tarte nous offre une version ultra creamy du shape tape !</p>
    </div>
    <section class="content">
      <p class="tags">Nouveau , tendance , maquillage - maquillage - teint</p>

      <BaseHeader html-type="h1">
        Armani nous offre une version longue tenue du mascara !</BaseHeader
      >

      <BaseHeader html-type="h2">
        Volumateur et allongeant, le mascara Eyes to kill arme plus que jamais
        le regard d'une intensité détonnante. En un seul coup de maître, obtenez
        un volume aérien, un allongement extrême et une définition considérable,
        avec un résultat longue tenue</BaseHeader
      >

      <div class="flex-column">
        <img src="~/assets/img/shape-tape-2.jpg" alt="shape tape" width="800" />
        <BaseHeader html-type="h3"
          >ARMANY EYES TO KILL : LE MASCARA QUI DONNE DES CILS SUPER VOLUMINEUX
          SANS EFFET PAQUET !</BaseHeader
        >
      </div>

      <BaseParagraph
        >Le mascara Eyes to Kill de Giorgio Armani révèle l'intensité de votre
        regard en un coup de maître. Grâce à sa brosse unique et à sa texture
        fluide,ce mascara galbe,donne du volume et allonge chaque cil sans pour
        un volume longue tenue. Fluide et légère,la texture issue de la
        technologie Micro-fil™ Giorgio Armani enrobe les cils tout en
        légèreté,pour les étirer et les allonger à l'infini. Le résultat est
        aérien,"ce mascara n'alourdit pas les cils et se fait oublier. La
        matière chargée sur la brosse ""lash liner"" est déposée sur les cils en
        un seul passage. L'application modulable vous permet d'obtenir un
        résultat sur mesure",en un ou plusieurs coups de brosse.</BaseParagraph
      >

      <BaseParagraph>
        Un volume et un allongement intense qui dure 24 heures,vous en
        réviez,Giorgio Armani l'a fait pour vous grâce à son meilleur mascara.
        Eyes to Kill déploie votre regard intensément,avec une définition proche
        de la perfection. Les cils sont séparés,domptés un à un par la brosse
        qui les allonge et les étire intensément,en un geste maîtrisé. La
        formule volumisante étoffe les cils,tout en vous offrant une extension
        haute définition. Le regard est ainsi intensifié,il paraît plus
        grand,plus profond,encore plus mystérieux.
      </BaseParagraph>

      <div class="flex-column">
        <img src="~/assets/img/Tarte_collection.jpg" alt="tarte collection" />
        <BaseHeader html-type="h3"
          >ELLES AIMENT LE MASCARA ARMANI EYES TO KILL !</BaseHeader
        >
      </div>

      <BaseParagraph
        >Vous savez tout sur Eyes to kill, le mascara Armani ! Pour ne rien
        rater de nos autres nouveautés, rendez-vous sur notre chaine
        <span>Youtube</span> et notre <span>page Facebook</span>.</BaseParagraph
      >
    </section>
  </article>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import BaseHeader from '~/components/Atoms/Typography/Header/BaseHeader.vue'
import BaseParagraph from '~/components/Atoms/Typography/Paragraph/BaseParagraph.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    BaseHeader,
    BaseParagraph,
  },
})
</script>

<style scoped>
article > div.flex-row.flex-left.breadcrumb > p {
  margin: 0 12px;
  color: rgb(151, 151, 151);
  font-weight: 700;
  font-size: 1rem;
  border: 0;
}

article > section.content {
  margin-left: 8%;
}

article > section.content > p.tags {
  color: #d7002c;
  font-size: 1.2rem;
  text-transform: uppercase;
  line-height: 1.4rem;
  margin-top: 10px;
  margin-bottom: 24px;
  letter-spacing: 3px;
}

article > section.content > ul {
  margin-left: 48px;
  font-size: 18px;
  font-weight: 400;
  line-height: 32.4px;
  list-style-type: disc;
}

article > section.content > p > span {
  color: #d7002c;
}

@media only screen and (max-width: 1024px) {
  article > div.breadcrumb {
    display: none;
  }
}
</style>
