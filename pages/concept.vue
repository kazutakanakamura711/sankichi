<template>
<div>

  <HomeContent
  :contentTitleImg="contentTitles[0].img"
  :contentTitleH1="contentTitles[0].h1Text"
  :contentTitleH4="contentTitles[0].h4Text"
  />
  <HomeContent
  :contentTitleImg="contentTitles[1].img"
  :contentTitleH1="contentTitles[1].h1Text"
  :contentTitleH4="contentTitles[1].h4Text"
  class="black"
  />
  <HomeContent
  :contentTitleImg="contentTitles[2].img"
  :contentTitleH1="contentTitles[2].h1Text"
  :contentTitleH4="contentTitles[2].h4Text"
  />
</div>
</template>

<script>
export default {
  data() {
    return {
      contentTitles: [
        {
          img: 'images/027.jpg', h1Text: '', h4Text: '瀬戸内の新鮮な素材',
        },
        {
          img: 'images/_DSC1690.jpg', h1Text: '', h4Text: 'どこか懐かしい昭和の香り',
        },
        {
          img: 'images/_DSC1740.jpg', h1Text: '', h4Text: '活気溢れる松山の中心地',
        },
      ]
    }
  }
}
</script>

<style>
  
</style>