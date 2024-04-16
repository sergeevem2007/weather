<script setup lang="ts">
defineProps<{}>()
</script>

<template>
  <section class="main">
    <div class="container">
      <div class="main__wrapper">
        <div>
          <input type="search" name="" id="" class="main__search" placeholder="Enter the city">
          
          <h1 class="main__heading">San Francisco</h1>
          <div class="main__date-wrapper">
            <div class="main__date">Monday, May 23</div>
            <div class="main__update">Update As Of <span>2:45 PM</span></div>
          </div>

          <div class="main__sun-wrapper">
            <div class="main__sun-bg sun-bg" style="background-image: url(/public/sunrise.webp);">
              <div class="sun-bg__title">Sunrise</div>
              <div class="sun-bg__time">6:42 am</div>
            </div>
            <div class="main__sun-bg sun-bg" style="background-image: url(/public/sunset.webp);">
              <div class="sun-bg__title">Sunset</div>
              <div class="sun-bg__time">7:30 pm</div>
            </div>
          </div>
        </div>
        <div>
          <div class="main__wind-wrapper">
            <div class="wind-wrapper">
              <div class="wind-wrapper__img">
                <img src="/public/wind.svg" width="32" alt="">
              </div>
              <div class="wind-wrapper__text">Wind 3km/h</div>
            </div>
            <div class="wind-wrapper">
              <div class="wind-wrapper__img">
                <img src="/public/light-rain.svg" width="32" alt="">
              </div>
              <div class="wind-wrapper__text">Rain 78%</div>
            </div>
            <div class="wind-wrapper">
              <div class="wind-wrapper__img">
                <img src="/public/barometer.svg" width="32" alt="">
              </div>
              <div class="wind-wrapper__text">Pressure 761mmHg</div>
            </div>
            <div class="wind-wrapper">
              <div class="wind-wrapper__img">
                <img src="/public/humidity.svg" width="32" alt="">
              </div>
              <div class="wind-wrapper__text">Humidity 40%</div>
            </div>
          </div>
        </div>
        <div>
          <div class="main__card">
            <span class="card__day">Today</span>
            <div class="card__wrapper">
              <img src="/public/sun_cloud.webp" alt="">
              <span class="card__title">23<sup>℃</sup></span>
              <div class="card__subtitle">
                <span class="">23<sup>℃</sup></span>
                - 
                <span class="">31<sup>℃</sup></span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.main {
  padding: 60px 0;
}

.main__wrapper  {
  background-image: url(/main-bg.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  padding: var(--section-gap) 20px;
  border-radius: 20px;

  display: grid;
  grid-template-columns: 3fr 3fr 2fr;
  gap: 20px;
  align-items: flex-end;
}

.main__search {
  width: 100%;
  background-color: rgb(247 248 250 / 0.3);
  backdrop-filter: blur(20px);
  padding: 12px 20px;
  border-radius: 20px;
  border: none;
  font-size: 32px;
  font-weight: 500;
  color: var(--vt-c-white-soft);
}
.main__search:focus {
  outline: 4px solid rgb(118 104 229 / 0.3);
  box-shadow: 0px 0px 20px 5px rgb(118 104 229 / 0.5);
}
.main__search::placeholder {
  color: var(--vt-c-white-soft);
  opacity: 0.7;
}

.main__heading {
  font-weight: 700;
  font-size: 76px;
  line-height: 1.2;
  color: var(--vt-c-white-soft);
  margin-bottom: 8px;
}

.main__date-wrapper {
  display: flex;
  gap: 2rem;
  color: var(--vt-c-white-soft);
}

.main__sun-wrapper {
  display: flex;
  gap: 20px;
  margin-top: 60px;
}

.main__sun-bg {
  width: 200px;
  height: 200px;
  border-radius: 20px;
  padding: 30px 20px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
.sun-bg__title {
  font-weight: 500;
  font-size: 24px;
  color: var(--vt-c-white-soft);
  margin-bottom: 8px;
}
.sun-bg__time {
  font-weight: 600;
  font-size: 40px;
  color: var(--vt-c-white-soft);
}
.main__wind-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  border-radius: 20px;
  padding: 20px;
  background-color: rgb(247 248 250 / 0.3);
  backdrop-filter: blur(20px);
}
.wind-wrapper {
  display: flex;
  align-items: center;
  gap: 16px;
}
.wind-wrapper__img {
  background-color: var(--vt-c-secondary);
  border-radius: 10px;
  padding: 6px;
}
.wind-wrapper__text {
  font-weight: 400;
  font-size: 18px;
}
.main__card {
  min-height: 360px;
  padding: 20px;
  border-radius: 20px;
  background-color: rgb(118 104 229 / 0.3);
  backdrop-filter: blur(20px);
}
.card__day {
  line-height: 1;
  padding: 6px 12px;
  border-radius: 20px;
  color: var(--vt-c-white-soft);
  background-color: var(--vt-c-primary);
}
.card__wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}
.card__title {
  font-weight: 700;
  font-size: 76px;
  color: var(--vt-c-white-soft);
  margin: 16px 0;
}
.card__subtitle {
  font-weight: 500;
  font-size: 24px;
  color: var(--vt-c-white-soft);
}
</style>
