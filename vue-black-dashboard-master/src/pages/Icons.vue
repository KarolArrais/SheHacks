<template>
  <div class="row">
    <div class="col-md-aaa">
        <h1>
          Membros de LOA
        </h1>
      <user-card :user="user"></user-card>
      <user-card :user="user"></user-card>
      <user-card :user="user"></user-card>
    </div>
  </div>
</template>
<script>
  import EditProfileForm from './Profile/EditProfileForm';
  import UserCard from './Profile/UserCard'
  export default {
    components: {
      EditProfileForm,
      UserCard
    },
    data() {
      return {
        model: {
          company: 'Creative Code Inc.',
          email: 'mike@email.com',
          username: 'michael23',
          firstName: 'Joice',
          lastName: 'Lee Otsuka',
          address: 'Bld Mihail Kogalniceanu, nr. 8 Bl 1, Sc 1, Ap 09',
          city: 'Melbourne',
          country: 'Australia',
          about: 'Lamborghini Mercy, Your chick she so thirsty, I\'m in that two seat Lambo.'
        },
        user: {
          fullName: 'Joice Lee Otsuka',
          title: 'Prof. Dr.',
          description: `Orientadora do Laboratório, trabalha com IHC e jogos educativos educacionais. Atualmente trabalha desenvolvendo alguns projetos.`,
        }
      }
    }
  }
</script>
<style>
#col-md-aaa{
  width: 100%;
}
</style>
