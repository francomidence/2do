<template>
  <div>
    <v-app id="inspire">
      <v-card class="mx-auto">
        <v-system-bar color="orange darken-2"></v-system-bar>

        <v-toolbar color="orange" dark>
          <v-toolbar-title>Descubre mediante</v-toolbar-title>

          <div class="flex-grow-1"></div>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
        </v-toolbar>
        <v-container class="pa-2" fluid>
          <v-row>
            <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
              <v-card hover>
                <v-img
                  :src="card.src"
                  class="white--text"
                  height="200px"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                >
                  <v-card-title
                    class="fill-height align-end"
                    v-text="card.title"
                  ></v-card-title>
                </v-img>

                <v-card-actions>
                  <div class="flex-grow-1"></div>

                  <v-btn icon>
                    <v-icon>mdi-heart</v-icon>
                  </v-btn>

                  <v-btn icon>
                    <v-icon>mdi-bookmark</v-icon>
                  </v-btn>

                  <v-btn icon>
                    <v-icon>mdi-share-variant</v-icon>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-app>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: 'Ubicacion',
          src:
            'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Openstreetmap_logo.svg/1024px-Openstreetmap_logo.svg.png',
          flex: 10
        },
        {
          title: 'Precio',
          src:
            'http://www.0800flor.net/wp-content/uploads/2018/05/C%C3%B3mo-establecer-el-precio-ideal-de-tus-producto.png',
          flex: 6
        },
        {
          title: 'Categoria',
          src:
            'https://as1.ftcdn.net/jpg/01/03/40/74/500_F_103407461_fF7BP05EdOA9w2v3PdRUxnSTefo5Ugh0.jpg',
          flex: 6
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>
