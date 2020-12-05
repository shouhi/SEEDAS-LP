<template lang="pug">
  header.header
    div.header-wrapper
      div.container
        div.row
          div(class="col col--1")
            div.logo
              img(src="@/assets/imgs/logo.png" alt="" width="100")
          div(class="col col--11 nav-panel")
              ul.nav-list
                li
                  a(href="#home") ホーム
                li
                  a(href="#about") サービス詳細
                li
                  a(href="#strong") SEEDASの強み
                li
                  a(href="#owner") 店舗を貸したいオーナーの皆様へ
                li
                  a(href="#student") 学生のみなさまへ
                li
                  a(href="#store") 現在貸出中店舗
                li
                  a(href="#vision") 将来ビジョン
</template>

<script>
import smoothscroll from 'smoothscroll-polyfill'

export default {
  mounted() {
    const self = this
    smoothscroll.polyfill()
    self.$el.querySelectorAll('a[href^="#"]').forEach(function(el) {
      el.addEventListener('click', event => {
        event.preventDefault()
        const href = el.getAttribute('href')
        const target = document.querySelector(
          href === '#' || href === '' ? 'html' : href
        )
        target.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        })
      })
    })
  }
}
</script>

<style lang="scss" scoped>
.header {
  position: absolute;
  z-index: 9999;
  width: 100%;
  top: 0;
  left: 0;
  height: 100px;
  @include tablet {
    height: 200px;
  }
}

.header-wrapper {
  position: sticky;
  top: 38px;
}

.nav-panel {
  position: fixed;
  top: 0;
  left: -100vw;
  max-width: 100vw;
  height: 150vh;
  padding-top: 20px;
  overflow-x: hidden;
  background: rgba(255, 255, 255, 0.95);
  transition: all 0.2s ease;
  @include pc {
    position: static;
    padding-top: 0;
    background: none;
    max-width: auto;
    height: auto;
  }
  &.open {
    transform: translateX(100vw);
    @include pc {
      transform: none;
    }
  }
}

.nav-list {
  display: flex;
  flex-wrap: wrap;
  font-size: 18px;
  @include pc {
    justify-content: flex-end;
    font-size: 12px;
  }
  & > * {
    padding: 13px 25px;
    width: 100%;
    border-bottom: 1px solid silver;
    line-height: 2;

    @include pc {
      margin: 0 12px;
      padding: 0;
      width: auto;
      border: none;
    }
  }
  a {
    display: block;

    color: $colCaption;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-decoration: none;
    text-transform: uppercase;
    &:link,
    &:visited {
      color: $colCaption;
    }
    &:hover {
      color: $colHighlight;
    }
    @include pc {
      display: inline;
    }
  }
}

.close-button {
  text-align: right;
  font-size: 36px;
  line-height: 1;
  cursor: pointer;
  @include pc {
    display: none;
  }
}
</style>
