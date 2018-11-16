<template>
    <div class="row">
      <div class="col-12">
        <card :title="table1.title">
          <div class="table-responsive">
            <base-table :data="tableData"
                        :columns="tableColumns"
                        thead-classes="text-primary">
            </base-table>
          </div>
        </card>
        <base-button slot="footer" type="primary" @click="rota" fill>Editar uma peça</base-button>
      </div>
    </div>
</template>
<script>
import { BaseTable } from "@/components";

export default {
  components: {
    BaseTable
  },
  data() {
    return {
      table1: {
        title: "Peças em cartaz",
      },
      tableColumns: ["nome", "data", "assentos", "horario", "Valor"],
      tableData: [
        {
          id: 1,
          nome: "Sonho de uma noite de verão",
          valor: "R$ 36",
          assentos: '50',
          data: "03/11",
          horario: '10h30',
        },
        {
          id: 2,
          nome: "O Lago dos Cisnes",
          valor: "R$ 23",
          assentos: '48',
          data: "13/11",
          horario: '11h30' 
        },
        {
          id: 3,
          nome: "Hairspray ",
          valor: "R$ 56",
          assentos: '30',
          data: "27/11",
          horario: '15h30'      
        },
        {
          id: 4,
          nome: "As Aventuras de João e Maria",
          valor: "R$ 38",
          assentos: '1',
          data: "15/11",
          horario: '16h50'
        },
        {
          id: 5,
          nome: "Porque os Homens Mentem?",
          valor: "R$ 63",
          assentos: '12',
          data: "19/11",
          horario: '20h00'
        },
        {
          id: 6,
          nome: 'A morte do caixeiro viajante',
          valor: 'R$ 98',
          assentos: '14',
          data: '03/11',
          horario: '21h30'        
        },
        {
          id: 7,
          nome: 'Ópera do malandro',
          valor: 'R$ 78',
          assentos: '4',
          data: '05/11',
          horario: '17h00'       
        },
      ]
    }
  },
  methods: {
    rota () {
      this.$router.push('Cadastro de Sessões')
    }
  }
};
</script>
<style>
</style>
