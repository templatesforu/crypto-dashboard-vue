<template>
  <div class="coin-stats-container">
    <img :alt="image_alt" :src="image_src" class="coin-stats-image" />
    <div class="coin-stats-card-body">
      <span class="heading5 coin-stats-coin">{{ coin_name }}</span>
      <span class="heading4 coin-stats-price">{{ coin_price }}</span>
      <div class="coin-stats-stats">
        <svg viewBox="0 0 585.1428571428571 1024" class="coin-stats-icon">
          <path
            d="M585.143 402.286c0 9.714-4 18.857-10.857 25.714l-256 256c-6.857 6.857-16 10.857-25.714 10.857s-18.857-4-25.714-10.857l-256-256c-6.857-6.857-10.857-16-10.857-25.714 0-20 16.571-36.571 36.571-36.571h512c20 0 36.571 16.571 36.571 36.571z"
          ></path>
        </svg>
        <label class="coin-stats-text">{{ coin_stat }}</label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CoinStats',
  props: {
    coin_price: {
      type: String,
      default: '$1.39',
    },
    image_src: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1519162584292-56dfc9eb5db4?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1000',
    },
    coin_name: {
      type: String,
      default: 'Cardano',
    },
    coin_stat: {
      type: String,
      default: '-8.64%',
    },
    image_alt: {
      type: String,
      default: 'image',
    },
  },
}
</script>

<style scoped>
.coin-stats-container {
  width: 213px;
  display: flex;
  position: relative;
  margin-top: var(--dl-space-space-halfunit);
  align-items: flex-start;
  margin-left: var(--dl-space-space-halfunit);
  padding-top: var(--dl-space-space-unit);
  margin-right: var(--dl-space-space-halfunit);
  padding-left: var(--dl-space-space-halfunit);
  border-radius: 16px;
  margin-bottom: var(--dl-space-space-halfunit);
  padding-right: var(--dl-space-space-halfunit);
  flex-direction: row;
  padding-bottom: var(--dl-space-space-unit);
  background-color: var(--dl-color-gray-400);
}
.coin-stats-image {
  width: 32px;
  height: 32px;
  object-fit: cover;
  border-radius: var(--dl-radius-radius-round);
}
.coin-stats-card-body {
  flex: 0 0 auto;
  width: auto;
  height: auto;
  display: flex;
  align-items: flex-start;
  margin-left: var(--dl-space-space-halfunit);
  flex-direction: column;
}
.coin-stats-coin {
  color: var(--dl-color-gray-600);
}
.coin-stats-price {
  color: var(--dl-color-gray-white);
}
.coin-stats-stats {
  display: flex;
  position: relative;
  margin-top: var(--dl-space-space-halfunit);
  align-items: flex-start;
  padding-left: var(--dl-space-space-halfunit);
  border-radius: var(--dl-radius-radius-radius8);
  padding-right: var(--dl-space-space-halfunit);
  flex-direction: row;
  background-color: var(--dl-color-danger-700);
}
.coin-stats-icon {
  top: auto;
  fill: var(--dl-color-gray-white);
  left: 0px;
  width: 16px;
  bottom: 11px;
  height: 16px;
  margin: auto;
  align-self: center;
}
.coin-stats-text {
  color: var(--dl-color-gray-white);
  z-index: 100;
  font-size: 12px;
  align-self: center;
  font-family: Roboto;
  border-radius: var(--dl-radius-radius-radius8);
  background-color: var(--dl-color-danger-700);
}
</style>
