<template>
  <div id="app" 
  class="menu">
    <div   >
          <center  class="titleTree">{{ tree }} </center>
        <ContenuMenu 
        class="folder"
        v-for="(elm, index) in menuTree"
        :key="index"
        :nom="elm.nom"
        :depth="0"
        :data="elm.fils"
        />
    </div>
  </div>
</template>

<script>
import ContenuMenu from './ContenueMenu.vue'
export default {
  components:{
    ContenuMenu
  },
  data(){
    return{
          tree:"Simple Tree",
        menuTree:[
               {
                nom:'Parent 1',
                   fils: [
                    {
                        nom:'fils 1'
                        ,icon : "trash",
                    },
                    {
                        nom:'fils 2'
                        ,icon : "clock",
                        
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    }
                ]
            },
                           {
                nom:'Parent 2',
                   fils: [
                    {
                        nom:'fils 1'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 2'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    }
                ]
            },
                           {
                nom:'Parent 3',
                   fils: [
                    {
                        nom:'fils 1'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 2'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    }
                ]
            },
                           {
                nom:'Parent 4',
                   fils: [
                    {
                        nom:'fils 1'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 2'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    }
                ]
            },
                           {
                nom:'Parent 5',
                   fils: [
                    {
                        nom:'fils 1'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 2'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    },
                    {
                        nom:'fils 3'
                          ,icon : "diamond-fill",
                    }
                ]
            }
        ]
    }
  }
}
</script>

<style scoped>
.folder{
    color: red;
}
*{ 
        background-color: rgb(231, 219, 219);
}

</style>