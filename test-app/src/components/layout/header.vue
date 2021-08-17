<template>
  <header>
    <div>
      <label for="">Ім'я</label>

      <input type="text" v-model="user.first_name" />
    </div>

    <div>
      <label for="">Прізвище</label>

      <input type="text" v-model="user.last_name" />
    </div>

    <div class="avatar">{{ initials }}</div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      user: {
        first_name: "",
        last_name: "",
      },
    };
  },
  computed: {
    initials() {
      var letters = "AB";
      if (
        this.user.first_name &&
        !this.user.last_name &&
        this.user.first_name.length >= 2
      ) {
        letters = this.user.first_name[0] + this.user.first_name[1];
      }
      if (this.user.first_name && this.user.last_name) {
        letters = this.user.first_name[0] + this.user.last_name[0];
      }
      return letters.toUpperCase();
    },
  },
  components: {},
};
</script>

<style lang="scss">
</style>