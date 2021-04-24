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
        Tarte nous offre une version ultra creamy du shape tape !</BaseHeader
      >

      <BaseHeader html-type="h2"
        >Vous aimez le classique Shape Tape™ de Tarte, cet anticernes mat,
        agréable à appliquer et redoutable pour cacher nos cernes et illuminer
        notre regard ? Vous allez adorer sa nouvelle version Shape Tape™ Ultra
        Creamy : une formule crémeuse capable d’hydrater et lisser la peau.
        Attention les yeux !</BaseHeader
      >

      <div class="flex-column">
        <img src="~/assets/img/shape-tape-2.jpg" alt="shape tape" />
        <BaseHeader html-type="h3"
          >SHAPE TAPE™ ULTRA CREAMY : L’ANTICERNES QUI APPORTE 24H D’HYDRATATION
          !</BaseHeader
        >
      </div>

      <BaseParagraph
        >Shape Tape™ Ultra Creamy de Tarte présente les mêmes atouts que son
        Shape Tape™ classique : une couvrance totale, ultra facile à s’estomper,
        qui illumine la peau en dissimulant les cernes, les rougeurs et autres
        imperfections. Comme lui, il ne file pas, ne s’écaille
        pas...</BaseParagraph
      >

      <BaseParagraph>
        Ce qui le distingue ? Sa formule pour commencer : elle intègre une
        hydratation 24h (cliniquement prouvée !). Sa texture pour continuer :
        elle se révèle divinement crémeuse. Quelle que soit la couleur parmi les
        18 teintes disponibles, le fini est toujours aussi mat et naturel mais
        il est encore plus confortable, surtout quand on a la peau sèche ou des
        rides et ridules à camoufler : Shape Tape™ Ultra Creamy est sans effet
        masque, ni pli. La peau est fraîche, lumineuse, ultra liftée et lissée.
        Bluffant !
      </BaseParagraph>

      <BaseHeader html-type="h3"
        >SHAPE TAPE™ ULTRA CREAMY : UN MÉLANGE D’INGRÉDIENTS
        NATURELS</BaseHeader
      >

      <BaseParagraph
        >Comme à son habitude, Tarte est allée puisée dans les ingrédients
        d’origine naturelle pour concevoir ce correcteur à la fois make-up et
        soin. On retrouve :</BaseParagraph
      >

      <ul>
        <li>La figue de barbarie, un incroyable antioxydant et hydratant.</li>
        <li>
          La racine de réglisse. Un des secrets du Shape Tape™ classique pour
          illuminer.
        </li>
        <li>
          La mangue, l’avocat et le beurre de karité. Eux aussi sont déjà
          présents dans la version originale. Mais on ne s’en passe pas pour
          hydrater et nourrir !
        </li>
        <li>
          L’acide hyaluronique et l’hyaluronane de sodium qui hydratent, lissent
          et liftent l’apparence de la peau.
        </li>
        <li>La cétone de framboise pour donner un effet repulpé.</li>
        <li>
          Un mélange de vegan squalène et ginseng qui aide à rendre la peau plus
          ferme et rebondie mais aussi à minimiser l’apparence des rides et
          ridules, sans plis... pendant 12 heures !
        </li>
      </ul>

      <BaseParagraph
        >Et bien sûr, comme tous les produits Tarte, le Shape Tape™ Ultra Creamy
        est formulé sans huiles minérales, phtalates, triclosan, sulfate de
        laurier de sodium et gluten. Ça fait du bien...</BaseParagraph
      >

      <div class="flex-column">
        <img src="~/assets/img/Tarte_collection.jpg" alt="tarte collection" />
        <BaseHeader html-type="h3"
          >ELLES AIMENT LE SHAPE TAPE™ ULTRA CREAMY !</BaseHeader
        >
      </div>

      <BaseParagraph
        >Le mieux est de donner la parole à celles qui l’ont essayé. Suite à une
        étude, 100% des participants ont confirmé que Shape Tape™ Ultra Creamy
        :</BaseParagraph
      >

      <ul>
        <li>Rend la peau plus lisse (y compris le contour des yeux !).</li>
        <li>N’assèche pas la peau et ne laisse pas un effet masque.</li>
        <li>Couvre les imperfections et les cernes.</li>
        <li>Apporte un éclat naturel.</li>
      </ul>

      <BaseParagraph
        >On a gardé le meilleur pour la fin : il donne un regard éclatant comme
        après une bonne nuit de sommeil !</BaseParagraph
      >
      <BaseParagraph
        >Vous savez tout sur Tarte, le Shape Tape™ Ultra Creamy ! Pour ne rien
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
</style>
