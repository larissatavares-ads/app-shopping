<template>
  <q-page>
    <div class="column justify-center">
      <div class="col-11 column q-gutter-sm">
        <q-card class="row col-4" v-for="evento in eventos" :key="evento.id">
          <q-img :src="evento.imagem" :ratio="16/9"/>
          <q-card-section class="col-12">
            <div class="text-h6">{{ evento.nome }}</div>
          </q-card-section>
          <q-card-section class="row">
            <div class="col-8 row">
              <span class="text-weight-medium"> Localização: </span>
              <span class="q-pl-sm"> {{ evento.localizacao }} </span>
            </div>
            <div class="col-8 row justify-between">
              <span class="text-weight-medium"> Período: </span>
              <span> {{ evento.periodo }} </span>
            </div>
            <div class="col-8 row">
              <span class="text-weight-medium"> Loja: </span>
              <span class="q-pl-sm"> {{ evento.loja }} </span>
            </div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  data () {
    return {
      eventos: [
        {
          id: '97a24e70-79b3-4791-904c-ba8206718608',
          nome: 'Saldão Magalu',
          imagem: '../../public/images/magalu.jpg',
          localizacao: '1º piso',
          loja: 'Magazine Luiza',
          periodo: '01/10/2023 - 10/10/2023'
        },
        {
          id: '5521023a-dde6-45e1-9b58-f90ff9c33ca5',
          nome: 'Feirão de Computadores',
          imagem: '../../public/images/sol.jpg',
          localizacao: '1º piso',
          loja: 'SOL',
          periodo: '09/10/2023 - 12/10/2023'
        },
        {
          id: '9490426b-7ff1-49db-83c9-dbf407400e31',
          nome: 'Sarau de poesia',
          imagem: '../../public/images/saraiva.jpg',
          localizacao: '4º piso',
          loja: 'Saraiva',
          periodo: '09/10/2023 - 12/10/2023'
        }
      ]
    }
  }
})
</script>
