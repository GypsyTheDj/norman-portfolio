<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    width="100%"
    height="100%"
    viewBox="0 0 24 24"
  >
    <g
      class="transition"
      fill="none"
      :stroke="themeColor"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <path d="M11 7H6a2 2 0 0 0-2 2v9a2 2 0 0 0 2 2h9a2 2 0 0 0 2-2v-5"></path>
      <path d="M10 14L20 4"></path>
      <path d="M15 4h5v5"></path>
    </g>
  </svg>
</template>

<script>
import { mapGetters } from 'vuex';

export default {
  name: 'ExternalLink',
  computed: {
    ...mapGetters({
      theme: 'theme'
    }),
    themeColor() {
      let color;

      if (!this.theme || this.theme === 'light') {
        color = '#6a727f';
      } else {
        color = '#9ca3af';
      }

      return color;
    }
  }
};
</script>
