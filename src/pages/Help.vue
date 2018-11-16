<template>
  <div class="row">
    <div class="col-md-12">
      <card type="user">
        <p class="card-text">
        </p>
        <div class="author">
          <div class="block block-one"></div>
          <div class="block block-two"></div>
          <div class="block block-three"></div>
          <div class="block block-four"></div>
          <a href="#">
            <img class="avatar" src="img/thandera.jpg" alt="...">
            <h5 class="title">Suporte Técnico</h5>
          </a>
        </div>
        <div slot="footer" class="button-container">
          <div class="row">
            <div class="col-md-12 pr-md-1">
              <base-input label="Nome do Associado"
                        v-model="nome">
              </base-input>
            </div>            
          </div>
          <div class="row">
            <div class="col-md-12 pr-md-1">
              <base-input label="Digite seu E-Mail"
                        v-model="email">
              </base-input>
            </div>            
          </div>
          <div class="row">
            <div class="col-md-12 pr-md-1">
              <base-input>
                <label>Descreva a ocorrência</label>
                <textarea rows="4" cols="80"
                          class="form-control"
                          placeholder="Faça um resumo da ocorrência"
                          v-model="texto">
                </textarea>
              </base-input>
            </div>            
          </div>
        <base-button slot="footer" type="primary"  @click="validarOcorrencia" fill>Salvar Ocorrencia</base-button>
        </div>
      </card>
    </div>
  </div>
</template>
<script>
  import NotificationTemplate from './Notifications/NotificationTemplate'
  import EditProfileForm from './Profile/EditProfileForm';
  import UserCard from './Profile/UserCard'
  export default {
    components: {
      EditProfileForm,
      UserCard
    },
    data() {
      return {
        type: ["", "info", "success", "warning", "danger"],
        notifications: {
          topCenter: false
        },
        nome: '',
        email: '',
        texto: ''
      }
    },
    methods: {
      validarOcorrencia: function () {
        if (this.nome && this.email && this.texto){
          this.$notify({
            group: 'foo',
            title: 'Aguarde o contato de nossa equipe em até 24h',
            text: 'Hello user! This is a notification!'
          })
        } else {
          this.$notify({
            group: 'foo',
            title: 'Preencha todos os campos corretamente!',
            text: 'Hello user! This is a notification!'
          })
        }
      },
    }
  };
</script>
<style>
</style>
