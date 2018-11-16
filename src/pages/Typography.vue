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
            <h5 class="title">Login</h5>
          </a>
        </div>
        <div slot="footer" class="button-container">
          <div class="row">
            <div class="col-md-12 pr-md-1">
              <base-input label="Usuário"
                        v-model="usuario">
              </base-input>
            </div>            
          </div>
          <div class="row">
            <div class="col-md-12 pr-md-1">
              <base-input label="Senha:"
                        v-model="senha">
              </base-input>
            </div>            
          </div>
        <base-button slot="footer" type="primary"  @click="validarSenha" fill>Login</base-button>
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
        usuario: '',
        senha: ''
      }
    },
    methods: {
      validarSenha: function () {
        if (this.usuario !== 'Fabio') {
          this.notifyVue('top', 'right')
          return 0
        }
        if (this.senha !== 'Fabio'){
          this.notifyVue('top', 'right')
          return 0
        }
        this.$router.push({ name: 'dashboard' })
      },
      notifyVue(verticalAlign, horizontalAlign) {
        const color = Math.floor(Math.random() * 4 + 1);
        this.$notify({
          component: NotificationTemplate,
          icon: "tim-icons icon-alert-circle-exc",
          horizontalAlign: horizontalAlign,
          verticalAlign: verticalAlign,
          type: this.type[color],
          timeout: 2000
        });
      }
    }
  };
</script>
<style>
</style>
