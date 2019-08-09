<template>
  <v-app>
    <v-content>
      <v-container fluid>
        <v-layout wrap>    
                
          <v-flex xs12 sm6 md3>
            <p>Nome</p>
            <v-text-field outlined solo flat v-model="name"></v-text-field>
          </v-flex>

          <v-flex xs12 sm6 md3 offset-md1>
            <p>Sexo</p>
            <v-radio-group row v-model="sexo">
              <v-radio label="Masculino" value="M"></v-radio>
              <v-radio label="Feminino" value="F"></v-radio>
            </v-radio-group>
          </v-flex>

          <v-flex xs12 sm6 md5 >
            <v-btn class="ma-2" outlined v-on:click="salvar">Adicionar</v-btn>
          </v-flex>

        </v-layout>

        <v-layout>
          <v-data-table
            :headers="headers"
            :items="pessoas"
            :items-per-page="5"
            class="elevation-1"
          ></v-data-table>
        </v-layout>

      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      headers: [
        {
          text: 'Nome',
          align: 'left',
          sortable: false,
          value: 'name',
        },
        {
          text: 'Sexo',
          value: 'sexo',
        },

      ],
      pessoas: [],
      column: null,
      row: null,
    }
  },
  methods:{
    salvar(){
      this.pessoas.push({name:this.name, sexo:this.sexo})
    }
  },
}
</script>
