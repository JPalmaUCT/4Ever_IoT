<template>
    <v-container fluid fill-height >
        <v-row align="center" justify="center">
            <v-col md="6">
                <v-card >
                    <v-card-text>
                        <div>
                            <v-form v-model="valid" ref="form" lazy-validation>
                                    <div class="text-h5 text-center title">
                                        Bienvenido
                                    </div>

                                    <div class="text-h7 text-center">
                                        No tienes cuenta en 4Ever IoT? <span class="pr-2"></span><router-link to="">Crear una cuenta</router-link>
                                    </div>

                                    <v-text-field
                                    v-model="email"
                                    :rules="emailRules"
                                    label="E-mail"
                                    required
                                    ></v-text-field>

                                    <v-text-field
                                    v-model="password"
                                    :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                                    :type="show1 ? 'text' : 'password'"
                                    name="input-10-1"
                                    label="Contraseña"
                                    hint="Al menos 8 caracteres"
                                    counter
                                    ></v-text-field>

                                    <div class="text-right">
                                        <router-link to="">Olvidé mi contraseña</router-link>
                                    </div>

                                    <v-btn 
                                    class="mr-4"
                                    @click="submit"
                                    >Enviar</v-btn>

                            </v-form>
                        </div>
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
    <!--:rules="[rules.required, rules.min]"-->
    <!--@click:append="show1 = !show1"-->
</template>


<script>
export default {
    data () {
        return{
            valid:true,
            show1: false,
            name: '',
            nameRules: [
                v => !!v || 'Nombre es necesario',
                v => (v && v.length <=15) || 'El nombre debe ser menor a 15 caracteres'
            ],
            email: '',
            emailRules: [
                v => !!v || 'E-mail es necesario',
                v => /.+@.+\..+/.test(v) || 'E-mail debe ser valido',
            ],
            password: '',
            rules: {
                required: value => !!value || 'Necesario.',
                min: v => v.length >= 8 || 'Min 8 Caracteres.',
                emailMatch: () => ('El email y contraseña que ingresaste no coinciden.')
            }
        }
    },
    methods: {
        submit(){
            console.log("hola");
        }
    }

}
</script>