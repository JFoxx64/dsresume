<template>
  <div class="professionalview">
    <ResumePrintButton :hackermode="hackermode"/>
    <SimpleIntro :hackermode="hackermode"/>
    <ProfessionalExperience :hackermode="hackermode"/>
    <PortfolioInfo :hackermode="hackermode"/>
  </div>
</template>

<script>
import ResumePrintButton from '../components/ResumePrintButton.vue'
import SimpleIntro from '../components/SimpleIntro.vue'
import ProfessionalExperience from '../components/ProfessionalExperience.vue'
import PortfolioInfo from '../components/PortfolioInfo.vue'

export default {
  name: 'ProfessionalView',
  props:{
    hackermode : Boolean
  },
  components : {
    ResumePrintButton,
    SimpleIntro,
    ProfessionalExperience,
    PortfolioInfo
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
