<template>
    <v-container fluid>
    <v-row no-gutters>
        <v-col cols="12" >
              <v-carousel delimiter-icon="mdi-minus" hide-delimiter-background>
                <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src">
                <v-sheet color="transparent" height="100%" tile class="disableBlur">
                    <v-row class="fill-height" align="center" justify="center" >
                    <v-col cols="10" class="text-right">
                    <div class="display-3 hidden-sm-and-down">
                        <strong id="titulo-big">4Ever IoT</strong>
                        <div class="display-1 hidden-sm-and-down">La plataforma en la que combinas</div>
                        <v-row >
                            <v-col cols="4" class="text-right">
                                <!--v-img src='../assets/imagenes/vue.png' contain height="100px" width="150px"></v-img>-->
                                <div>Vue</div>
                            </v-col>
                            <v-col cols="4">
                                <!--<v-img src="../assets/imagenes/vuetify.png" contain height="100px" width="150px"></v-img>-->
                                <div>+ Vuetify</div>
                            </v-col>
                            <v-col cols="4">
                                <!--<v-img src="../assets/imagenes/vuetify.png" contain height="100px" width="150px"></v-img>-->
                                <div>+ Internet de las cosas</div>
                            </v-col>
                        </v-row>
                    </div>
                    <v-col cols="12" class="display-2 hidden-md-and-up">
                        <strong>4Ever IoT</strong>
                        <div class="hidden-md-and-up" id="txt-2">En donde combinas</div> <!--Esconde medianas a arriba/muestra en md abajo -->
                    </v-col>
                    </v-col>
                    </v-row>
                </v-sheet>
                </v-carousel-item>

            </v-carousel>
        </v-col>
    </v-row>
    <v-row align="center">
        <v-col col="6" class="text-right">
            <v-btn
            color="primary"
            elevation="9"
            large
            >Prueba Ya!
            </v-btn>
        </v-col>
        <v-col col="6">
            <v-btn
            color="primary"
            elevation="9"
            large
            >Tutorial</v-btn>
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