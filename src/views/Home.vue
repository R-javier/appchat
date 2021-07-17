<template>

  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-container fluid>
      <v-row>
        <v-col col="12" sm="3" class="border" >
          <v-app-bar flat color="rgba(0,0,0,0)">
            <v-btn tile color="white"  block>
              <v-icon left color="green">mdi-plus</v-icon>
            
            <v-divider class="mr-3"></v-divider>
              Nueva conversación 
              </v-btn>
          </v-app-bar>
          <v-app-bar flat color="rgba(0,0,0,0)">
            <v-toolbar-title class="title">Chat</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon>
              <v-icon>mdi-dots-horizontal</v-icon>
            </v-btn>
          </v-app-bar>
          <v-app-bar flat color="rgba(0,0,0,0)">
            <v-text-field
            filled
            label="Buscar Aquí"
            append-icon="mdi-magnify"
            color="grey">
            </v-text-field>
          </v-app-bar>
          <v-list two-line color="rgba(0,0,0,0)">
            <v-list-item-group v-model="selected" active-class="blue lighten-4" multiple>
              <template v-for="(item, index) in items">
                <v-list-item :key="item.title">
                  <v-badge bordered bottom color="green" dot offset-x="22" offset-y="26">
                    <v-list-item-avatar>
                      <v-img :src="item.avatar"></v-img>
                    </v-list-item-avatar>
                  </v-badge>
                  <template>
                    <v-list-item-content>
                      <v-list-item-title v-text="item.title"></v-list-item-title>
                      <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
                    </v-list-item-content>
                  </template>
                </v-list-item>
                <v-divider v-if="index < items.length - 1" :key="index"></v-divider>
              </template>
            </v-list-item-group>
          </v-list>
        </v-col>
        <v-col cols="12" sm="6" class="border">
          <v-app-bar flat color="rgba(0,0,0,0)">
            <v-badge bordered bottom color="green" dot offset-x="11" offset-y="13">
              <v-avatar class="mt-n7" size="40" elevation="10">
                <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="">
              </v-avatar>
            </v-badge>
            <v-toolbar-title class="title pl-0 ml-2 mt-n4">Jonathan Ruiz</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-title class="title pl-0 mr-2 mt-n4">
              Miembros:
            </v-toolbar-title>
            <v-btn color="green" icon class="mt-n5 mr-n2" outlined max-height="35" max-width="35">
              <v-icon small>mdi-plus</v-icon>
            </v-btn>
            <v-avatar class="mt-n5 mr-2 ml-4" size="28" elevation="10">
              <img src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460" alt="">
            </v-avatar>
            <v-divider vertical inset class="mt-n1"></v-divider>
            <v-btn color="black" icon class="mt-n5">
              <v-icon>mdi-cog</v-icon>
            </v-btn>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="blue" dark>
                <v-list-item three-lines>
                  <v-list-item-content>
                    <div class="mb-4">
                      Hola Buenos días, como estas hoy ?
                    </div>
                    <v-list-item-subtitle>hace 40 minutos <span class="ml-16">visto 3:30PM</span> </v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
            </v-card>
            <v-badge bordered bottom color="green" dot offset-x="10" offset-y="10">
              <v-avatar class="mt-n5" size="30" elevation="10">
                <img src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460" alt="">
              </v-avatar>
            </v-badge>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
            <v-badge bordered bottom color="green" dot offset-x="16" offset-y="9">
              <v-avatar class="mt-n5 mr-2" size="30" elevation="10">
                <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="">
              </v-avatar>
            </v-badge>
            <v-card class="mt-10" max-width="350px" color="">
              <v-list-item three-line>
                <v-list-item-content>
                  <div class="mb-4">
                    Bien, todo bien y vos ? Te envio las fotos que me pediste...
                  </div>
                  <v-list-item-subtitle>20 min</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-card>
            <v-btn color="grey" icon class="mb-n10">
              <v-icon>mdi-dots-horizontal</v-icon>
            </v-btn>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
            <v-badge bordered bottom color="green" dot offset-x="10" offset-y="10">
              <v-avatar class="mt-n5" size="30" elevation="10">
                <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="">
              </v-avatar>
            </v-badge>
            <v-card class="mt-10 ml-2" max-width="350px">
              <v-list-item-content>
                <div class="mb-4 ml-4">
                  Te envió 3 fotos :<br><br>
                  <v-avatar size="60" tile class="mr-2"><v-img src="https://picsum.photos/id/237/536/354"></v-img></v-avatar>
                  <v-avatar size="60" tile class="mr-2"><v-img src="https://picsum.photos/seed/picsum/536/354"></v-img></v-avatar>
                  <v-avatar size="60" tile class="mr-2"><v-img src="https://picsum.photos/id/1084/536/354?grayscale"></v-img></v-avatar>
                </div>
                <v-list-item-subtitle class="ml-4">25 min</v-list-item-subtitle>
              </v-list-item-content>
            </v-card>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-8">
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="blue" dark>
              <v-list-item three-line>
                <v-list-item-content>
                  <div class="mb-4">
                   Que bien, gracias
                  </div>
                  <v-list-item-subtitle>8min <span class="ml-16">Visto 3:33 PM</span> </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-card>
            <v-badge bordered bottom color="green" dot offset-x="10" offset-y="10">
              <v-avatar class="mt-n5" size="30" elevation="10">
                <img src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460" alt="">
              </v-avatar>
            </v-badge>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="blue" dark>
              <v-list-item three-line>
                <v-list-item-content>
                  <div class="mb-4">
                    Que tengas buen inicio de semana nos vemos!!!
                  </div>
                  <v-list-item-subtitle>5 minutos <span class="ml-16">Visto 3:45PM</span> </v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-card>
            <v-badge bordered bottom color="green" dot offset-x="10" offset-y="10">
              <v-avatar class="mt-n5" size="30" elevation="10">
                <img src="https://avatars0.githubusercontent.com/u/9064066?v=4&s=460" alt="">
              </v-avatar>
            </v-badge>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat>
            <v-text-field
             v-model="message"
             color="green"
             append-icon="mdi-emoticon"
             :append-outer-icon="message ? 'mdi-send' : 'mdi-microphone'"
             filled clear-icon="mdi-close-circle"
             clearable
             type="text" 
             @click:append-outer="sendMessage" 
             @click:clear="clearMessage">  
              
            </v-text-field>
          </v-app-bar>
        </v-col>
        <v-col cols="12" sm="3">
            <v-card class="text-center mt-8 mb-3" shaped>
              <v-badge bordered bottom color="green" offset-x="18" offset-y="14">
                <v-avatar class="mt-n7" size="60" elevation="20">
                  <img src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light" alt="">
                </v-avatar>
              </v-badge>
              <v-card-title class="layout justify-center">Laura Gimenez</v-card-title>
              <v-card-subtitle class="layout justify-center">Creadora de contenido</v-card-subtitle>
            </v-card>
            <v-expansion-panels v-model="panel" multiple >
              <v-expansion-panel>
                <v-expansion-panel-header>
                  <h3>Informacion</h3>
                </v-expansion-panel-header>
                <v-expansion-panel-content>

                </v-expansion-panel-content>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-header>
                  <h3>Imagenes(10)</h3>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  
                </v-expansion-panel-content>
              </v-expansion-panel>

              <v-expansion-panel>
                <v-expansion-panel-header>
                  <h3>Archivos(1)</h3>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                    <v-list shaped>
                      <v-list-item-group>
                        <v-list-item v-for="(item, i) in files" :key="i">
                          <v-list-item-icon>
                            <v-icon v-text="item.icon" color="green"></v-icon>
                          </v-list-item-icon>
                          <v-list-item-content>
                            <v-list-item-title v-text="item.text">

                            </v-list-item-title>
                          </v-list-item-content>
                        </v-list-item>
                      </v-list-item-group>
                    </v-list>
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
              
            
          
        </v-col>
      </v-row>
    </v-container>
  </v-app>
  
