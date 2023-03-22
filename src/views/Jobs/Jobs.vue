<template>
  <div v-for="item in data">
    <router-link :to="{name:'jobDetail', params:{id:item.id}}">
      <h1>
        {{ item.name }}
      </h1>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          name: "Rana",
          id: 1012,
          description: `corporis hic et est quasi voluptatem sunt distinctio quas, aspernatur nostrum vero
            tenetur dolore consequuntur necessitatibus sequi. Rem soluta sint quaerat aspernatur, 
        facilis dolor voluptate quisquam nisi dolorum.`,
        },
        {
          name: "Subhan",
          id: 1013,
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. 
        Quis ea voluptatem fugiat laboriosam optio provident,
         at impedit nostrum laudantium dolor?`,
        },
      ],
    };
  },
};
</script>

<style>
div a {
  font-weight: bold;
  text-decoration: none;
 
}
</style>
