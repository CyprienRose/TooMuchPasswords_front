<template>
  <v-app id="back" :style="{ backgroundImage: 'url(/bg.jpg)' }">
    <v-layout column justify-center align-center>
      <v-flex xs12 sm12 md12>
  
        <div class="text-xs-center">
          <img src="/locked.png" alt="Vuetify.js" class="ma-5" />
        </div>

        <div class="text-xs-center">
          <v-btn v-bind:class="[signin ? 'activeClass' : '', 'border-b', 'border-r']" 	 primary flat @click.native.stop="signin = true">Sign In</v-btn>
          <v-btn v-bind:class="[signin ? '' : 'activeClass', 'border-b']" 	 primary flat @click.native.stop="signin = false">Sign Up</v-btn>
        </div>
    
        <div v-if="signin">
          <v-text-field name="input-1-3" label="Username" single-line prepend-icon="perm_identity"></v-text-field>
          <v-text-field name="input-1-3" label="Password" :append-icon="e1 ? 'visibility' : 'visibility_off'" :append-icon-cb="() => (e1 = !e1)" :type="e1 ? 'password' : 'text'" single-line prepend-icon="lock_outline"></v-text-field>
  
          <div class="text-xs-center">
            <v-btn primary flat outline nuxt to="/inspire">Sign In</v-btn>
            <br>
            <a class="ma-10 fpassword" flat  href="/password">Forgot password ?</a>
          </div>
        </div>
  
        <div v-if="!signin">
          <v-text-field name="input-1-3" label="Username" single-line prepend-icon="perm_identity"></v-text-field>
          <v-text-field name="input-1-3" label="Password" :append-icon="e1 ? 'visibility' : 'visibility_off'" :append-icon-cb="() => (e1 = !e1)" :type="e1 ? 'password' : 'text'" single-line prepend-icon="lock_outline"></v-text-field>
          <v-text-field name="input-1-3" label="Confirm your password" :append-icon="e1 ? 'visibility' : 'visibility_off'" :append-icon-cb="() => (e1 = !e1)" :type="e1 ? 'password' : 'text'" single-line prepend-icon="lock_outline"></v-text-field>
  
          <div class="text-xs-center">
            <v-btn primary flat outline nuxt to="/inspire">Sign Up</v-btn>
          </div>
  
        </div>
  
      </v-flex>
    </v-layout>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      signin: true,
      e1: true
    }
  }
}
</script>

<style scoped>
.fpassword {
  color: rgba(0, 0, 0, 0.54);
  text-decoration: none;
  transition: all 0.40s ease;
  opacity: 0.5;
}


.fpassword:hover {
  opacity: 1;
  color: #8d6e63;
}

.border-b{
  margin-left: 0px;
  border-bottom: thin solid #8d6e63;
}
.border-r{
  margin-right: 0px;
  border-right: thin solid #8d6e63;
}

.activeClass{
  background-color: rgba(0,0,0,.20) !important;
}
</style>