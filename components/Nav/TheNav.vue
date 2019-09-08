<template>
  <div class="nav container">
    <div class="row">
      <div class="nav-desktop">
        <div class="nav-left">
          <a href="/">
            <Logo class="logo" />
          </a>
        </div>
        <div class="nav-right">
          <a
            href="#home"
            class="nav-right-item"
          >
            Home
          </a>
          <a
            href="#features"
            class="nav-right-item"
          >
            Feature
          </a>
          <button class="btn btn--small primary">
            <a
              href=""
              target="_blank"
            >
              Download
            </a>
          </button>
        </div>
      </div>
      <div class="nav-mobile ">
        <div class="nav-left">
          <a href="/">
            <Logo class="logo" />
          </a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import Logo from '../Icon/logo'
export default {
  components: {
    Logo
  }
};
</script>

<style lang="scss" scoped>
.nav {
  position: relative;
  .nav-desktop {
    height: 100px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    display: none;
    position: absolute;
    .nav-left {
      display: flex;
      align-items: center;
      .logo {
        height: 50px;
      }
    }

    .nav-right {
      display: flex;
      align-items: center;
      a {
        margin-right: 48px;
        font-weight: 700;
        font-size: 18px;
        color: $black80;
        transition: color 0.3s ease;

        &:hover {
          color: $primary50;
        }

        @include media(md) {
          margin-right: 96px;
        }
      }
      .btn {
        a {
          color: white;
          margin-right: 0;
        }
      }
    }

    @include media(sm) {
      display: flex;
    }
  }

  .nav-mobile {
    height: 60px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    position: fixed;
    top: 0;
    left: 0;
    border-bottom: 1px solid $black10;
    background: white;
    z-index: 10;

    .nav-left {
      display: flex;
      align-items: center;
      .logo {
        height: 40px;
      }
    }

    @include media(sm) {
      display: none;
    }
  }
}
</style>