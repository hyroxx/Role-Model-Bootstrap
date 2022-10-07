<template>
    <div> 
        <b-card
            :title="modalName"
            :img-src="modalImage"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2 max-w-xs"
  >
    <b-card-text>
      {{modalJob}} - {{modalNationality}} - {{modalBirthday}}
    </b-card-text>
     
    <b-card-text>
      {{modalAbout}}
    </b-card-text>

    <div class="flex flex-row flex-wrap ">
     <b-card-text class="mx-1 my-3 bg-teal-50 text-sm font-serif px-2 py-2 shadow-blue-500 shadow-sm "
        v-for="(i,index) in tags" :key="index">
        {{i}}
     </b-card-text>
    </div>
    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>

    </div>
</template>
<script>
export default {
    props:{ 

        modalName:String,
        modalJob:String,
        modalNationality:String,
        modalBirthday:String,
        modalAbout:String,
        modalImage:String,
        tags:Array,


    },

    data(){
        return{
            
    }
}
}

</script>

