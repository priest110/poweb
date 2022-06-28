<template>
  <v-container class="principal fluid">
    <v-row class="text-center" style="height:100%; margin-bottom: 0px; margin-top: 0px;">
      <v-col xl="6" lg="6" md="6" cols="12">
        <lottie-vue-player src="https://assets6.lottiefiles.com/packages/lf20_cijhv0zb/logo 2/data.json"
          :theme="options.theme"
          :player-size="options.playerSize"
          autoplay
          style="width: 100%; height:100%"
          ref="lottie"
          class="animation_logo">
        </lottie-vue-player> 
      </v-col>
      <v-col xl="6" lg="6" md="6" cols="12" style="padding-top: 0px;padding-bottom: 0px;">
        <v-row :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? 'right_side_page' : ''">
          <v-col xl="7" lg="7" md="7" cols="12" class="message_col">
            <v-row class="text-left" style="background-color:#47b1e3;">
              <v-col v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" cols="3"/>

              <v-col xl="8" lg="8" md="8" cols="12">
                <v-card class="message_card" flat rounded="0">
                  <h2 class="font-weight-bold white--text mt-10">
                    website em desenvolvimento...
                  </h2>
                  <h3 class="my-4 subheading white--text font-weight-regular white--text">
                    Poweb.pt está prestes a chegar para demonstrar como conectamos ideias, negócios, produtos a planos de comunicação e soluções criativas para o seu negócio.
                  </h3>
                  <h1 class="mb-10 display-2 font-weight-bold white--text">
                    Vamos trabalhar juntos!
                  </h1>   
                  <v-row>
                    <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                      <v-icon x-large class="white--text">
                          mdi-phone
                      </v-icon>
                    </v-col>
                    <v-col class="mt-2" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                      <strong class="white--text">933 012 704</strong>
                    </v-col>
                  </v-row>
                  <v-row class="mt-n4">
                    <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                      <v-icon x-large class="white--text">
                        mdi-map-outline
                      </v-icon>
                    </v-col>
                    <v-col class="mt-n1" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                      <strong class="white--text">
                        Rua Padre Armando Lira
                      </strong>
                      <p class="white--text mt-n1">
                        <strong>
                          n12 Maximinos
                        </strong>
                      </p>
                      <p class="white--text mt-n5">
                        <strong>
                          4705-672 Braga
                        </strong>
                      </p>
                    </v-col>
                  </v-row>
                  <v-row class="mt-n9 mb-4">
                    <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                      <v-icon x-large class="white--text">
                        mdi-clock-time-four-outline
                      </v-icon>
                    </v-col>
                    <v-col class="mt-2" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                      <strong class="white--text">
                        Seg-Sex: 9h30-18h00
                      </strong>
                    </v-col>
                  </v-row>
                  <v-btn class="mr-4" icon href="http://www.facebook.com/wearePOWEB" target="_blank">
                    <v-icon x-large class="white--text">
                      mdi-facebook
                    </v-icon>
                  </v-btn>
                  <v-btn class="mr-4" icon href="http://www.instagram.com/wearepoweb/" target="_blank">
                    <v-icon x-large class="white--text">
                      mdi-instagram
                    </v-icon>
                  </v-btn>
                  <v-btn class="mr-4" icon href="http://www.linkedin.com/company/powebmedia/" target="_blank">
                    <v-icon x-large class="white--text">
                      mdi-linkedin
                    </v-icon>
                  </v-btn>
                  <v-btn icon href="http://www.twitter.com/wearePOWEB" target="_blank">
                    <v-icon x-large class="white--text">
                      mdi-twitter
                    </v-icon>
                  </v-btn>
                </v-card>
              </v-col>
                
              <v-col v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" cols="1">
              </v-col>
            </v-row>
          </v-col>
          <v-col xl="5" lg="5" md="5" cols="12" class="form_col" :style="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'padding: 0;'">
            <v-card class="form_card" color="white" flat rounded="0">
              <v-form ref="form" v-model="form_valid" lazy-validation @submit.prevent="send_email">
                <v-card-text class="mb-n4">
                  <v-text-field label="Nome*" name="nome" v-model="nome" :rules="general_rules" required>
                  </v-text-field>
                  <v-text-field label="Telefone" name="telefone" v-model="telefone" :rules="telefone_rules">
                  </v-text-field>
                  <v-text-field label="Email*" name="email" v-model="email" :rules="email_rules" required>
                  </v-text-field>
                  <v-text-field label="Assunto*" name="assunto" v-model="assunto" :rules="general_rules" required>
                  </v-text-field>
                  <v-textarea label="Mensagem*" name="mensagem" v-model="mensagem" :rules="general_rules" required>
                  </v-textarea>
                </v-card-text>
                <v-card-actions class="justify-center">
                  <v-btn class="mt-n3 white--text" type="submit"  :disabled="!form_valid" color="#47b1e3">
                    Enviar
                  </v-btn>
                </v-card-actions>
              </v-form>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  //import html from '../assets/logo/demo/data.html'
  import emailjs from 'emailjs-com';

  export default {
    name: 'HelloWorld',

    data: () => ({
      //html,
      loader: null,
      loading: false,
      logo_view : 'logo_view',
      nome: '',
      general_rules: [
        v => !!v || 'Campo obrigatório',
      ],
      telefone: '',
      telefone_rules: [
          v => v == '' || /^(91|92|93|96)[0-9]{7}$/.test(v) || 'Número inválido'
      ],
      email: '',
      email_rules: [
        v => !!v || 'Campo obrigatório',
        v => /.+@.+\..+/.test(v) || 'Email tem de ser válido',
      ],
      assunto: '',
      mensagem: '',
      form_valid: true,
      options: {
        minimizable: false,
        playerSize: "standard",
        backgroundColor: '#fff',
        backgroundStyle: 'color',
        theme: {
            controlsView: "standard",
            active: "light",
            light: {
                color: '#3D4852',
                backgroundColor: '#fff',
                opacity: '0.7',
            },
            dark: {
                color: '#fff',
                backgroundColor: '#202020',
                opacity: '0.7',
            }
        }
      },
      counter: 0
    }),
    mounted(){
      this.onResize
      let resizeTimer;
      
      window.addEventListener("resize", () => {
        document.getElementsByClassName('form_col')[0].style.display = "none"
        document.getElementsByClassName('message_col')[0].style.display = "none"
        document.body.classList.add("resize-animation-stopper");
        clearTimeout(resizeTimer);
        resizeTimer = setTimeout(() => {
          document.getElementsByClassName('form_col')[0].style.display = "initial"
          document.getElementsByClassName('form_col')[0].style.visibility = "visible"
          document.getElementsByClassName('message_col')[0].style.display = "initial"
          document.getElementsByClassName('message_col')[0].style.visibility = "visible"
        }, 200);
      });
        
      setTimeout(this.signal_pause, 1000)
    },
    
    watch: {
      loader () {
        const l = this.loader
        this[l] = !this[l]
        console.log()
        this.loader = null
      }
    },

    methods:{
      signal_pause(){
        console.log(this.$refs.lottie.getLottie().currentFrame)

        if(this.$refs.lottie.getLottie().currentFrame < 87.0){
          this.currentFrame = this.$refs.lottie.getLottie().currentFrame
          setTimeout(this.signal_pause, 1000)
        }
        else{
          this.currentFrame = this.$refs.lottie.getLottie().currentFrame
          this.$refs.lottie.togglePlayPause()
        }
      },
      send_email(e) {
        try {
          if(this.$refs.form.validate()){
            emailjs.sendForm('service_35n3vii', 'template_tns1jwt', e.target,
            'feys9QoyArDyoEylB', {
              nome: this.nome,
              telefone: this.telefone,
              email: this.email,
              assunto: this.assunto,
              mensagem: this.mensagem
            })
            this.$refs.form.reset()
          }
        } catch(error) {
            console.log({error})
        }
        // Reset form field
        this.nome = ''
        this.telefone = ''
        this.email = ''
        this.assunto = ''
        this.mensagem = ''
    },
    }
  }
