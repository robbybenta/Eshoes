<template>
  <div>
    <v-app-bar flat class="transparent mt-5 mx-5">
      <v-img
        src="https://i.imgur.com/Hqme6OL.png"
        aspect-ratio="4"
        contain
      ></v-img>
      <v-col cols="12" sm="6" md="6" class="ma-auto pa-0  d-flex align-center">
        <v-text-field
          label="Solo"
          placeholder="Apa yang ingin anda cari ?"
          solo
          class="ma-0 pa-0"
        ></v-text-field>
      </v-col>
      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item v-for="n in 5" :key="n" @click="() => {}">
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </div>
</template>
<script>
export default {}
</script>
<style></style>
