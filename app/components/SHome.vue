<template lang="pug">
  div.home-wrapper
    div.container
      div#home.home-wrapper-2
        div.row
          div(class="col col--6")
          div(class="col col--")
            div.home
              my-section-title(:level="1" class="title")
                template(v-slot:heading) [ 学生と店舗のマッチングサービス ]
                template(v-slot:body)
                  p.subtitiles ~学生がお店経営を経験できる場を提供する~
                  p 「芽吹くための経験」というビジョンを持って、学生たちがリアルな経営を経験できることを目指しています
              a(href="#" class="button contact-us") Let's Movie
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
.home-wrapper {
  background-color: #fafafafa;
}
.home {
  padding: 54px 0 90px;
  @include tablet {
    padding: 100px 0 120px;
  }
  @include pc {
    padding: 132px 64px 160px 60px;
  }
}
/deep/ .heading {
  color: #1d1d1d;
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

/deep/ .body {
  background: rgba(255, 255, 255, 0.7);
  color: #666;
  font-size: 18px;
  letter-spacing: 0.005em;
  line-height: 28px;
  padding: 10px;
  @include pc {
    background: none;
    color: inherit;
    font-size: 16px;
    line-height: 28px;
    padding: 0;
  }
}
.subtitiles {
  color: #1d1d1d;
  font-size: 20px;
  font-weight: 500;
  line-height: 60px;
}

.contact-us {
  margin-top: 40px;
}
</style>
