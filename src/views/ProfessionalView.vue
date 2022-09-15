<template>
  <div class="professionalview">
    <ResumePrintButton :hackermode="hackermode"/>
    <SimpleIntro :hackermode="hackermode"/>
    <SkillSet :hackermode="hackermode"/>
    <ProfessionalExperience :hackermode="hackermode"/>
    <PortfolioInfo :hackermode="hackermode"/>
  </div>
</template>

<script>
import ResumePrintButton from '../components/ResumePrintButton.vue'
import SimpleIntro from '../components/SimpleIntro.vue'
import ProfessionalExperience from '../components/ProfessionalExperience.vue'
import PortfolioInfo from '../components/PortfolioInfo.vue'
import SkillSet from '../components/SkillSet.vue'

export default {
  name: 'ProfessionalView',
  props:{
    hackermode : Boolean
  },
  components : {
    ResumePrintButton,
    SimpleIntro,
    ProfessionalExperience,
    PortfolioInfo,
    SkillSet
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
