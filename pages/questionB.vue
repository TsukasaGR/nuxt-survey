<template>
  <div class="question-b">
    <h1>アンケートB</h1>
    <!-- If you want to show survey, uncomment the line below -->
    <survey :survey="survey"></survey>
    <!-- If you want to show survey editor, uncomment the line below -->
    <!-- <survey-editor></survey-editor> -->
    <!--<survey-editor></survey-editor>-->
  </div>
</template>

<script>
  // import SurveyEditor from './components/SurveyEditor'
  import * as SurveyVue from 'survey-vue'
  // import 'bootstrap'
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
  var Survey = SurveyVue.Survey
  Survey.cssType = "bootstrap";

  import * as widgets from "surveyjs-widgets";
  import "inputmask/dist/inputmask/phone-codes/phone.js";

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
    name: 'app',
    components: {
      Survey,
      // SurveyEditor
    },
    data () {
      var json = { title: 'Product Feedback Survey Example', showProgressBar: 'top', pages: [
          {
            name: "page1",
            elements: [
              {
                type: "text",
                name: "question1",
                title: "テスト"
              },
              {
                type: "checkbox",
                name: "question2",
                choices: [
                  "item1",
                  "item2",
                  "item3"
                ]
              },
              {
                type: "radiogroup",
                name: "question3",
                choices: [
                  "item1",
                  "item2",
                  "item3"
                ]
              }
            ]
          }
        ]
      };
      var model = new SurveyVue.Model(json)
      return {
        survey: model
      }
    }
  }
</script>

<style scoped>
.question-b {
  padding: 50px 300px;
}
.question-b h1 {
  margin-bottom: 50px;
}
</style>