</script>
<style>

.right_side_page{
  position: relative; 
  overflow: auto; 
  height: 100%;
  margin-top: 0px !important;
  margin-bottom: 0px !important;
}

/* ESTE É QUE FODE A CENA RESPONSIVA */
@media screen and (min-width: 960px) {
  .form_col{
    position: absolute;
    margin-top: 15%;
    left: 10%;
    visibility: hidden;
    animation-name: change_form;
    animation-delay: 5s;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }
}

.form_card{
  z-index: 10;
}

@media screen and (min-width: 960px) {
  .message_col{
    position: absolute;
    right: 0;
    height:100%;
    background-color: #47b1e3 !important;
    visibility: hidden;
    animation-name: change_message;
    animation-delay:3s;
    animation-duration: 3s;
    animation-fill-mode: forwards;
  }
}

/* * { border: 1px solid red; } */

.message_card{
  background-color: transparent !important;
  height: 100%;
}

.principal{
  margin-right: 0 !important;
  padding-right: 0 !important;
  padding-bottom: 0 !important;
  padding-top: 0 !important;
  height: 100%;
  max-width: 100% !important;
}

/* Background da animação transparente */
.vue-lottie-player{
  background-color: transparent !important;
}

/* A regra keyframes serve para certa animação mudar de um certo estilo para outros */
@keyframes change_logo {
  0%   {left:25%;}
  30%  {left:25%;}
  50%  {left:25%;}
  70% {left:0;}
  100% {left:0;}
}

@keyframes change_message {
  0%   {right:-25%; visibility: hidden;}
  50%  {right:25%; visibility: visible;}
  100% {right:0; visibility: visible;}
}

@keyframes change_form {
  0%   {left:-25%; visibility: hidden;}
  50%  {left:15%; visibility: visible;}
  100% {left:10%; visibility: visible;}
}

@media screen and (min-width: 960px) {
  .animation_logo{
    animation-name: change_logo;
    animation-duration: 7s;
  }
}

.resize-animation-stopper * {
  animation: none !important;
  transition: none !important;
}

.lf-spinner{
  visibility: hidden !important;
}

 @import '../../node_modules/video.js/dist/video-js.css';
</style>