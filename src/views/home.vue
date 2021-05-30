<template>
  <div class="home-container">
    <div class="home-container1">
      <app-navbar></app-navbar>
      <div class="home-row">
        <div class="home-container2">
          <span class="heading2 home-text">Today&apos;s Cryptocurrency Prices by Market Cap</span>
          <div class="home-container3">
            <span class="heading5 home-text1">
              The Global crypto market cap is #1.55T.
              <span v-html="rawjj6t"></span>
            </span>
            <a
              href="https://example.com"
              target="_blank"
              rel="noreferrer noopener"
              class="heading5 thqLink home-read-more"
            >
              Read more
            </a>
          </div>
        </div>
        <div class="home-container4">
          <news-small-card
            image_src="https://images.unsplash.com/photo-1621501103258-3e135c8c1fda?ixlib=rb-1.2.1&amp;q=85&amp;fm=jpg&amp;crop=entropy&amp;cs=srgb&amp;h=1000"
          ></news-small-card>
          <news-small-card></news-small-card>
        </div>
      </div>
      <div class="home-row1">
        <div class="home-col-8">
          <iframe
            src="https://s.tradingview.com/widgetembed/?frameElementId=tradingview_56c2a&amp;symbol=BTCUSDT&amp;interval=D&amp;hidesidetoolbar=0&amp;symboledit=1&amp;saveimage=1&amp;toolbarbg=F1F3F6&amp;studies=%5B%5D&amp;hideideas=1&amp;theme=Dark&amp;style=1&amp;timezone=Etc%2FUTC&amp;studies_overrides=%7B%7D&amp;overrides=%7B%7D&amp;enabled_features=%5B%5D&amp;disabled_features=%5B%5D&amp;locale=en&amp;utm_source=coinmarketcap.com&amp;utm_medium=widget&amp;utm_campaign=chart&amp;utm_term=BTCUSDT"
            class="home-chart"
          ></iframe>
        </div>
        <div class="home-col-4">
          <coin-stats
            coin_name="Ethereum"
            image_src="https://images.unsplash.com/photo-1621501103258-3e135c8c1fda?ixlib=rb-1.2.1&amp;q=85&amp;fm=jpg&amp;crop=entropy&amp;cs=srgb&amp;h=1000"
          ></coin-stats>
          <coin-stats
            image_src="https://images.unsplash.com/photo-1617004890839-25d5d8a9730d?ixlib=rb-1.2.1&amp;q=85&amp;fm=jpg&amp;crop=entropy&amp;cs=srgb&amp;h=1000"
          ></coin-stats>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppNavbar from '../components/navbar'
import NewsSmallCard from '../components/news-small-card'
import CoinStats from '../components/coin-stats'

export default {
  name: 'Home',
  components: {
    AppNavbar,
    NewsSmallCard,
    CoinStats,
  },

  data() {
    return {
      rawjj6t: ' ',
    }
  },

  metaInfo: {
    title: 'crypto-dashboard',
    meta: [
      {
        property: 'og:title',
        content: 'crypto-dashboard',
      },
    ],
  },
}
</script>

<style scoped>
.home-container {
  width: 100%;
  height: auto;
  display: flex;
  min-height: 100vh;
  align-items: flex-start;
  flex-direction: column;
  background-color: var(--dl-color-gray-black);
}
.home-container1 {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  max-width: 1200px;
  align-self: center;
  align-items: flex-start;
  flex-direction: column;
  justify-content: flex-start;
}
.home-row {
  flex: 0 0 auto;
  width: 100%;
  display: flex;
  padding: var(--dl-space-space-unit);
  position: relative;
  align-items: flex-start;
  flex-direction: row;
  background-color: var(--dl-color-gray-300);
}
.home-container2 {
  display: flex;
  align-self: center;
  align-items: flex-start;
  flex-direction: column;
  justify-content: flex-start;
}
.home-text {
  color: var(--dl-color-gray-white);
  margin-top: 0px;
  margin-left: 0px;
}
.home-container3 {
  flex: 0 0 auto;
  width: 100%;
  height: auto;
  display: flex;
  align-items: flex-start;
  flex-direction: row;
  justify-content: flex-start;
}
.home-text1 {
  color: var(--dl-color-gray-600);
}
.home-read-more {
  color: var(--dl-color-gray-600);
  margin-left: var(--dl-space-space-halfunit);
}
.home-container4 {
  top: auto;
  left: auto;
  right: 68px;
  bottom: 16px;
  display: flex;
  margin-left: var(--dl-space-space-unit);
  flex-direction: row;
  justify-content: flex-end;
}
.home-row1 {
  width: 100%;
  display: flex;
  padding: var(--dl-space-space-unit);
  align-items: flex-start;
  flex-direction: row;
  justify-content: flex-start;
}
.home-col-8 {
  width: 66.66%;
  height: 500px;
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  justify-content: flex-start;
}
.home-chart {
  width: 100%;
  height: 100%;
}
.home-col-4 {
  width: 33.44%;
  display: flex;
  align-self: center;
  align-items: center;
  flex-direction: column;
  justify-content: flex-start;
}
</style>
