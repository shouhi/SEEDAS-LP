<template lang="pug">
  div#store.clients
    div.container
      div.row
        div(class="col col--1-5")
          figure.logo
            img(
              src="@/assets/imgs/client1.jpeg"
              alt="HANA"
              width="250px"
            )
        div(class="col col--1-5")
          figure.logo
            img(
              src="@/assets/imgs/client2.jpeg"
              alt="MAGIE"
              width="120px"
            )
        div(class="col col--1-5")
          figure.logo
            img(
              src="@/assets/imgs/client3.jpeg"
              alt="KAZE"
              width="120px"
            )
</template>

<style lang="scss" scoped>
.clients {
  padding: 54px;
}

.row {
  justify-content: space-around;
}

.logo {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  padding: 20px 0;
  @include pc {
    padding: 10px 0;
  }
  img:hover {
    transform: scale(1.2, 1.2);
  }
}
</style>
