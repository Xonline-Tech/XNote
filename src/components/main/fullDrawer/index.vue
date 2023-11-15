<script lang="ts">
export default {
  name: "fullDrawer",
  data() {
    return {
      widgets_cards: [
        {
          title: 'Favorites',
          type: 'list', //list,clist,tree
          icon: 'heart'

        }, {
          title: 'Pen',
          type: 'list', //list,clist,tree
          icon: 'pen-nib'

        }, {
          title: 'Download',
          type: 'list', //list,clist,tree
          icon: 'download'

        },
      ]
    }
  }
}
</script>

<template>
  <!--Space Info-->
  <v-card class="ma-2" elevation="3" color="primary">
    <v-card-title>
      <v-avatar class="mr-2">
        <v-img src="https://api.dicebear.com/7.x/rings/svg?seed=Coco"></v-img>
      </v-avatar>
      <strong>Space Title</strong>
    </v-card-title>
  </v-card>
  <!--Widgets-->
  <v-card v-for="(card,index) in widgets_cards"
          class="ma-2 pa-0"
          elevation="3"
          rounded
          density="comfortable"
          :title="card.title"
          prepend-avatar="https://cdn.vuetifyjs.com/images/logos/v-alt.svg">
    <template v-slot:append>
      <v-btn icon variant="plain">
        <v-icon :icon="'fas fa-'+card.icon" color="success"></v-icon>
      </v-btn>
    </template>
    <v-card-item>
      <v-list>
        <v-list-item>
          111
        </v-list-item>
      </v-list>
    </v-card-item>
  </v-card>
  <v-spacer/>
  <v-btn-group class="ma-2" elevation="3" rounded>
    <v-btn>
      <v-icon icon="fas fa-magnifying-glass"></v-icon>
    </v-btn>
    <v-btn>
      <v-icon icon="fas fa-diagram-project"></v-icon>
    </v-btn>
    <v-btn>
      <v-icon icon="fas fa-plus"></v-icon>
    </v-btn>
  </v-btn-group>

</template>

<style scoped>
</style>