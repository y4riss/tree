<template>
<div>
 
  <div  class="container">
    <div >
           <div    class="align " >
       <div v-if="hasChild" @click="menuToggle()">
         <b-icon  icon="plus-lg"  v-if="!varia"></b-icon>
         <b-icon   icon="dash-lg"  v-else-if="varia"></b-icon> 
       </div>
       
       <div v-if="!hasChild" >
         <b-icon  icon="diamond-fill"  ></b-icon>
       </div>

<div >{{ nom }}</div>     
     
     </div>
         <div class="child">
            <div  v-if="varia"  >
              <ContenuMenu
               class="children"
             v-for="(item,index) in data"
               :key="index"
               :nom="item.nom"
               :depth="depth + 1"
               :data="item.fils"
              />
       </div>
     </div>
    </div>
   
  
  </div>
</div>
</template>

<script>
export default {
   name:'ContenuMenu',
  data(){
    return {
       varia:false
   
    }
  },
  props:{
     nom:{
      type: String,
      required: true
     },
     menuTree:{
           type: Object
     },
     depth:{
      type:Number,
      required:true
     },
     data:{
        type: Array,
        required:true
     },
     fils:{
      type: Array,
      required:true
     }
  },
  methods:{
    menuToggle(){
    this.varia = !this.varia;
    }
  },
  computed:{
        hasChild(){
       return this.data
    }
  },
}
</script>

<style scoped>
.children {
 margin-left: 10px;

}

.child{
  color: rgb(15, 17, 15);
 
}

.align{
  display: flex;
margin-left: 10px;
}
#treeName{
  margin-left: 1px;
}
.b-icon{
    cursor: pointer;
    margin-right: 10px;
}
.container{
  margin-bottom: 10px;
    margin-left: 10px;
    padding-right: 20px;
     
}

.titleTree{
  margin-right: 50px; 
}



</style>