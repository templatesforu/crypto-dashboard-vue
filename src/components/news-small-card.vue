<template>
  <div class="news-small-card-container">
    <img :alt="image_alt" :src="image_src" class="news-small-card-image" />
    <div class="news-small-card-card-body">
      <span class="news-small-card-category">{{ smoll_text }}</span>
      <span class="news-small-card-title">{{ text }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NewsSmallCard',
  props: {
    text: {
      type: String,
      default: "CoinDesk TV's Coverage of Consensus 2021",
    },
    image_src: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1519162584292-56dfc9eb5db4?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb&w=1000',
    },
    image_alt: {
      type: String,
      default: 'image',
    },
    smoll_text: {
      type: String,
      default: 'Consensus 2021',
    },
  },
}
</script>

<style scoped>
.news-small-card-container {
  width: 300px;
  margin: var(--dl-space-space-halfunit);
  display: flex;
  padding: var(--dl-space-space-halfunit);
  position: relative;
  align-items: flex-start;
  border-radius: var(--dl-radius-radius-radius8);
  flex-direction: row;
  background-color: var(--dl-color-gray-400);
}
.news-small-card-image {
  width: 64px;
  height: 64px;
  object-fit: cover;
  margin-right: 0px;
  border-radius: 16px;
}
.news-small-card-card-body {
  width: 100%;
  display: flex;
  margin-left: var(--dl-space-space-halfunit);
  padding-right: var(--dl-space-space-halfunit);
  flex-direction: column;
}
.news-small-card-category {
  color: var(--dl-color-gray-600);
  font-size: 12px;
  font-family: Roboto;
}
.news-small-card-title {
  color: var(--dl-color-gray-white);
  width: 100%;
  font-size: 14px;
  font-family: Roboto;
}
</style>
