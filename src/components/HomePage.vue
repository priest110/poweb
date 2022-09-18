<template>
  <v-container class="principal fluid">
    <v-row class="text-center" style="height:100%; margin-bottom: 0px; margin-top: 0px;">
      <v-col xl="6" lg="6" md="6" cols="12" :style="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm ? 'min-height:650px' : ''">
        <v-row style="height:100%">
          <v-col xl="11" lg="11" md="11" cols="12">
          <lottie-vue-player src="logo/data.json"
            :theme="options.theme"
            :player-size="options.playerSize"
            autoplay
            style="width: 100%; height:100%"
            ref="lottie" 
            id="logo"
            class="animation_logo logo_poweb">
          </lottie-vue-player> 
          </v-col>
          <v-col v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" cols="1">
            <div class="animation_icons social_icons" style="display:inline-flex; position: relative; top: 90%;">
              <v-btn style="margin-right:1vw" icon href="http://www.facebook.com/wearePOWEB" target="_blank">
                <v-icon x-large class="white--text icon_size">
                  mdi-facebook
                </v-icon>
              </v-btn>
              <v-btn style="margin-right:1vw" icon href="http://www.instagram.com/wearepoweb/" target="_blank">
                <v-icon x-large class="white--text icon_size">
                  mdi-instagram
                </v-icon>
              </v-btn>
              <v-btn style="margin-right:1vw" icon href="http://www.linkedin.com/company/powebmedia/" target="_blank">
                <v-icon x-large class="white--text icon_size">
                  mdi-linkedin
                </v-icon>
              </v-btn>
              <v-btn icon href="http://www.twitter.com/wearePOWEB" target="_blank">
                <v-icon x-large class="white--text icon_size">
                  mdi-twitter
                </v-icon>
              </v-btn>
            </div>
          </v-col>
        </v-row>
      </v-col>
      <v-col xl="6" lg="6" md="6" cols="12" style="padding-top: 0px;padding-bottom: 0px; padding-left: 0px;" :class="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm ? 'resize_col_padding' : ''">
        <v-row :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? 'right_side_page' : ''">
          <v-col xl="6" lg="6" md="7" cols="12" class="message_col animation_message"  style="background-color: #47b1e3 !important;">
            <v-row class="text-left">
              <v-col v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" cols="1"/>

              <v-col xl="10" lg="10" md="10" cols="12">
                <v-card class="message_card" flat rounded="0">
                  <lottie-vue-player src="manutencao.json"
                    :theme="options.theme"
                    :player-size="options.playerSize"
                    autoplay
                    loop
                    style="width: 100%;"
                    class="manutencao">
                  </lottie-vue-player> 
                  <h3 class="info_text font-weight-regular white--text">
                    Contacte-nos para saber como conectamos ideias, negócios, produtos a planos de comunicação e soluções criativas para o seu negócio.
                  </h3>
                  <h1 class="font-weight-bold white--text">
                    Vamos trabalhar em conjunto!
                  </h1>
                  <v-btn id="open_button" v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" fab color="transparent" style="left: 106%; top: -10%;" @click="show_form()"></v-btn>
                  <div :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? 'info_icons' : ''">
                    <v-row>
                      <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                        <v-icon v-if="$vuetify.breakpoint.md" large class="white--text">
                            mdi-phone
                        </v-icon>
                        <v-icon v-else x-large class="white--text icon_size">
                            mdi-phone
                        </v-icon>
                      </v-col>
                      <v-col :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                        <h2 class="font-weight-regular white--text">933 012 704</h2>
                      </v-col>
                    </v-row>
                    <v-row class="mt-n2">
                      <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                        <v-icon v-if="$vuetify.breakpoint.md" large class="white--text">
                            mdi-email
                        </v-icon>
                        <v-icon v-else x-large class="white--text icon_size">
                            mdi-email
                        </v-icon>
                      </v-col>
                      <v-col class="mt-1" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                        <h3 class="font-weight-regular white--text">geral@poweb.pt</h3>
                      </v-col>
                    </v-row>
                    <v-row class="mt-n2">
                      <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                        <v-icon v-if="$vuetify.breakpoint.md" large class="white--text">
                          mdi-map-marker
                        </v-icon>
                        <v-icon v-else x-large class="white--text icon_size">
                          mdi-map-marker
                        </v-icon>
                      </v-col>
                      <v-col class="mt-n1" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                        <h3 class="font-weight-regular white--text">
                          Rua Padre Armando Lira
                        </h3>
                        <p></p>
                        <h3 class="font-weight-regular white--text mt-n5">
                          nº12, 1º Andar Loja 1A Maximinos
                        </h3>
                        <p></p>
                        <h3 class="font-weight-regular white--text mt-n5">
                          4705-672 Braga
                        </h3>
                      </v-col>
                    </v-row>
                    <v-row class="mt-n5">
                      <v-col :cols="$vuetify.breakpoint.sm ? 1 : 2">
                        <v-icon v-if="$vuetify.breakpoint.md" large class="white--text">
                          mdi-clock-time-four-outline
                        </v-icon>
                        <v-icon v-else x-large class="white--text icon_size">
                          mdi-clock-time-four-outline
                        </v-icon>
                      </v-col>
                      <v-col class="mt-2" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'ml-n4'">
                        <h3 class="font-weight-regular white--text">
                          Seg-Sex: 9h30-18h00
                        </h3>
                      </v-col>
                    </v-row>
                  </div>
                  <div  v-if="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm" class="animation_icons social_icons mt-8">
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
                  </div>
                </v-card>
              </v-col>
                
              <v-col v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" cols="1"/>
            </v-row>
          </v-col>
          <v-col xl="5" lg="5" md="5" cols="12" class="form_col" :style="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : 'padding: 0;'">
            <v-card id="form_card" color="white" flat rounded="0">
              <v-form ref="form" v-model="form_valid" lazy-validation @submit.prevent="send_email">
                <v-card-actions v-if="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md" class="justify-end">
                  <v-btn id="close_button" icon class="grey--text" color="#47b1e3" @click="close_form()">
                    <v-icon class="icon_size">
                      mdi-close
                    </v-icon>
                  </v-btn>
                </v-card-actions>
                <v-card-text :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? 'my-n4' : ''">
                  <v-text-field class="text_field" label="Nome*" name="nome" v-model="nome" :rules="general_rules" required>
                  </v-text-field>
                  <v-text-field class="text_field" label="Telefone" name="telefone" v-model="telefone" :rules="telefone_rules">
                  </v-text-field>
                  <v-text-field class="text_field" label="Email*" name="email" v-model="email" :rules="email_rules" required>
                  </v-text-field>
                  <v-text-field class="text_field" label="Assunto*" name="assunto" v-model="assunto" :rules="general_rules" required>
                  </v-text-field>
                  <v-textarea label="Mensagem*" name="mensagem" v-model="mensagem" :rules="general_rules" required>
                  </v-textarea>
                </v-card-text>
                <v-card-actions class="justify-center">
                  <v-btn id="send_button"  class="mt-n3 white--text" type="submit"  :disabled="!form_valid" color="#47b1e3">
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
      counter: 0,
      show: false
    }),
    mounted(){
      this.onResize
      let resizeTimer;
      
      window.addEventListener("resize", () => {
        document.getElementsByClassName('form_col')[0].style.display = "none"
        document.getElementsByClassName('message_col')[0].style.display = "none"
        document.getElementsByClassName('social_icons')[0].style.display = "none"
        document.getElementById('logo').classList.remove('animation_logo')
        document.getElementById('logo').classList.remove('animation_logo_before')
        document.getElementById('logo').classList.remove('animation_logo_after')
        document.getElementById('form_card').classList.remove('animation_form')
        document.getElementById('form_card').classList.remove('animation_form_back')
        document.body.classList.add("resize-animation-stopper");
        clearTimeout(resizeTimer);
        resizeTimer = setTimeout(() => {
          document.getElementsByClassName('form_col')[0].style.display = "initial"
          document.getElementsByClassName('message_col')[0].style.display = "initial"
          document.getElementsByClassName('social_icons')[0].style.display = "inline-flex"
          document.getElementsByClassName('message_col')[0].style.visibility = "visible"
          document.getElementsByClassName('social_icons')[0].style.visibility = "visible"
        }, 200);
      });
      setTimeout(this.signal_pause, 1000)
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
      show_form(){
        var ob = document.getElementById('open_button')
        ob.classList.remove('animation_button')
        void ob.offsetWidth;
        ob.classList.add('animation_button')
        var fc = document.getElementById('form_card')
        fc.classList.remove('animation_form_back')
        void fc.offsetWidth;
        fc.classList.add('animation_form')
        var lg = document.getElementById('logo')
        lg.classList.remove('animation_logo')
        lg.classList.remove('animation_logo_before')
        void lg.offsetWidth;
        lg.classList.add('animation_logo_after')
      },
      close_form(){
        var fc = document.getElementById('form_card')
        fc.classList.remove('animation_form')
        void fc.offsetWidth;
        fc.classList.add('animation_form_back')
        var lg = document.getElementById('logo')
        lg.classList.remove('animation_logo_after')
        void lg.offsetWidth;
        lg.classList.add('animation_logo_before')
      }
    }
  }
