<template>
  <section class="container">
    <h2 style="text-align: left; margin-bottom: 20px;">ダッシュボード</h2>
    <div class="box">
      <div class="box-header" style="background-color: #e62a76;">
        期限切れのタスク
      </div>
      <div class="box-body">
        <table class="table table-striped">
          <thead>
            <tr>
              <th>#</th>
              <th>期限</th>
              <th>年度</th>
              <th>設問</th>
            </tr>
          </thead>
          <tbody>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[1].id} }" tag="a">
                4
              </nuxt-link>
            </th>
            <td>2日前</td>
            <td>2018</td>
            <td>○○アンケート</td>
          </tr>
          </tbody>
        </table>
      </div>
    </div>
    <div class="box">
      <div class="box-header" style="background-color: #00a8b5;">
        回答済みのタスク
      </div>
      <div class="box-body">
        <table class="table table-striped">
          <thead>
          <tr>
            <th>#</th>
            <th>年度</th>
            <th>設問</th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">
                3
              </nuxt-link>
            </th>
            <td>2018</td>
            <td>××アンケート</td>
          </tr>
          </tbody>
        </table>
      </div>
    </div>
    <div class="box">
      <div class="box-header" style="background-color: #fbb901;">
        終了したタスク
      </div>
      <div class="box-body">
        <table class="table table-striped">
          <thead>
          <tr>
            <th>#</th>
            <th>年度</th>
            <th>設問</th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">
                2
              </nuxt-link>
            </th>
            <td>2017</td>
            <td>○○アンケート</td>
          </tr>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">
                1
              </nuxt-link>
            </th>
            <td>2017</td>
            <td>××アンケート</td>
          </tr>
          </tbody>
        </table>
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

<style lang="scss">
.container {
  margin-top: 60px;
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  text-align: center;
  @include mq() {
    padding: 40px 80px;
  }
  table {
    margin: 0;
  }
  .box {
    border: 1px solid $border-color;
    margin-bottom: 30px;
    width: 100%;
    .box-header {
      padding: 10px 5px;
      color: #fff;
    }
    .box-body {
    }
  }
}
</style>

