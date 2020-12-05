<template lang="pug">
  div#about.about
    div(class="container container--narrow")
      my-section-title.title
        template(v-slot:heading) 🌱SEEDASのビジネスモデルについて
        template(v-slot:body)
          p.subtitiles １，学生⇢店舗オーナーへのレント代より10%
          p.subtitiles ２，学生の売上より10%
      figure.model
        img(src="@/assets/imgs/model.jpg" alt="" width="500px")
</template>

<script>
import MySectionTitle from '@/components/SectionTitle'

export default {
  components: {
    MySectionTitle
  }
}
</script>

<style lang="scss" scoped>
.about {
  text-align: center;
  padding-bottom: 60px;
  @include tablet {
    padding-bottom: 100px;
  }
}

.title {
  max-width: 620px;
  margin: auto;
}

/deep/ .heading {
  color: #f19710;
  font-size: 38px;
  font-weight: 500;
  letter-spacing: 0.01em;
  line-height: 60px;
  @include tablet {
    padding-top: 60px;
    margin-left: 60px;
  }
  @include pc {
    padding-top: 92px;
    margin-left: 10px;
    margin-right: 0;
  }
}

.subtitiles {
  color: #1d1d1d;
  font-size: 17px;
  font-weight: 500;
}
</style>