</template>

<script>
 

  export default {
    data:()=>({
     
        selected:[2],
        items:[
             {
            avatar:'https://avatars0.githubusercontent.com/u/9064066?v=4&s=460',
            subtitle:'Hola Buenos días, como estas hoy ?',
            title: 'Lucas Ruiz'
          },
          {
            avatar:'https://cdn.vuetifyjs.com/images/lists/4.jpg',
            subtitle:'Estuve en tu barrio el otro día, pero no pude pasar a saludar, como estas?',
            title: 'María Laura Perez'
          },
               {
            avatar:'https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light',
            subtitle:'Hola !!!',
            title: 'Laura Gimenez'
          },
            {
            avatar:'https://cdn.vuetifyjs.com/images/lists/1.jpg',
            subtitle:'Estaba en la oficina, paso algo?, todo bien y vos?',
            title: 'yo, Mariano Perez'
          },
            {
            avatar:'https://cdn.vuetifyjs.com/images/lists/2.jpg',
            subtitle:':D',
            title: 'Lautaro Mansilla'
          },
              {
            avatar:'https://cdn.vuetifyjs.com/images/lists/3.jpg',
            subtitle:'Buen dia!?',
            title: 'Laura Gimenez'
          },
           
        
        ],
        files:[
          {text: 'Landing_page.zip', icon:'mdi-cloud-upload'},
          {text: 'requirements.pdf', icon:'mdi-cloud-upload'},
          {text: 'Uwagl.docx', icon:'mdi-cloud-upload'},
        
        ],
        panel:[2],
        show: false,
        message: 'Escribe un mensaje',
        marker: true,
        inconIndex: 0
         }),
         computed: {
           theme(){
             return this.$vuetify.theme.dark ? 'dark' : 'light';
           }
         },
         methods: {
           sendMessage (){
             this.resetIcon()
             this.clearMessage()
           },
           clearMessage(){
             this.message = ''
           },
           resetIcon (){
             this.iconIndex = 0
           }
         }
  }
  
</script>


<style scoped>
.border {
  border-right: 1px solid grey;
}
</style>