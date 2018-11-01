<template>
  <card>
    <h5 slot="header" class="title">Nova Sessão</h5>
    <div class="row">
      <div class="col-md-5 pr-md-1">
        <base-input label="Nome da Peça"
                  placeholder="Ex. Nome da Peça"
                  v-model="model.company"
                  >
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
          placeholder="Pick a day"
          format="DD/MM/yyyy">
        </el-date-picker>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6 pr-md-1">
        <base-input label="First Name"
                  v-model="model.firstName"
                  placeholder="First Name">
        </base-input>
      </div>
      <div class="col-md-6 pl-md-1">
        <base-input label="Last Name"
                  v-model="model.lastName"
                  placeholder="Last Name">
        </base-input>
      </div>
    </div>
    <div class="row">
      <div class="col-md-12">
        <base-input label="Address"
                  v-model="model.address"
                  placeholder="Home Address">
        </base-input>
      </div>
    </div>
    <div class="row">
      <div class="col-md-4 pr-md-1">
        <base-input label="City"
                  v-model="model.city"
                  placeholder="City">
        </base-input>
      </div>
      <div class="col-md-4 px-md-1">
        <base-input label="Country"
                  v-model="model.country"
                  placeholder="Country">
        </base-input>
      </div>
      <div class="col-md-4 pl-md-1">
        <base-input label="Postal Code"
                  placeholder="ZIP Code">
        </base-input>
      </div>
    </div>
    <div class="row">
      <div class="col-md-8">
        <base-input>
          <label>About Me</label>
          <textarea rows="4" cols="80"
                    class="form-control"
                    placeholder="Here can be your description"
                    v-model="model.about">

              </textarea>
        </base-input>
      </div>
    </div>
    <base-button slot="footer" type="primary" fill>Save</base-button>
  </card>
</template>
<script src="https://unpkg.com/element-ui/lib/index.js"></script>

<script>
  
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
    }
  }
</script>
<style>
</style>
