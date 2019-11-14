<template>
  <div>
    <v-container>
      <v-row>
        <v-col v-for="category in categories" v-bind:key="category">
          <v-card>
            <v-card-title class="cyan darken-1">{{category.name}}</v-card-title>
            <v-list>
              <v-list-item link v-for="item in category.sites" v-bind:key="item" :href="item.url">
                <v-list-item-content>
                  <v-list-item-title>{{item.name}}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-card>
        </v-col>
      </v-row>
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