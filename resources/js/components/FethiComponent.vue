
<template>
  <div>
    wesha fethi
   
    <Lewl></Lewl>
    <div>{{steps[0].__file}}</div>
    <div>{{step}}</div>
    <component v-bind:is="steps[step]"></component>
    

  </div>
</template>

<script >
  import Zawej from './zawej.vue';
  import { ref } from 'vue';
  
  import Lewl from './lewl.vue' ;
  import { data } from 'browserslist';
  const steps =[Zawej ,Lewl] ;
  export default {
      components: { Zawej ,Lewl } ,
      setup (props){
        
        return{
          steps,step
        }
      }
  }

  const step = ref(1);


  console.log(steps[0].__file) ;
  </script>



<style>

</style>