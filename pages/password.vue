<template>
    <v-app id="back">
        <v-layout column justify-center align-center>
            <v-flex xs12 sm12 md12>

                <div class="text-xs-center">
                    <img src="/locked.png" alt="Vuetify.js" class="ma-5" />
                </div>

                <h5 class="title" ma->Enter your username and I will give you your password ! </h5>

                <v-text-field name="input-1-3" label="Username" single-line></v-text-field>
                <div class="text-xs-center">
                    <v-btn primary flat outline @click.native.stop="dialog = !dialog">Take me my password</v-btn>
                </div>
    
            </v-flex>
    
            <v-dialog absolute v-model="dialog">
                <v-card>
                    <v-card-text>
                        <p class="text-xs-center">1234</p>
                    </v-card-text>
                    <v-card-actions class="text-xs-center">
                        <v-spacer></v-spacer>
                        <v-btn flat primary outline @click.native="dialog = false" router nuxt to="/">Back to login</v-btn>
                    </v-card-actions>
                </v-card>
            </v-dialog>
    
        </v-layout>
    </v-app>
</template>

<script>
export default {
    data() {
        return {
            dialog: false
        }
    }
}
</script>
<style scoped>
#back { 
    
  background-image: url("/bg.jpg");
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;

  
}
.title {
    color: #4e342e;
}
</style>

