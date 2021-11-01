<template>
    <!-- <div class="main">
        <Sidebar/>
        <Menu/>
    </div>    -->
    <div class="container">
    <Logo />

    <ValidationObserver v-slot="{ invalid }" class="form">
      <h1>{{ $t('title') }}</h1>
      
      <!-- Name -->
      <ValidationProvider name="Username" rules="required" v-slot="{ errors }">
        <input v-model="name" type="text" placeholder="Name">
        <span class="error">{{ errors[0] }}</span>
      </ValidationProvider>

      <!-- Email -->
      <ValidationProvider name="Email" rules="required|email" v-slot="{ errors }">
        <input v-model="email" type="email" placeholder="Email">
        <span class="error">{{ errors[0] }}</span>
      </ValidationProvider>

      <!-- Password -->
      <ValidationProvider name="Password" vid="confirm" rules="required" v-slot="{ errors }">
        <input v-model="password" type="password" placeholder="Password">
        <span class="error">{{ errors[0] }}</span>
      </ValidationProvider>

      <!-- Confirm Password -->
      <ValidationProvider name="Confirm password" rules="required|confirmed:confirm" v-slot="{ errors }">
        <input v-model="confirmPassword" type="password" placeholder="Confirm password">
        <span class="error">{{ errors[0] }}</span>
      </ValidationProvider>

      <button>Submit</button>
    </ValidationObserver>
  </div>
</template>

<style lang="scss">
div {
    margin: 0;
    padding: 0;
}

.main {
    display: flex;
    @media(max-width: 722px) {
        flex-wrap: wrap;
        flex-direction: column;
    }
}
</style>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      password: '',
      confirmPassword: '',
      locale: 'en'
    }
  }
}
</script>
