<template>
    <v-container fluid fill-height>
    <v-row no-gutters>
        <v-col cols="12" >
              <!--<v-carousel delimiter-icon="mdi-minus" hide-delimiter-background>
                <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src">
                <v-sheet color="transparent" height="100%" tile class="disableBlur">
                    <v-row class="fill-height" align="center" justify="center" >
                    <v-col cols="10" class="text-right">
                    <div class="display-3 hidden-sm-and-down">
                        <strong id="titulo-big">4Ever IoT</strong>
                        <div class="display-1 hidden-sm-and-down">La plataforma en la que combinas</div>
                        <v-row >
                            <v-col cols="4" class="text-right">
                                <div>Vue</div>
                            </v-col>
                            <v-col cols="4">
                                <div>+ Vuetify</div>
                            </v-col>
                            <v-col cols="4">
                                <div>+ Internet de las cosas</div>
                            </v-col>
                        </v-row>
                    </div>
                    <v-col cols="12" class="display-2 hidden-md-and-up">
                        <strong>4Ever IoT</strong>
                        <div class="hidden-md-and-up" id="txt-2">En donde combinas</div> 
                        <v-row>
                            <v-col cols="3">
                                <div class="text-h5">Vue</div>
                            </v-col>
                            <v-col cols="4">
                                <div class="text-h5">+Vuetify</div>
                            </v-col>
                            <v-col cols="5">
                                <div class="text-h5">+Internet de las cosas</div>
                            </v-col>
                        </v-row>
                    </v-col>
                    </v-col>
                    </v-row>
                </v-sheet>
                </v-carousel-item>
            </v-carousel>-->
        </v-col>
    </v-row>
    <v-row no-gutters >
        <v-col md="4" vertical-centered>
            <div class="pa-12 ma-12"></div>
            <div class="text-h4 text-left jmbo">Bienvenido a 4EverIoT</div>
            <div class="text-h5 text-left jmbo">En esta página podras implementar una solución IoT para tus dispositivos</div>
            <v-btn color="success" elevation="9" x-large to="/login" class="ma-6 jmbo"> Prueba Ya! </v-btn>
            <v-btn color="primary" elevation="9" x-large to="/guias" class="ml-6 jmbo">Tutorial</v-btn>
        </v-col>
        <v-col md="8" class="mt-2">
            <v-img src="../assets/imagenes/4445_2.png"></v-img>
        </v-col>
    </v-row>
    <v-divider></v-divider>
    <div class="pa-7"></div>
    <v-divider></v-divider>
    <v-row>
        <v-col cols="12">
            <div class="text-h3" align="center">
            Conceptos
            </div>
        </v-col>
    </v-row>
    
    <v-row justify="center">
        <v-col cols="12">
            <v-row no-gutters>
                <v-col md="4" class="text-left"> 
                    <v-card elevation="0" color="transparent">
                        <v-card-title>Internet de las cosas</v-card-title>
                        <v-card-subtitle>Comunmente IoT</v-card-subtitle>
                        <v-card-text></v-card-text>
                    </v-card>   
                </v-col>
                <v-col md="4" class="text-left">
                    <v-card elevation="0" color="transparent">
                        <v-card-title>Vue</v-card-title>
                        <v-card-subtitle>Basado en Javascript</v-card-subtitle>
                        <v-card-text></v-card-text>
                    </v-card>   
                </v-col>
                <v-col md="4" class="text-left">
                    <v-card elevation="0" color="transparent">
                        <v-card-title>Diseño de Vuetify</v-card-title>
                        <v-card-subtitle>Framework Material Desing</v-card-subtitle>
                        <v-card-text></v-card-text>
                    </v-card>   
                </v-col>
            </v-row>
        </v-col>
    </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        model: 0,
        colors: [
            'primary',
            'secondary',
            'yellow darken-2',
            'red',
            'orange',
        ]
        }),
    data (){
        return{
            items: [
                {src: require('@/assets/imagenes/modern-city-2.png')},
            ]
        }
    }

}
</script>

<style scoped>
#txt-2{
    font-size:.5em
}
#titulo-big{
    font-size: 2em;
}
</style>