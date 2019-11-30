<template>
  <div>
    <v-container fluid fill-height>
      <v-layout row align-center>
        <v-flex v-for="category in categories" v-bind:key="category">
          <v-card class="ma-8 pa-3 deep-purple lighten-5">
            <v-card-title>{{category.name}}</v-card-title>
            <v-divider></v-divider>
            <v-list class="deep-purple lighten-5">
              <v-list-item link v-for="item in category.sites" v-bind:key="item" :href="item.url">
                <v-list-item-content>
                  <v-list-item-title>{{item.name}}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "BlockContainer",
  props: ["categories"]
};
</script>

<style scoped>
</style>