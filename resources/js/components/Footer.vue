<template>
  <div class="footer-wrap tw-truncate">
    <footer
      class="tw-container tw-px-10 md:tw-px-48 lg:tw-px-80 tw-mt-5 tw-m-auto tw-text-center"
    >
      <div class="md:tw-flex md:tw-justify-center md:tw-text-xl">
        <div class="tw-font-bold md:tw-font-semibold tw-px-4">
          <router-link
            :to="{ name: 'home' }"
            class="tw-text-transparent-60 hover:tw-text-transparent-60"
          >
            דף הבית
          </router-link>
        </div>
        <div class="tw-font-bold md:tw-font-semibold tw-px-4">
          <router-link
            :to="{ name: 'home', hash: '#choose-a-test' }"
            class="tw-text-transparent-60 hover:tw-text-transparent-60"
          >
            מבחני תאוריה
          </router-link>
        </div>
        <div class="tw-font-bold md:tw-font-semibold tw-px-4">
          <router-link
            :to="{ name: 'about-us' }"
            class="tw-text-transparent-60 hover:tw-text-transparent-60"
          >
            אודות
          </router-link>
        </div>
        <div class="tw-font-bold md:tw-font-semibold tw-px-4">
          <router-link
            :to="{ name: 'privacy-policy' }"
            class="tw-text-transparent-60 hover:tw-text-transparent-60"
          >
            פרטיות
          </router-link>
        </div>
      </div>

      <div
        class="tw-border-t tw-border-solid tw-border-transparent-50 tw-py-4 tw-mt-4 md:tw-mt-8"
      >
        <div
          class="tw-text-transparent-60 tw-text-base md:tw-text-sm tw-text-center tw-font-semibold md:tw-font-bold"
        >
          © טסטלי {{ new Date().getFullYear() }}. כל הזכויות שמורות.
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "testly-footer"
};
</script>

<style scoped>
.footer-wrap {
  background: radial-gradient(
      circle at 1% 1%,
      var(--primary-color),
      rgb(220, 155, 0)
    )
    no-repeat 50%;
  background-size: auto;
}

.tw-text-transparent-60 {
  color: rgba(255, 255, 255, 0.6);
}

.hover\:tw-text-transparent-60:hover {
  color: white;
}

.tw-border-transparent-50 {
  border-color: rgba(255, 255, 255, 0.5);
}
</style>
