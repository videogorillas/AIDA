<template lang="html">
    <v-flex xs12>

        <!-- Adjust which tools are activated.  -->
       <v-list two-line subheader>
           <v-list-item v-for="tool in config.tools" :key="tool.name">
               <v-list-tile avatar>

                   <v-list-tile-action>
                       <v-checkbox v-model="tool.include"></v-checkbox>
                   </v-list-tile-action>

                   <v-list-tile-content>
                       <v-list-tile-title> {{ tool.name }} </v-list-tile-title>
                       <v-list-tile-sub-title> {{ tool.caption }}</v-list-tile-sub-title>
                   </v-list-tile-content>

               </v-list-tile>
           </v-list-item>
       </v-list>

   </v-flex>
</template>

<script>
export default {

    props: ['config'],

    data() {
        return {

        }
    }
}
</script>

<style lang="css">
</style>
