<template>
  <div class="home-page">
    <mcv-banner />
    <div class="container page">
      <div class="row">
        <div class="col-md-9">
          <mcv-feed-toggle />
          <mcv-feed :api-url="apiUrl"></mcv-feed>
        </div>
        <div class="col-md-3">
          <mcv-popular-tags />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import McvFeed from '@/components/Feed.vue';
import McvPopularTags from '@/components/PopularTags';
import McvBanner from '@/components/Banner';
import McvFeedToggle from '@/components/FeedToggle';
export default {
  name: 'McvYourFeed',
  components: {
    McvFeedToggle,
    McvBanner,
    McvPopularTags,
    McvFeed,
  },
  data() {
    return {
      apiUrl: '/articles/feed',
    };
  },
};
</script>
