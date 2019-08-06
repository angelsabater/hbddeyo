<template>
  <v-layout 
    class="mainBackground">
    <v-flex >
      <v-btn 
        to="/james" 
        class="mx-2"
        fab dark large color="blue"
        style="position: absolute; top: 300px; left: 250px"
      >
        <v-icon dark>← tura</v-icon>
      </v-btn>
      <v-btn 
        to="/deo"
        class="mx-2" 
        fab dark large 
        color="blue"
        style="position: absolute; top: 300px; right: 250px"
      >
          <v-icon dark>deo →</v-icon>
      </v-btn>

    </v-flex>
</v-layout>
</template>