<template>
    <div class="profile">
      <div class="profile-header">
        <!-- Profile picture -->
        <img src="assets/images/Yuumi.png" alt="Profile Picture" class="profile-pic">
      </div>
      <div class="profile-info">
        <h2>Profile Information</h2>
        <form @submit.prevent="updateProfile">
          <div class="form-group">
            <label for="fullName">Full Name:</label>
            <input type="text" id="fullName" v-model="fullName">
          </div>
          <div class="form-group">
            <label for="dob">Date Of Birth:</label>
            <input type="date" id="dob" v-model="dateOfBirth">
          </div>
          <div class="form-group">
            <label for="password">Change Password:</label>
            <input type="password" id="password" v-model="password">
          </div>
          <div class="form-group">
            <label for="fullName">About me</label>
            <input type="text" id="fullName" v-model="Aboutme">
          </div>
          <div class="form-group">
            <label for="fullName">Biography</label>
            <input type="text" id="fullName" v-model="bio">
          </div>
          <div class="form-group">
            <label for="fullName">Website</label>
            <input type="text" id="fullName" v-model="website">
          </div>
          <div class="form-group">
            <label for="fullName">Linkedin</label>
            <input type="text" id="fullName" v-model="linkedin">
          </div>
          <div class="form-group">
            <label for="fullName">Twitter</label>
            <input type="text" id="fullName" v-model="Twitter">
          </div>
          <div class="button">
          <button type="submit">Save Profile</button>
        </div>
        </form>
      </div>
    </div>
  </template>
  
  <script>
import Dashboard from '~/layouts/dashboard.vue';
definePageMeta({
  layout: 'dashboard',
});
import { ref } from 'vue';
export default {
    components: {
        Dashboard
        
    },
    data() {
    return {
      fullName: '',
      dateOfBirth: '',
      password: '',
      Aboutme: '',
      bio: '',
      website: '',
      linkedin: '',
      Twitter: ''
    };
  },
  methods: {
    updateProfile() {
      // Handle updating profile logic here
      console.log('Profile updated:', {
        fullName: this.fullName,
        dateOfBirth: this.dateOfBirth,
        password: this.password,
        Aboutme: this.Aboutme,
        bio: this.bio,
        website: this.website,
        linkedin: this.linkedin,
        Twitter: this.Twitter
      });
    },
  },
};

  </script>
  
  <style>
  /* Style your profile page as needed */
  .profile {
  display: flex;
  flex-direction: column;
  align-items: center; /* Align items in the center horizontally */
  padding: 20px;
}

.profile-header {
  padding: 10px;
}

.profile-pic {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-right: 15rem;
}

.profile-info {
  margin-top: 20px; /* Adjust the margin between picture and form */
}
.profile-info h2 {
  margin-top: 20px;
  font-weight: bold;
}

.form-group {

    margin-bottom: 20px;
}
  
  input[type="text"],
  input[type="date"],
  input[type="password"] {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
.button {
    padding: 10px 10px;
    background-color: #2B348F;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    width: 7rem;
  }
  </style>
  