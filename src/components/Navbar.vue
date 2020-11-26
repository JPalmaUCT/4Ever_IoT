<template>
    <v-app-bar app color="transparent" absolute flat>
        <v-btn text to="/">
            <div class="d-flex align-center">
                <v-img
                alt="plataforma Logo"
                class="shrink mr-2"
                contain
                src="@/assets/imagenes/logo.png"
                transition="scale-transition"
                width="50"
                style="filter: invert(100%);"
                />
                <h3 class="display-.5 font-weight-bold hidden-sm-and-down">
                  4Ever IoT
                </h3>
                <div style="color:black"><h4 class="display-.3 hidden-md-and-up black--text"  >4Ever IoT</h4></div>
            </div>
        </v-btn>
        <v-spacer class="hidden-sm-and-down"></v-spacer>
        <v-btn to="/" text class="hidden-sm-and-down">
        <v-icon>mdi-home</v-icon>
            <span class="mr-1">Home</span>
        </v-btn>
        <!--<v-btn to="/about" text class="hidden-sm-and-down" >
            <v-icon>mdi-information-outline </v-icon>
            <span>Acerca de </span>
        </v-btn>-->
        <div class="text-center">
        <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">     
              <v-btn
                color="transparent"
                depressed
                v-bind="attrs"
                v-on="on"
                class="hidden-sm-and-down"
              >
              <v-icon>mdi-information-outline </v-icon> 
                Acerca de
              </v-btn>
            </template>
            <v-list>
              <v-list-item
                v-for="(item, index) in acerca_de"
                :key="index"
                :to="item.url"
                
              >
                  <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-icon>
                <v-list-item-title>{{ item.titulo }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </div>

        <v-btn to="/login" text class="hidden-sm-and-down">
            <span class="mr-2">Log in</span>
        <v-icon>mdi-login</v-icon>
        </v-btn>
        <v-spacer class="hidden-md-and-up"></v-spacer>
        <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      app
      class="primary"
      right
    >
      <v-list-item>
          <v-icon> mdi-account-circle</v-icon>  
        <v-list-item-content>
          <v-list-item-title>Bienvenido</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.titulo"
          link
          :to="item.url"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title >{{ item.titulo }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    </v-app-bar>
</template>

<script>
export default {
    data: ()=> ({
        drawer:false,
        group:null,
        items: [
            {titulo: 'Home', icon:'mdi-home', url:'/'},
            {titulo: 'Iniciar Sesion',icon:'mdi-login', url:'/login'},
            {titulo: 'Acerca de',icon:'mdi-information-outline', url:''},
            {titulo: 'Contacto',icon:'mdi-account-box', url:'/contacto'},
        
        ],
        acerca_de:[
          {titulo: 'Nosotros', icon:'mdi-account-group', url:'/about'},
          {titulo: 'Contacto', icon:'mdi-card-account-phone', url:'/contact'},
          {titulo: 'Historia', icon:'mdi-book-open-blank-variant',url:'/history'}
        ]
    }),
    watch:{
        group(){
            this.drawer= false
        },
    },
}
</script>
<style scoped>
.v-btn:before {
  background-color: transparent !important;
}
</style>