</script>
<style>

/* Fixes responsive and size stuff in general */

  .manutencao{
    left: -2%;
  }

  .right_side_page{
    position: relative; 
    overflow: visible; 
    left: -100%;
    height: 100%;
    margin-top: 0px !important;
    margin-bottom: 0px !important;
  }

  .message_card{
    background-color: transparent !important;
    height: 100%;
  }

  .principal{
    margin-right: 0 !important;
    padding-bottom: 0 !important;
    padding-top: 0 !important;
    height: 100%;
    max-width: 100% !important;
  }

  .vue-lottie-player{
    background-color: transparent !important;
  }

  .resize_col_padding{
    padding-left: 12px !important;
  }

  .lf-spinner{
    visibility: hidden !important;
  }

  #open_button{
      background-image: url('../assets/Mensager.svg');
      background-size: cover;
  }

/* Deals how animations work (the keyframes rule is for a certain animation to change from a certain style to another) */
  
  @keyframes change_logo {
    0%   {left:30%;}
    30%  {left:30%;}
    50%  {left:30%;}
    70%  {left:40%;}
    100% {left:40%;}
  }

  @keyframes change_logo_after {
    0%   {left:40%;}
    100% {left:45%;}
  }

  @keyframes change_logo_before {
    0%   {left:45%;}
    100% {left:40%;}
  }

  @keyframes change_message {
    0%   {left:-25%; visibility: hidden;}
    50%  {left:25%; visibility: visible;}
    100% {left:0; visibility: visible;}
  }

  @keyframes change_form {
    0%   {transform: translate(0, 0) scale(0.1);visibility: hidden;}
    100% {transform: translate(35%, 5%) scale(1);visibility: visible;}
  }

  @keyframes change_form_back {
    0%   {transform: translate(35%, 5%) scale(1);visibility: visible;}
    100% {transform: translate(0%, 0%) scale(0.1);visibility: hidden;}
  }

  @keyframes change_icons {
    0%   {top:95%; visibility: hidden;}
    50%  {top:90%; visibility: visible;}
    100% {top:90%; visibility: visible;}
  }

  @keyframes change_menu {
    0%   {bottom:-25%; visibility: hidden;}
    50%  {bottom:-15%; visibility: visible;}
    100% {bottom:-15%; visibility: visible;}
  }

  @keyframes change_button {
    0%   {scale: 1.25; visibility: visible;}
    50%  {scale: 1.25; visibility: visible;}
    100% {scale: 1.25; visibility: visible;}
  }

