<template>
  <div
    id="features"
    class="section"
  >
    <div class="container">
      <div class="row mw-2 mx-auto flex-center pb-7">
        <h2 class="fw-700">
          Our Features
        </h2>
      </div>
      <div class="feature mt-7">
        <div class="phone-wrapper">
          <img
            src="/phone.png"
            alt="phone"
            class="phone"
          >
          <div class="slider">
            <Carousel
              v-for="(item, index) in featureImages"
              :data="item"
              :curr-index="activePanel"
              :dataId="index"
              :key="index"
            />
          </div>
        </div>
        <div class="feature-items">
          <div
            v-for="(item, index) in features"
            :key="index"
            class="item flex-center flex-column"
            @click="activePanel = index"
          >
            <div
              class="icon flex-center"
              :class="activePanel == index ? 'active': null"
            >
              <img :src="`/feature${index + 1}.svg`" />
            </div>
            <h4 class="title fw-700">{{item.title}}</h4>
            <p class="desc">{{item.desc}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Carousel from '@/components/UI/Carousel'
export default {
  components: {
    Carousel,
  },
  data () {
    return {
      activePanel: 0,
      featureImages: [
        '/img-feature1.jpg',
        '/img-feature2.jpg',
        '/img-feature3.jpg',
        '/img-feature4.jpg',
      ],
      features: [{
        icon: 'feature1',
        title: 'Collecting your mood daily',
        desc: 'By saving a little time to reflect on your daily mood would give a huge effect. Piara aims to be your right hand to  accompany your day and to illustrate your emotional state.',
      },
      {
        icon: 'feature2',
        title: 'Record your activities',
        desc: 'By recording your activities, analysis towards your habit helps create an understanding which kind of activities trigger your feeling of joy or sadness.',
      },
      {
        icon: 'feature3',
        title: 'Cute Companion',
        desc: 'Everyone loves a cute character, right? Piara got you. A cute character will increase your mood and elevate your feelings throughout the day.',
      },
      {
        icon: 'feature4',
        title: 'Invest in Yourself',
        desc: 'Find a pattern that increase your productivity and resolve your problem in the future by investing your time to introspecting yourself with your daily mood journal.',
      }],
    }
  },
}
</script>

<style lang="scss" scoped>
.section {
  background-color: #edeff2;
  .slider {
    height: 100%;
    overflow: hidden;
  }

  .feature {
    position: relative;

    .phone-wrapper {
      display: none;
      @include media(xl) {
        display: block;
      }
      .phone {
        position: absolute;
        width: 300px;
        left: 50%;
        transform: translate3d(-50%, -50%, 0);
        top: 50%;
      }
    }

    &-items {
      position: relative;
      min-height: 550px;
      display: flex;
      flex-wrap: wrap;

      .item {
        position: relative;
        max-width: 360px;
        text-align: center;
        cursor: pointer;
        margin: 0 auto;
        margin-bottom: 36px;

        @include media(xl) {
          position: absolute;
        }
        .icon {
          width: 70px;
          height: 70px;
          background-color: white;
          border-radius: 50%;
          margin-bottom: 24px;

          box-shadow: 0 5px 20px rgba(#5a99d4, 0.5);

          &.active {
            @include media(xl) {
              -webkit-animation: pulse 1.5s infinite;
            }
          }

          &:hover {
            -webkit-animation: none;
          }
          img {
            width: 36px;
          }
        }
        .title {
        }
        .desc {
        }
      }
      .item:nth-child(1) {
        top: 0;
        left: 0;
      }
      .item:nth-child(2) {
        top: 0;
        right: 0;
      }
      .item:nth-child(3) {
        bottom: 0;
        left: 0;
      }
      .item:nth-child(4) {
        bottom: 0;
        right: 0;
      }
    }
  }

  @-webkit-keyframes pulse {
    0% {
      transform: scale3d(0.9, 0.9, 1);
    }
    70% {
      transform: scale3d(1, 1, 1);
      box-shadow: 0 0 0 40px rgba(90, 153, 212, 0);
    }
    100% {
      transform: scale3d(0.9, 0.9, 1);
      box-shadow: 0 0 0 0 rgba(90, 153, 212, 0);
    }
  }
}
</style>