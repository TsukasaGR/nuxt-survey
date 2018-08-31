<template>
  <div class="question">
    <h1>{{ target.title }}</h1>
    <survey :survey="survey"></survey>
  </div>
</template>

<script>
import * as SurveyVue from 'survey-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
var Survey = SurveyVue.Survey
Survey.cssType = "bootstrap";

import * as widgets from "surveyjs-widgets";
import "inputmask/dist/inputmask/phone-codes/phone.js";

import data from '~/api/data.json'

widgets.icheck(SurveyVue);
widgets.select2(SurveyVue);
widgets.inputmask(SurveyVue);
widgets.jquerybarrating(SurveyVue);
widgets.jqueryuidatepicker(SurveyVue);
widgets.nouislider(SurveyVue);
widgets.select2tagbox(SurveyVue);
widgets.signaturepad(SurveyVue);
widgets.sortablejs(SurveyVue);
widgets.ckeditor(SurveyVue);
widgets.autocomplete(SurveyVue);
widgets.bootstrapslider(SurveyVue);

export default {
  name: 'question',
  components: {
    Survey
  },
  data () {
    for (const val of data.data) {
      if (this.$route.params.id === val.id) {
        this.target = val
      }
    }
    var model = new SurveyVue.Model(this.target.prop)
    model.onComplete.add((ret) => {
        console.log(ret)
        alert(JSON.stringify(ret.data))
        alert('回答完了')
      }
    )
    return {
      survey: model,
      target: Object
    }
  }
}
</script>

<style scoped>
.question {
  padding: 50px 300px;
}
.question h1 {
  margin-bottom: 50px;
}
</style>
