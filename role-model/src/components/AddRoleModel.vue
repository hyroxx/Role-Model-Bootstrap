
<template>
    <div class="mx-auto " style="width: 100%;"> 
        <b-img :src="ImageSource" v-bind="mainProps" rounded alt="Rounded image"></b-img>
        <b-form>
            <b-form-input class ="mt-2" v-model ="modallName" placeholder="What is your role model name?"></b-form-input>
            <b-form-input class ="mt-2" v-model="modalJob" placeholder="What is his/her job?"></b-form-input>
            <b-form-input class ="mt-2" v-model="modalNationality" placeholder="What is his/her nationality?"></b-form-input>
            <b-form-input class ="mt-2" v-model="modalImage" placeholder="Add his/her picture link."></b-form-input>
            <label class ="mt-3">Choose his/her birthday</label>
            <b-form-datepicker id="example-datepicker" v-model="modalBirthday" class="mb-2"></b-form-datepicker>
            <b-form-textarea v-model="modalAbout" placeholder="Notes about him/her..." rows="3" max-rows="6"></b-form-textarea> 
            <label for="tags-basic">Type a new tag and press enter</label>
                <b-form-tags input-id="tags-basic" v-model="tags"></b-form-tags>
                <p class="mt-2">Array: {{ tags }}</p>
            <b-button @click="sendRoleModel()" block variant="outline-primary">Submit</b-button>
        </b-form>
    </div>
    
</template>
<script>

export default{
    data(){
        return{
            modalName:'',
            modalJob:'',
            modalNationality:'',
            modalImage:'',
            modalBirthday:'',
            tags:[],
            modalAbout:'',
            ImageSource:"https://www.rootsofaction.com/wp-content/uploads/2017/12/Who-is-my-role-model.jpg",
            mainProps: { width: 350, height: 250, class: 'm1' }
        }
    },
    methods:{
        sendRoleModel(){
            const a =[this.modalName,this.modalJob,this.modalNationality,this.modalBirthday,this.modalAbout,this.modalImage,this.tags];
            this.$emit('fromAddRoleModel',a);

        }
    }
}


</script>
