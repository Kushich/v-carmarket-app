<template>
  <div class="banner">
    <div class="banner-item">
      <div class="banner-content container">
        <h1>Welcome to Car Market</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod
        </p>
        <app-button url="/" options="round inline">Read More</app-button>
      </div>
    </div>
  </div>
</template>

<script>
import AppButton from '@/components/Button'
export default {
  components: {
    AppButton,
  },
}
</script>

<style lang="scss">
/* Banner */
.banner-item {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: linear-gradient(180deg, rgba(0,0,0,1) 0%, rgba(255,128,0,1) 50%, rgba(255,128,0,1) 100%)  no-repeat center;
  background-image: url('../assets/banner-bg.jpg');
  background-size: cover;
  background-position: bottom;
}
.banner-item:before {
  content: '';
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}
.banner-content {
  display: -webkit-flex;
  display: -moz-flex;
  display: -ms-flex;
  display: -o-flex;
  display: flex;
  flex-direction: column;
  position: absolute;
  right: 0;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  margin: 0 auto;
  justify-content: center;
  align-items: center;
  color: #fff;
  user-select: none;
}
.banner-content h1 {
  color: #fff;
  font-size: 70px;
  font-weight: 700;
  text-transform: uppercase;
  margin-bottom: 20px;
}
.banner-content p {
  color: #fff;
  font-size: 18px;
  font-weight: 400;
  opacity: 0.8;
  margin-bottom: 30px;
}

@media (max-width: 992px) {
  .banner-item {
    height: 75vh;
  }
  .banner-content h1 {
    font-size: 50px;
  }
}
@media (max-width: 768px) {
  .banner-item {
    height: 65vh;
  }
  .banner-content h1 {
    font-size: 25px;
  }
}
@media (max-width: 576px) {
  .banner-content h1 {
    font-size: 20px;
  }
  .banner-content p {
    text-align: center;
  }
}
</style>
