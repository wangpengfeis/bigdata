<template>
  <div class="app-container">
    <card1 class="box-card" />
    <card2 class="box-card" />
    <card3 class="box-card" />
  </div>
</template>

<script>
import card1 from './card1'
import card2 from './card2'
import card3 from './card3'
export default {
  components: { card1, card2, card3 },
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
.line{
  text-align: center;
}
.app-container{
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap:wrap;
  .box-card{
      width: 48%;
      margin-right: 2%;
  }
}
</style>

