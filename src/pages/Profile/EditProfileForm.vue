<template>
  <card>
    <h5 slot="header" class="title">Nova Sessão</h5>
    <div class="row">
      <div class="col-md-5 pr-md-1">
        <base-input label="Nome da Peça"
                  placeholder="Ex. Nome da Peça"
                  v-model="model.company">
        </base-input>
      </div>
      <div class="col-md-3 px-md-1">
        <base-input label="Faixa Etária"
                  placeholder="Ex: +18"
                  v-model="model.username">
        </base-input>
      </div>
      <div class="col-md-4 pl-md-1">
        <label class="control-label">Data da Peça*</label>
        <br>
        <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css">
        <el-date-picker
          v-model="model.data"
          type="date"
          placeholder="Escolha o dia da Peça"
          format="DD/MM/yyyy">
        </el-date-picker>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6 pr-md-1">
        <base-input label="Valor da Entrada"
                  v-model="model.firstName"
                  placeholder="Ex. R$ 50,00">
        </base-input>
      </div>
      <div class="col-md-6 pl-md-1">
        <base-input label="Capacidade Máxima"
                  v-model="model.lastName"
                  placeholder="Ex. 50 pessoas">
        </base-input>
      </div>
    </div>
    <div class="row">
      <div class="col-md-8">
        <base-input>
          <label>Sinopse da Peça</label>
          <textarea rows="4" cols="80"
                    class="form-control"
                    placeholder="Faça um resumo da nova Peça"
                    v-model="model.about">

              </textarea>
        </base-input>
      </div>
    </div>
    <base-button slot="footer" type="primary" @click="rota" fill>Salvar</base-button>
  </card>
</template>
<script src="https://unpkg.com/element-ui/lib/index.js"></script>

<script>
  import { BaseAlert } from '@/components';
  import {
    DatePicker,
    Select,
    Option
  } from 'element-ui'


  export default {
    components: {

      [DatePicker.name]: DatePicker,
      [Option.name]: Option,
      [Select.name]: Select
    },
    props: {
      model: {
        type: Object,
        default: () => {
          return {};
        }
      }
    },
    methods:{
      rota () {
        alert('Peça salva com sucesso!')
        this.$router.push('dashboard')
      },
    }
  }
</script>
<style>
</style>
