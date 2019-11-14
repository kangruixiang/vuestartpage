<template>
  <div>
    <v-container fluid fill-height>
      <v-layout row wrap justify-center align-center>
        <v-card
          class="ma-8 pa-3"
          width="300px"
          v-for="category in categories"
          v-bind:key="category"
        >
          <v-card-title>{{category.name}}</v-card-title>
          <v-divider></v-divider>
          <v-list>
            <v-list-item link v-for="item in category.sites" v-bind:key="item" :href="item.url">
              <v-list-item-content>
                <v-list-item-title>{{item.name}}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
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