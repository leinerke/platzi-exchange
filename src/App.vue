<template>
  <main>
    <px-header :links="links" />
    <router-view class="container px-5 sm:p-20 flex justify-center" />
  </main>
</template>

<script>
import PxHeader from '@/components/PxHeader';

export default {
  name: 'App',
  data() {
    return {
      links: [
        { title: 'BTC', to: { name: 'coin-detail', params: { id: 'bitcoin' } } },
        { title: 'ETH', to: { name: 'coin-detail', params: { id: 'ethereum' } } },
        { title: 'BNB', to: { name: 'coin-detail', params: { id: 'binance-coin' } } },
      ],
    };
  },
  components: {
    PxHeader,
  },
};
</script>

<style>
</style>
