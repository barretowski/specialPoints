<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="10">
        <v-card class="elevation-6 mt-10">
          <v-window v-model="step">
            <v-window-item :value="1">
              <v-row>
                <v-col cols="12" md="6">
                  <v-card-text class="mt-12">
                    <h4 class="text-center">Entre na sua conta</h4>
                    <h6 class="text-center  grey--text ">Faça login na sua conta para continuar gerenciando ou explorando
                      suas tarefas/pontuações</h6>
                    <v-row align="center" justify="center">
                      <v-col cols="12" sm="8">

                        <v-text-field label="Email" outlined dense color="blue" autocomplete="false" class="mt-16" />
                        <v-text-field label="Senha" outlined dense color="blue" autocomplete="false" type="password" />
                        <v-row>
                          <v-col cols="12" sm="7">
                            <v-checkbox label="Lembrar login" class="mt-n1" color="blue"> </v-checkbox>
                          </v-col>
                          <v-col cols="12" sm="5">
                            <span class="caption blue--text">Esqueci a senha</span>
                          </v-col>
                        </v-row>
                        <v-btn color="blue" dark block tile>Entrar</v-btn>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-col>
                <v-col cols="12" md="6" class="blue rounded-bl-xl">
                  <div style="  text-align: center; padding: 180px 0;">
                    <v-card-text class="white--text">
                      <h3 class="text-center ">Não tem uma conta ainda?</h3>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step++">Registre-se</v-btn>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>
            <v-window-item :value="2">
              <v-row>
                <v-col cols="12" md="6" class="blue rounded-br-xl">
                  <div style="  text-align: center; padding: 180px 0;">
                    <v-card-text class="white--text">
                      <h3 class="text-center ">Já se cadastrou?</h3>
                      <h6 class="text-center">Faça o login em sua conta</h6>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step--">Entrar</v-btn>
                    </div>
                  </div>
                </v-col>

                <v-col cols="12" md="6">
                  <v-card-text class="mt-12">
                    <h4 class="text-center">Cadastre-se</h4>
                    <h6 class="text-center  grey--text ">Vamos preparar tudo para que você possa<br>
                      começar a criar sua primeira experiência</h6>
                    <v-row align="center" justify="center">
                      <v-col cols="12" sm="8">
                        <v-row>
                          <v-col cols="12" sm="6">
                            <v-text-field label="Nome" outlined dense color="blue" autocomplete="false"
                              class="mt-4" />
                          </v-col>
                          <v-col cols="12" sm="6">
                            <v-text-field label="Sobrenome" outlined dense color="blue" autocomplete="false"
                              class="mt-4" />
                          </v-col>
                        </v-row>
                        <v-text-field label="Email" outlined dense color="blue" autocomplete="false" />
                        <v-text-field label="Senha" outlined dense color="blue" autocomplete="false" type="password" />

                        <v-btn color="blue" dark block tile>Confirmar</v-btn>
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
    step: 1
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
</style>