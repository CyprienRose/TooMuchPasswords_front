  <template>
  <div>
     <v-toolbar class="brown lighten-1" light dense>
        <v-toolbar-title class="title">Too Much Passwords</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon class="brown--text text--lighten-4">exit_to_app</v-icon>
        </v-btn>
      </v-toolbar>
  <nuxt/>

    <v-bottom-nav absolute value="true" class="transparent">
      <v-btn flat dark class="brown--text" @click.native="e1 = 1" :value="e1 === 1" nuxt to="/add">
         <span>Add</span>
        <v-icon>add_circle_outline</v-icon>
      </v-btn>
      <v-btn flat dark class="brown--text"  @click.native="e1 = 2" :value="e1 === 2" nuxt to="/list">
       <span>List</span>
        <v-icon>format_list_bulleted</v-icon>
      </v-btn>
      <v-btn flat dark class="brown--text" @click.native="e1 = 3" :value="e1 === 3" nuxt to="/settings">
        <span>Settings</span>
        <v-icon>settings</v-icon>
      </v-btn>
    </v-bottom-nav>
</div>

  </template>

  <script>
  export default {
    data () {
      return {
        e1: 2
      }
    }
  }
</script>
<style>
.title {
    color: #d7ccc8;
}

</style>