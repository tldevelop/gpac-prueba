<template>
  <div class="home">
    <MainHeader></MainHeader>
    <div class="main-section">
      <div class="video-container">
        <video src="https://gogpac.com/wp-content/uploads/2020/11/gpac-home-2020.mp4" autoplay muted loop playsinline></video>
      </div>
      <div class="main-content">
        <h1 class="main-title kanit">
          EMBRACE THE <span class="gpac-brand"><strong class="first-letter">g</strong>pac</span><br><span class="fw-900">DIGITAL RECRUITMENT <br> PLATFORM</span>
        </h1>
        <div class="buttons-container">
          <router-link to="/jobs" tag="button" class="home-button red-bg">FIND JOBS</router-link>
          <router-link to="/nopage" tag="button" class="home-button red-bg space-up">FIND TALENT</router-link>
          <router-link to="/nopage" tag="button" class="home-button red-bg space-up">BECOME A RECRUITER</router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import MainHeader from '@/components/MainHeader.vue'

export default {
  name: 'Home',
  components: {
    MainHeader
  }
}
</script>

<style lang="less">
  .red-bg {
    background-color: #D52028;
  }
  .video-container {
    pointer-events: none;
    position: absolute;
    overflow: hidden;
    height: 100%;
    width: 100%;
    z-index: -1;
    top: 0;
    left: 0;
  }
  .main-content {
    position: relative;
    min-height: 88vh;
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    align-items: center;
    justify-content: center;
    .main-title {
      color: #ffffff;
      font-family: 'Kanit', Sans-Serif;
      font-weight: 200;
      font-size: 68px;
      line-height: 0.9em;
    }
  }
  .fw-900 {
    font-weight: 900;
  }
  .gpac-brand {
    font-family: "swatchit", sans-serif;
    letter-spacing: 1px;
    display: inline-block;
    .first-letter {
      color: #D52028; 
    }
  }
  .buttons-container {
    width: 50%;
    display: flex;
    align-items: center;
    justify-content: space-around;
  }
  .home-button {
    color: #ffffff;
    text-decoration: none;
    font-family: 'Kanit', Sans-Serif;
    font-weight: 700;
    padding: 8px 48px;
    font-size: 24px;
    border-radius: 48px;
    transition: all .4s ease-in-out;
    &:hover {
      transform: scale(1.1);
    }
  }
  @media (max-width: 768px) {
    .space-up {
      margin-top: 24px;
    }
    .main-content {
      padding: 0 24px;
    }
    .main-title {
      font-size: 36px !important;
    }
    .buttons-container {
      flex-direction: column;
      width: 100%;
    }
    .home-button {
      width: 100%;
      padding: 8px 16px;
    }
  }
</style>
