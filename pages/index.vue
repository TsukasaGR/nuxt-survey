<template>
  <section class="container">
    <h2 style="text-align: left; margin-bottom: 20px;">ダッシュボード</h2>
    <h3 style="text-align: left; margin-bottom: 20px;">設問一覧</h3>
    <div class="box">
      <div class="box-body">
        <table class="table table-striped">
          <thead>
          <tr style="background-color: #00a8b5; color: #fff;">
            <th>#</th>
            <th>年度</th>
            <th>設問</th>
            <th>ステータス</th>
            <th>回答/送信数</th>
            <th>作成日</th>
            <th>更新日</th>
            <th>期限</th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[1].id} }" tag="a">6</nuxt-link>
            </th>
            <td>2018</td>
            <td>日本語アンケートTypeB</td>
            <td>作成中</td>
            <td>-</td>
            <td>2018/06/13</td>
            <td>-</td>
            <td>-</td>
          </tr>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">5</nuxt-link>
            </th>
            <td>2018</td>
            <td>英語アンケートTypeB</td>
            <td>回収中</td>
            <td>95/100</td>
            <td>2018/01/15</td>
            <td>2018/02/01</td>
            <td>2018/03/01</td>
          </tr>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[1].id} }" tag="a">4</nuxt-link>
            </th>
            <td>2018</td>
            <td>日本語アンケート</td>
            <td>完了</td>
            <td>95/100</td>
            <td>2018/01/15</td>
            <td>2018/02/01</td>
            <td>2018/03/01</td>
          </tr>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">3</nuxt-link>
            </th>
            <td>2018</td>
            <td>英語アンケート</td>
            <td>完了</td>
            <td>90/100</td>
            <td>2018/01/18</td>
            <td>2018/02/02</td>
            <td>2018/03/01</td>
          </tr>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[1].id} }" tag="a">2</nuxt-link>
            </th>
            <td>2017</td>
            <td>日本語アンケート</td>
            <td>完了</td>
            <td>100/100</td>
            <td>2017/01/10</td>
            <td>-</td>
            <td>2017/03/01</td>
          </tr>
          <tr>
            <th scope="row">
              <nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">1</nuxt-link>
            </th>
            <td>2017</td>
            <td>英語アンケート</td>
            <td>完了</td>
            <td>98/100</td>
            <td>2017/01/08</td>
            <td>2017/02/04</td>
            <td>2017/03/01</td>
          </tr>
          </tbody>
        </table>
      </div>
    </div>
    <!--<div class="box">-->
      <!--<div class="box-header" style="background-color: #e62a76;">-->
        <!--期限切れのタスク-->
      <!--</div>-->
      <!--<div class="box-body">-->
        <!--<table class="table table-striped">-->
          <!--<thead>-->
            <!--<tr>-->
              <!--<th>#</th>-->
              <!--<th>期限</th>-->
              <!--<th>年度</th>-->
              <!--<th>設問</th>-->
            <!--</tr>-->
          <!--</thead>-->
          <!--<tbody>-->
          <!--<tr>-->
            <!--<th scope="row">-->
              <!--<nuxt-link :to="{ name: 'question-id', params: {id: data.data[1].id} }" tag="a">-->
                <!--4-->
              <!--</nuxt-link>-->
            <!--</th>-->
            <!--<td>2日前</td>-->
            <!--<td>2018</td>-->
            <!--<td>○○アンケート</td>-->
          <!--</tr>-->
          <!--</tbody>-->
        <!--</table>-->
      <!--</div>-->
    <!--</div>-->
    <!--<div class="box">-->
      <!--<div class="box-header" style="background-color: #00a8b5;">-->
        <!--回答済みのタスク-->
      <!--</div>-->
      <!--<div class="box-body">-->
        <!--<table class="table table-striped">-->
          <!--<thead>-->
          <!--<tr>-->
            <!--<th>#</th>-->
            <!--<th>年度</th>-->
            <!--<th>設問</th>-->
          <!--</tr>-->
          <!--</thead>-->
          <!--<tbody>-->
          <!--<tr>-->
            <!--<th scope="row">-->
              <!--<nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">-->
                <!--3-->
              <!--</nuxt-link>-->
            <!--</th>-->
            <!--<td>2018</td>-->
            <!--<td>××アンケート</td>-->
          <!--</tr>-->
          <!--</tbody>-->
        <!--</table>-->
      <!--</div>-->
    <!--</div>-->
    <!--<div class="box">-->
      <!--<div class="box-header" style="background-color: #fbb901;">-->
        <!--終了したタスク-->
      <!--</div>-->
      <!--<div class="box-body">-->
        <!--<table class="table table-striped">-->
          <!--<thead>-->
          <!--<tr>-->
            <!--<th>#</th>-->
            <!--<th>年度</th>-->
            <!--<th>設問</th>-->
          <!--</tr>-->
          <!--</thead>-->
          <!--<tbody>-->
          <!--<tr>-->
            <!--<th scope="row">-->
              <!--<nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">-->
                <!--2-->
              <!--</nuxt-link>-->
            <!--</th>-->
            <!--<td>2017</td>-->
            <!--<td>○○アンケート</td>-->
          <!--</tr>-->
          <!--<tr>-->
            <!--<th scope="row">-->
              <!--<nuxt-link :to="{ name: 'question-id', params: {id: data.data[0].id} }" tag="a">-->
                <!--1-->
              <!--</nuxt-link>-->
            <!--</th>-->
            <!--<td>2017</td>-->
            <!--<td>××アンケート</td>-->
          <!--</tr>-->
          <!--</tbody>-->
        <!--</table>-->
      <!--</div>-->
    <!--</div>-->
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

</style>