/* Sets animations */

  @media screen and (min-width: 960px) {
    .animation_logo{
      animation-name: change_logo;
      animation-duration: 7s;
      animation-fill-mode: forwards;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_logo_after{
      position: relative;
      animation-name: change_logo_after;
      animation-duration: 1s;
      animation-fill-mode: forwards;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_logo_before{
      position: relative;
      animation-name: change_logo_before;
      animation-duration: 1s;
      animation-fill-mode: forwards;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_button{
      position: relative;
      animation-name: change_button;
      animation-duration: 0.5s;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_message{
      animation-name: change_message;
      animation-delay:3s;
      animation-duration: 3s;
      animation-fill-mode: forwards;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_form{
      position: relative;
      animation-name: change_form;
      animation-duration: 1s;
      animation-fill-mode: forwards;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_form_back{
      position: relative;
      animation-name: change_form_back;
      animation-duration: 1s;
      animation-fill-mode: forwards;
    }
  }

  @media screen and (min-width: 960px) {
    .animation_icons{
      animation-name: change_icons;
      animation-delay: 6s;
      animation-duration: 2s;
      animation-fill-mode: forwards;
    }
  }

/* Fixes responsive and size stuff for min-width of 960px */

  @media screen and (min-width:960px) {
    .logo_poweb{
      left: 40%;
    }
    .info_text{
      font-size: 1.6vw!important;
      line-height: normal;
      margin-top: 2vh !important;
    }
    h1{
      font-size: 3.4vw !important;  
      line-height: normal;
      margin-top: 6vh !important;
    }
    .info_icons{
      font-size: 1.4vw !important;
      margin-top: -1vh !important;
    } 
    .social_icons{
      visibility: hidden;
      left:30vw !important; 
    }
    .message_col{
      position: absolute;
      left: 0%;
      height:100%;
      background-color: #47b1e3 !important;
      visibility: hidden;
    }
    .form_col{
      position: absolute;
      top: 6%;
      left: 40%;
      visibility: hidden;
    }
  }

/* Fixes responsive and size stuff for min-width of 1264px */

  @media screen and (min-width:1264px) {
    .info_text{
      font-size: 1.4vw!important;
      line-height: normal;
      margin-top: 2vh !important;
    }
    h1{
      font-size: 3vw !important;  
      line-height: normal;
      margin-top: 6vh !important;
    }
    .info_icons{
      font-size: 1vw !important;
      margin-top: -1vh !important;
    } 
    .social_icons{
      visibility: hidden;
      left:35vw !important; 
    }
    .form_col{
      left: 30%;
    }
  }

/* Fixes responsive and size stuff for min-width of 1560px */

  @media screen and (min-width:1560px) {
    .info_text{
      font-size: 1.4vw !important;
      line-height: normal;
      margin-top: 0.5vh !important;
    }
    h1{
      font-size: 2.5vw !important;  
      line-height: normal;
      margin-top: 5vh !important;
    }
    .info_icons{
      font-size: 0.9vw !important;
      margin-top: 0vh !important;
    } 
    .social_icons{
      visibility: hidden;
      left:40vw !important; 
    }
    .form_col{
      left: 30%;
    }
    .icon_size{
      font-size: 2vw !important;
    }
    .text_field{
      height: 4vw !important;
    }
    textarea{
      height: 8vw !important;
      margin-top: 0.8vw !important;
      padding-top: 0.2vw !important;
    }
    #open_button{
      background-image: url('../assets/Mensager.svg');
      background-size: cover;
      min-width: 60px;
      min-height: 60px;
      width: 3vw;
      height: 3vw;
    }
    #close_button{
      min-width: 60px;
      min-height: 60px;
      width: 3vw;
      height: 3vw;
    }
    #send_button{
      min-width: 80px;
      min-height: 60px;
      width: 4vw;
      height: 2vw;
      font-size: 0.8vw !important;
    }
    .v-input{
      font-size: 1vw !important;
    }
    .v-input input{
      max-height: inherit !important;
      padding-top: 0.5vw !important;
      padding-bottom: 0.2vw !important;
    }
    .v-label{
      font-size: 1vw !important;
      height: 3vw !important;
      padding-top: 0.7vw !important;
    }
    .v-text-field__slot{
      padding-top: 0.2vw !important;
    }
    .v-messages{
      font-size: 0.7vw !important;
      padding-top: 0.3vw !important;
      padding-bottom: 0.4vw !important;
    }
  }

/* Stops animations */

  .resize-animation-stopper :is(.animation_icons, .animation_logo, .animation_message) {
    animation: none !important;
    transition: none !important;
  }

</style>