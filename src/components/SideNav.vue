<template>
  <v-container fluid fill-height>
    <v-btn color="pink" dark @click.stop="drawer = !drawer">Toggle</v-btn>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img
              src="https://awe-some-media.s3.ap-northeast-1.amazonaws.com/wp-content/uploads/2016/10/03023515/gorilla-752875_960_720-300x213.jpg"
            />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>Gorilla</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list-item v-for="(item, index) in items" :key="index">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      items: [{ title: "連絡先一覧", icon: "mdi-menu" }],
    };
  },
};
</script>