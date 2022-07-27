<template>
  <the-tweet v-for="tweet in tweets" :key="tweet.id" :tweet="tweet"></the-tweet>
</template>

<script>
import { ref } from "vue";
import vweets from "../vweets";
import TheTweet from "@/components/TheTweet.vue";

export default {
  components: { TheTweet },
  setup() {
    const tweets = ref(vweets);

    return {
      tweets,
      TheTweet,
    };
  },
};
</script>
