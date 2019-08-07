<template>
  <v-app>
    <v-content>
      <v-container fluid>
        <v-layout wrap>    
                
          <v-flex xs12 sm6 md3>
            <v-text-field outlined solo flat label="Nome"></v-text-field>
          </v-flex>

          <v-flex xs12 sm6 md3 offset-md1>
            <v-radio-group v-model="row" row>
              <v-radio label="Masculino" value="radio-1"></v-radio>
              <v-radio label="Feminino" value="radio-2"></v-radio>
            </v-radio-group>
          </v-flex>

        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      column: null,
      row: null,
    }
  },
}
</script>
