<template>
   <nav>
       <v-navigation-drawer v-model="drawer" permanent dark app mini-variant mini-variant-width="80" class="white">
           <v-list>
               <v-list-item class="mb-12">
                <v-list-item-content>
                   <v-icon class="mb-2" large color="green">mdi-wechat</v-icon>
                </v-list-item-content>
               </v-list-item>
           </v-list>
           <v-list flat>
               <v-list-item router to="">
                   <v-list-item-content>
                       <v-icon class="mb-2" color="grey">mdi-file</v-icon>
                   </v-list-item-content>
               </v-list-item>
               <v-list-item router to="/">
               <v-list-item-content>
                   <v-icon class="mb-2" color="grey">mdi-calendar</v-icon>
                   </v-list-item-content>
                   </v-list-item>
                   <v-list-item router to="/">
                        <v-list-item-content>
                            <v-icon class="mb-2" color="green">mdi-comment</v-icon>
                        </v-list-item-content>
                   </v-list-item>
                   <v-list-item router to="">
                       <v-badge color="green" dot overlap>
                    <v-list-item-content>
                        <v-icon class="mb-2" color="grey">mdi-bell</v-icon>
                    </v-list-item-content>
                    </v-badge>
                   </v-list-item>
           </v-list>
           <v-list class="my-6" >
               <v-list-item router to="/">
                   <v-list-item-content>
                       <v-icon color="grey">mdi-account</v-icon>
                   </v-list-item-content>
               </v-list-item>
               <v-list-item router to="/">
               <v-list-item-content>
                   <v-icon color="grey">mdi-cog</v-icon>
               </v-list-item-content>
               </v-list-item>
               <v-list-item router to="/">
                <v-list-item-avatar >
                 <v-badge 
                 bordered
                 bottom
                 color="blue"
                 dot
                 offset-x="10"
                 offset-y="10"
                 >
                <v-avatar size="30" class="ml-1">
                    <v-img src="https://cdn.vuetifyjs.com/images/john.jpg"></v-img>
                </v-avatar>
                 </v-badge>
                </v-list-item-avatar>
               </v-list-item>
           </v-list>
        
       </v-navigation-drawer>
   </nav>
</template>

<script>
export default {
    data(){
        return{
            drawer:true
        }
    }
}
</script>

<style>

</style>