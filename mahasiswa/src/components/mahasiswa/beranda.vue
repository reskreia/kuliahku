<template>
  <div class="layout-padding page-showcase">
    <div class="showcase-top text-center">
      <img src="~assets/logo-usm.png" style="height: 180px; width: 156px;" />
      <h6 class="caption">
        Sistem Monitoring Akademik
        <br>
        Universitas Semarang
      </h6>
    </div>

    <div class="row justify-center">
      <div style="width: 850px; max-width: 90vw;" class="row">
        <div class="col-xs-6 col-sm-4 col-lg-3">
          <div class="card text-center category-link text-orange" @click="goTo('/pedomankrs/mPedoman')">
            <q-icon name="info_outline" />
            <p class="caption">Pedoman KRS</p>
          </div>
        </div>
        <div class="col-xs-6 col-sm-4 col-lg-3">
          <div class="card text-center category-link text-light-blue" @click="goTo('/master/inputSMS')">
            <q-icon name="layers" />
            <p class="caption">Master Data</p>
          </div>          
        </div>
        <div class="col-xs-6 col-sm-4 col-lg-3">
          <div class="card text-center category-link text-teal" @click="goTo('/mkrs/dashKRS')">
            <q-icon name="local_library" />
            <p class="caption">Menu KRS</p>
          </div>          
        </div>
        <div class="col-xs-6 col-sm-4 col-lg-3">
          <div class="card text-center category-link text-indigo" @click="goTo('/mkhs/dashKHS')">
            <q-icon name="bubble_chart" />
            <p class="caption">Menu KHS</p>
          </div>          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { QList, QItem, QItemMain, QItemTile, QIcon, QFixedPosition, QAlert, QBtn } from 'quasar'

export default{
  components: { QList, QItem, QItemMain, QItemTile, QIcon, QFixedPosition, QAlert, QBtn },
  methods: {
    goTo (link) {
      this.$router.push(link)
    }
  }
}
</script>

<style lang="stylus">
.page-showcase
.layout-padding {
  padding 0.5rem 0.5rem
}
  .showcase-top
    margin-bottom 24px
    .q-alert
      max-width 500px
  .card
    cursor pointer
    position relative
    padding 15px

    .q-icon
      font-size 56px
    p
      color rgba(0, 0, 0, .87)
      margin 15px 0 0 0 !important
    &:before
      content ''
      position absolute
      top 0
      right 0
      bottom 0
      left 0
      border-radius 2px
      opacity 0
      transition opacity .2s
      background currentColor
    &:hover:before
      opacity .4
</style>
