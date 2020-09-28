<template>
  <div>
    <form @submit.prevent="onSubmit()">
      <input v-model="form.password" type="text" placeholder="Password">
      <input v-model="form.confirmPassword" type="text" placeholder="Confrm Password">
      <button type="submit">Submit</button>
    </form>
  </div>
</template>
<script>
export default {
  data () {
    return {
      form: {
        password: '',
        confirmPassword: '',
        user_key: this.$route.query.key
      }
    }
  },
  methods: {
    onSubmit () {
      console.log(this.form)
    }
  }
}
</script>
