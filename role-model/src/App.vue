<template>
  <div >
    <b-container>
  <b-row>
    <b-col sm="4">

      <AddRoleModel @fromAddRoleModel="updateCard($event)"/>
      
    </b-col>
    <b-col sm="8">
      <ModelCard v-for="(item,index) in card" :key="index" :modalName="item[0]" :modalJob="item[1]" 
      :modalNationality="item[2]" :modalBirthday="item[3]"  :modalAbout="item[4]" :modalImage="item[5]" :tags="item[6]"/>
    </b-col>
    
  </b-row>
</b-container>


    
  </div>
</template>

<script>


import globalComponent from "./components/globalComponent";

export default {
  components:{
    ...globalComponent,
   
},
data(){
  return{
    card:[]
  }
},
methods:{
  updateCard(e){
    this.card.push(e);
    console.log(this.card);
  }
}
 
}
</script>

