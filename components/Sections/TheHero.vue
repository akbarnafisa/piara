<template>
  <div
    id="home"
    class="section-header container hero-section"
  >
    <div class="row align-items-center">
      <div class="col-md-6 ">
        <div class="text-wrapper ml-0 mr-lg-4">
          <h3 class="h2-md">
            Keep track of your daily activities to understand your emotions better
          </h3>
          <p class="mt-3">
            Piara is here to help you to gain better understanding of your emotional state
          </p>
          <div class="button-wrapper">
            <a
            href='https://play.google.com/store/apps/details?id=com.piara'
            target="_blank"
            class="mt-5"
            >
              <img 
                style="margin-right: 12px" 
                src="/download.png"
              />
            </a>
            <a 
              href="https://www.producthunt.com/posts/piara?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-piara"
              target="_blank"
            >
              <img 
                src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=167944&theme=light"
                alt="Piara - Privacy-First Mood Tracker | Product Hunt Embed"
                class="mt-2"
              />
            </a>
          </div>
          
          <!-- <button class="btn btn--medium primary mt-5">
            Join Us
          </button> -->
        </div>

      </div>
      <div class="col-md-6 ">
        <HeroImage class="mt-7 mt-md-0" />
      </div>
    </div>
  </div>
</template>

<script >
import HeroImage from '../Icon/hero'
export default {
  components: {
    HeroImage
  },

};
</script>

<style lang="scss" scoped>
.hero-section {
  min-height: calc(100vh - 100px);
  width: 100%;
  .button-wrapper {

    a {
      transition: transform 0.3s ease;
      height: 50px;
      cursor: pointer;
      display: inline-block;
      img {
        height: 100%;
      }
      &:hover {
        transform: scale(1.1);
      }
    }
  }
  h3 {
    font-weight: bold;
    line-height: 36px;
    letter-spacing: 0.5px;
    color: $black80;
    @include media(sm) {
      line-height: 48px;
      letter-spacing: 0.5px;
    }
  }
  p {
    letter-spacing: 0px;
    color: $black60;
    opacity: 0.8;
    @include media(sm) {
      line-height: 25px;
      letter-spacing: 0.1px;
    }
    @include media(lg) {
      line-height: 26px;
      letter-spacing: 0.2px;
    }
  }
  svg {
    width: 100%;
    height: 100%;
  }
}
</style>