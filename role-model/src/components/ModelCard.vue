<template>
    <div>
        <b-card
            :title="modalName"
            :img-src="modalImage"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem;"
            class="mb-2"
  >
    <b-card-text>
      {{modalJob}} - {{modalNationality}} - {{modalBirthday}}
    </b-card-text>
    <b-card-text>
      {{modalAbout}}
    </b-card-text>

    <div class="tagsClass">
     <b-card-text class="tagsText"
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
<style>

.tagsClass{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}
.tagsText{
    background-color:azure;
    margin: 6px 4px 6px 4px;
    font-size: 18px;
    font-family: Cambria, sans-serif;
    padding: 2px 3px 2px 3px;
    box-shadow:0 0 2px mediumblue;
}
</style>
