<template>
    <main class="no-page">
        <MainHeader></MainHeader>
        <div class="no-container">
            <router-link to="/" tag="button" class="back-button">
                <i class='bx bx-left-arrow-alt bk-icon'></i>
                <span class="button-text">Go Back</span>
            </router-link>
        </div>
    </main>
</template>

<script>
import MainHeader from '@/components/MainHeader.vue'

export default {
  name: 'Home',
  components: {
    MainHeader
  }
}
</script>

<style lang="less">
    .no-page {
        width: 100%;
        height: 100%;
    }
    .no-container {
        position: relative;
        min-height: 88vh;
        display: flex;
        align-items: center;
        justify-content: center;
        .back-button {
            font-family: 'Kanit', Sans-Serif;
            text-decoration: none;
            color: #333;
            font-weight: 600;
            font-size: 68px;
            display: flex;
            align-items: center;
            i {
                display: none;
                transition: all .4s ease-in-out;
            }
            &:hover i {
                display: inline;
            }
        }
    }
</style>