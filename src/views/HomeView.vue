<template>
  <v-container>
      <v-row align="center" justify="center" >
          <v-col cols="20" sm="10" md="15" lg="10">
            <v-card class="elevation-6 mt-10"  :class="{ 'signup-active': step === 2 }" >
             <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="6">
                      <v-card-text class="mt-12">
                        <h4
                          class="text-center"
                        >Inicie sesión en su cuenta</h4>
                        <h6
                          class="text-center  grey--text "
                        >Inicia sesión en tu cuenta para que puedas continuar construyendo
 <br>y editar tus cotizaciones</h6>
                        <v-row align="center" justify="center">
                          <v-col cols="12" sm="8">
                           
                          <v-text-field
                            label="Email"
                            outlined
                            dense
                            color="blue"
                            autocomplete="false"
                           class="mt-16"
                          />
                          <v-text-field label="Contraseña" outlined dense color="blue" autocomplete="false" v-model="password" :type="showPassword ? 'text' : 'password'" append-icon="mdi-eye" @click:append="showPassword = !showPassword" />
                            <v-row>
                              <v-col cols="12" sm="7">
                                <v-checkbox
                       
                        label="Recordar contraseña"
                        class="mt-n1"
                        color="blue"
                      > </v-checkbox>
                              </v-col>
                              <v-col cols="12" sm="5">
                                <span class="caption blue--text">Has olvidado tu contraseña</span>
                              </v-col>
                            </v-row>
                          <v-btn color="blue" dark block tile>Inicias sesión</v-btn>
                     
                          </v-col>
                        </v-row>  
                      </v-card-text>
                    </v-col>
                    <v-col cols="12" md="6" class="blue rounded-bl-xl" >
                    <div style="  text-align: center; padding: 90px 0;">
                      <v-card-text class="white--text" >
                        <h3 class="text-center ">¿No tienes cuenta? </h3>
                        <h6
                          class="text-center"
                        ><br>  registrate presionando el botoN de abajo.</h6>
                        <img src="https://img.freepik.com/vector-premium/hombre-electricista-sosteniendo-ilustracion-vectorial-iluminacion_10548-519.jpg?w=740" alt="Texto alternativo de la imagen" style="width: 50%; height: auto;">
                        
                        
                      </v-card-text>
                      <div class="text-center">
                        <v-btn tile outlined dark @click="step++">REGISTRASE</v-btn>
                      </div>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row >
                    <v-col cols="12" md="6" class="blue rounded-br-xl">
                     <div style="  text-align: center; padding: 90px 0;">
                      <v-card-text class="white--text" >
                        <h3 class="text-center ">¿Ya se encuentra registrado?</h3>
                        <h6
                          class="text-center"
                        ><br> Precionar el boton de abajo para Iniciar sesion </h6>
                      </v-card-text>
                      <img src="https://img.freepik.com/vector-gratis/ilustracion-dibujos-animados-electricistas-dibujados-mano_52683-152426.jpg?t=st=1715500697~exp=1715501297~hmac=9be6cf04f028b87e6207e5c6fb5c23328b90e7ef1793124a3a46e96eaed136e3" alt="Texto alternativo de la imagen" style="width: 50%; height: auto; border-radius: 5px;">
                      <div class="text-center">
                       
                        <v-btn tile outlined dark @click="step--">INICIAR SESION </v-btn>
                      </div>
                      </div>
                    </v-col>

                    <v-col cols="12" md="6">
                      <v-card-text class="mt-12">
                        <h4
                          class="text-center"
                        >Regístrate para obtener una cuenta
</h4>
                        <h6
                          class="text-center  grey--text "
                        >¡Vamos a configurarte para que puedas empezar a crear tu primera experiencia de incorporación!</h6>
                        <v-row align="center" justify="center">
                          <v-col cols="12" sm="8">
                           <v-row>
                           <v-col cols="12" sm="6">
                            <v-text-field
                            label="First Name"
                            outlined
                            dense
                            color="blue"
                            autocomplete="false"
                            class="custom-field mt-4"
                           
                          />
                           </v-col>
                           <v-col cols="12" sm="6">
                            <v-text-field
                            label="Last Name"
                            outlined
                            dense
                            color="blue"
                            autocomplete="false"
                           class="custom-field mt-4"
                          />
                           </v-col>
                           </v-row>
                          <v-text-field
                            label="Email"
                            outlined
                            dense
                            color="blue"
                            autocomplete="false"
                            class="custom-field2 mt-4"
                          />
                          <v-text-field
                            label="Password"
                            outlined
                            dense
                            color="white"
                          autocomplete="false"
                           type="password"
                           class="custom-field2 mt-4"
                          
                          />
                            <v-row>
                              <v-col cols="12" sm="7">
                               
                              </v-col>
                             
                            </v-row>
                          <v-btn color="blue" style="" dark block tile>Registrarse</v-btn>
                     
                         <h5
                          class="text-center  grey--text mt-4 mb-3"
                        >Encuentranos en nuestras redes sociales</h5>
                         <div class="d-flex  justify-space-between align-center mx-10 mb-11">
                          <v-btn depressed outlined color="withe">
                            <i class="fab fa-google" style="color: red;"></i>
                          </v-btn>
                          <v-btn depressed outlined color="withe">
                            <i class="fab fa-facebook-f" style="color: blue;"></i>
                          </v-btn>
                          <v-btn depressed outlined color="withe">
                            <i class="fab fa-twitter" style="color: lightblue;"></i>
                          </v-btn>

                         </div>
                          </v-col>
                        </v-row>  
                      </v-card-text>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
  

  export default {
   data: () => ({
    step: 1,
    showPassword: false 
  }),
  props: {
    source: String
  } 

    
  }
</script>
<style scoped>
.v-application .rounded-bl-xl {
    border-bottom-left-radius: 300px !important;
}
.v-application .rounded-br-xl {
    border-bottom-right-radius: 300px !important;
}

  .signup-active {
  background-color: #0c4fcc; /* Color de fondo cuando se activa el formulario de registro */
  transition: background-color 0.5s ease; /* Transición suave del color de fondo */
}

/* Transiciones suaves para los elementos secundarios */
.v-window-item-move {
  transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out; /* Transiciones suaves */
}

/* Estilos para ocultar y mostrar el formulario */
.v-window-item-enter,
.v-window-item-leave-to {
  opacity: 0; /* Oculta el elemento */
  transform: translateX(-100%); /* Empieza fuera de la pantalla */
}
.custom-field {
  background-color: #f5f5f5; /* Cambia el color de fondo */
  width: 140px;
  height: 50px;
  border-radius: 5px;
}
.custom-field2 {
  background-color: #f5f5f5; /* Cambia el color de fondo */
  width: 285px;
  height: 50px;
  border-radius: 5px;
  margin: 5px;

}

</style>