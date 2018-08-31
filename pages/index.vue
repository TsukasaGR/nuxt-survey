<template>
  <section class="container">
    <div>
      <app-logo/>
      <h1 class="title">
        self-maintenance
      </h1>
      <h2 class="subtitle">
        自己点検システム
      </h2>
      <div class="links">
        <div :key="object.title" v-for="object in data.data">
          <nuxt-link :to="{ name: 'question-id', params: {id: object.id} }" tag="a" class="button--grey">{{ object.title }}</nuxt-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import data from '~/api/data.json'

export default {
  components: {
    AppLogo
  },
  data() {
    return {
      data: data
    }
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
  display: flex;
  justify-content: center;
}
</style>

