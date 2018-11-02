<template>
  <div class="row">
    <div class="col-md-12">
      <user-card :user="user" style="height:250px"></user-card>
    </div>
    <div class="col-md-12">
      <edit-profile-form :model="model">
      </edit-profile-form>
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
          company: '',
          email: '',
          username: '',
          data: '',
          firstName: '',
          lastName: '',
          address: '',
          city: '',
          country: '',
          about: ''
        },
        user: {
          fullName: '',
          title: '',
          description: ``,
        }
      }
    }
  }
</script>
<style>
</style>
