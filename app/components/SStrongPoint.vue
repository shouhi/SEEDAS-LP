<template lang="pug">
  div#strong
    div.strong-wrapper
      div.container
        div.row
          div(class="col col--6")
            my-section-title
              template(v-slot:heading) SEEDASの強み
            div.strong
              my-gauge.gauge(caption="cost" :value="80")
              my-gauge.gauge(caption="easy" :value="90")
              my-gauge.gauge(caption="marketing" :value="75")
          div(class="col col--6")
</template>

<script>
import MySectionTitle from '@/components/SectionTitle'
import MyGauge from '@/components/Gauge'

export default {
  components: {
    MySectionTitle,
    MyGauge
  }
}
</script>

<style lang="scss" scoped>
.strong-wrapper {
  background: #f9f9f9;
  padding: 50px 0 80px;
  @include tablet {
    background-image: url('../assets/imgs/skills.jpg');
    background-repeat: no-repeat;
    background-size: contain;
    background-position: right;
  }
}

/deep/ .heading {
  padding: 0;
  text-align: center;
  @include pc {
    text-align: left;
    padding-top: 120px;
  }
}

.strong {
  padding: 0 20px;
  @include pc {
    padding: 0 86px 70px 0;
  }
}

.gauge {
  margin-top: 40px;
}
</style>
