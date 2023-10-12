<template>
  <div class="home-container">
    <h1>welcome {{ name }}!</h1>
    <v-card v-if="!haveTodos" class="mt-16 mx-auto" width="450px">
      <div class="no-todo">
        <h2>Looks like you have no tasks to do at the moment</h2>
        <v-card-actions>
          <v-btn color="blue" class="white--text" @click="goToCreatePage"
            >ADD</v-btn
          >
        </v-card-actions>
      </div>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      haveTodos: false,
      name: 'uday',
    }
  },
  head() {
    return {
      title: 'My Tasks',
    }
  },
}
</script>
<style>
.home-container {
  margin-top: 50px;
}
.no-todo {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
