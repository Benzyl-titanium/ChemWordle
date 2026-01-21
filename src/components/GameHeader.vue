<template>
  <div
    class="flex justify-between items-center w-full mb-5 px-4 py-2 box-border bg-red-500 rounded"
  >
    <h4 class="text-gray-800 m-0 font-bold">猜无机化合物游戏</h4>
    <div class="flex items-center gap-2">
      <button
        @click="$emit('toggle-dark')"
        class="toggle-dark-btn flex items-center p-0 m-0 mt-2 bg-transparent border-none shadow-none focus:outline-none"
      >
        <i :class="['fa-solid', isDark ? 'fa-sun' : 'fa-moon', 'w-6', 'h-6']"></i>
      </button>
      <a
        href="https://github.com/Benzyl-titanium/ChemWordle"
        target="_blank"
        rel="noopener noreferrer"
        class="github-link flex items-center p-0 m-0 mt-2 bg-transparent border-none shadow-none focus:outline-none"
      >
        <i class="fa-brands fa-github w-6 h-6"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    isDark: {
      type: Boolean,
      required: true,
    },
  },
}
</script>

<style scoped>
:root .github-link:hover i.fa-github,
:root .toggle-dark-btn:hover i.fa-sun,
:root .toggle-dark-btn:hover i.fa-moon {
  color: #fff !important;
}
.dark .github-link:hover i.fa-github,
.dark .toggle-dark-btn:hover i.fa-sun,
.dark .toggle-dark-btn:hover i.fa-moon {
  color: #111 !important;
}
</style>
