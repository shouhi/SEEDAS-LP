<template lang="pug">
  div#about.about
    div(class="container container--narrow")
      my-section-title.title
        template(v-slot:heading) 🌱SEEDASが提供するサービスとは
        template(v-slot:body)
          p.subtitiles １，既存の店舗の空き時間と自分で経営をしたい学生を繋ぐマッチングサービス
          button(@click="toBusinessModel") ビジネスモデルについて
      figure.signature
        img(src="@/assets/imgs/signature.png" alt="")
</template>

<script>
import MySectionTitle from '@/components/SectionTitle'

export default {
  components: {
    MySectionTitle
  },
  methods: {
    toBusinessModel() {
      this.$router.push('/business-model')
    }
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
.model {
  color: #f19710;
  font-size: 20px;
  font-weight: 300;
}

.signature {
  margin-top: 30px;
}
</style>
