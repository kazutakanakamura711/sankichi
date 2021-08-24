<template>
<v-app>

<div>
  <HomeSlide/>
  <HomeCalendar
  class="calendar"
  />
  <HomeBusinessHours
  class="hours"
  />
  <HomeContent
  :contentTitleImg="contentTitles[0].img"
  :contentTitleH1="contentTitles[0].h1Text"
  :contentTitleH4="contentTitles[0].h4Text"

  />
  <HomeMessage
  class="msg"
  />
  <!-- <Link
  :titleName="titleNameConcept"
  :linkDestination="linkDestinationConcept"
  class="link"
  /> -->
  <HomeContent
  :contentTitleImg="contentTitles[1].img"
  :contentTitleH1="contentTitles[1].h1Text"
  :contentTitleH4="contentTitles[1].h4Text"
  />
  <Link
  :titleName="titleNameMenu"
  :linkDestination="linkDestinationMenu"
  class="link"
  />
  <HomeContent
  id="a"
  :contentTitleImg="contentTitles[2].img"
  :contentTitleH1="contentTitles[2].h1Text"
  :contentTitleH4="contentTitles[2].h4Text"
  />
  <HomeAddressMap
  class="addressMap"
  />
  <HomeLogo
  class="logo"
  />

</div>
</v-app>
</template>
<script>
export default {
  layout: 'home',
  data() {
    return {
      titleNameMenu: 'MENU',
      titleNameConcept: 'CONCEPT',
      linkDestinationMenu: '/Menu',
      linkDestinationConcept: '/Concept',
      contentTitles: [
        {
          img: 'images/_DSC1743.jpg', h1Text: 'CONCEPT', h4Text: '癒やし懐かし「昭和」の空間',
        },
        {
          img: 'images/_DSC1678.jpg', h1Text: 'MENU', h4Text: '瀬戸内の新鮮な素材',
        },
        {
          img: 'images/_DSC1740.jpg', h1Text: 'ACCESS', h4Text: '活気溢れる松山の中心地',
        },
      ]

    }
  },
}
</script>
<style lang="css">
  .calendar {
    margin: 10%;
  }
  .hours,
  .address {
    font-size: 88%;
  }
  .addressMap {
    margin: 10%;
  }
  .logo {
    margin: 10% auto;
    width: 100px;
  }
  .link {
      font-size: 50%;
  }
  .v-parallax__image {
    margin: 0px;
  }
  .msg {
    margin: 10%;
  }
  @media (min-width: 600px){
    .logo {
      width: 200px;
    }
    .link {
      font-size: 100%;
    }
  }
</style>