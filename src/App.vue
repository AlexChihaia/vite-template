<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';
export default{
  name:'Template',
  data(){
    return{
      baseUrl:'http:/examplebaseurl',
      apiUrls:{
        exampleApi:'/api/example',
      }
    }
  },
  components:{
    AppHeader,
    AppMain,
    AppFooter
  },
  methods:{
    getApi(){
      axios.get(this.baseUrl + this.apiUrls.exampleApi).then(response=>{
        console.log(response);
      } ).catch((error)=>{
        console.log(error);
      });
    }
  }

}
</script>
<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>
<style scoped></style>