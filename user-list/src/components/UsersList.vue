<template>
  <h1 class="text-center my-5">User List</h1>
  <v-card class="mx-auto" max-width="450">
    <v-list>
      <v-list-item v-for="item in users" :key="item.id" :prepend-avatar="item.image">
        <v-list-item-title class="font-weight-bold my-2">{{ item.name }}</v-list-item-title>
        <v-list-item-subtitle class="my-2 multi-line-item">{{ item.about }}</v-list-item-subtitle>
      </v-list-item>
    </v-list>
  </v-card>
</template>

<style>
.multi-line-item{
  -webkit-line-clamp: initial!important;
}
</style>

<script>
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'John',
          about: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos blanditiis tenetur. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos blanditiis tenetur. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos blanditiis tenetur. Quos blanditiis tenetur. Quos blanditiis tenetur. Quos blanditiis tenetur.',
          image: 'https://picsum.photos/200'
        },
        {
          id: 2,
          name: 'Jane',
          about: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos blanditiis tenetur',
          image: 'https://picsum.photos/200'
        },
        {
          id: 3,
          name: 'Joe',
          about: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos blanditiis tenetur',
          image: 'https://picsum.photos/200'
        }
      ]
    }
  }
}
</script>
