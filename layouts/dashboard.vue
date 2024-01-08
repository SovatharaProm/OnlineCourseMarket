<template>
  <div class="drawer">
    <div>
      <div>
        <h1 class="font-bold text-center text-[#2B348F] text-2xl py-[2rem] px-[1rem]">
          Paragon Academy
        </h1>
      </div>
      <ul>
        <router-link to="/" tag="li" class="font-bold text-4xl router-link" exact>
      <Icon name="material-symbols:home-rounded" class="text-4xl icon" /> Home
    </router-link>
    <router-link to="/instructor/courses" tag="li" class="font-bold text-4xl router-link" exact>
      <Icon name="material-symbols:book-4" class="text-4xl icon" /> Courses
    </router-link>
    <router-link to="/instructor/instructorprofile" tag="li" class="font-bold text-4xl router-link" exact>
  <Icon name="material-symbols:account-circle-outline" class="text-4xl icon" /> Profile
    </router-link>
      </ul>
    </div>
    <div>
      <p class="font-bold signOut-btn flex items-center">
        <Icon name="mdi-light:logout" class="text-4xl" />Sign out
      </p>
    </div>
  </div>
  <div class="content-wrapper">
    <div class="user-area">
      <div class="user-action">
        <div class="px-2">
          <img
            src="https://docs.material-tailwind.com/img/face-2.jpg"
            alt="avatar"
            class="relative inline-block h-10 w-10 rounded-[9px] object-cover object-center" />
        </div>
        <div><span class="font-bold text-xl">User Profile</span></div>
      </div>
    </div>
    <slot />
  </div>
</template>

<script></script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta:wght@400;700&display=swap');

/* Applying consistent font styles */
.font-bold {
  font-weight: 700;
  font-family: 'Plus Jakarta', sans-serif;
}

.text-center {
  text-align: center;
}
.drawer {
  width: 15%;
  height: 100%;
  background-color: #fff;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  ul {
    display: flex;
    flex-direction: column;
    justify-content: center;
    li {
      padding: 0.5rem 25%;
      font-weight: bold;
      font-size: 1.3rem;
      color: #8a8a8a;
      display: flex;
      align-items: flex-end;
    }
  }
}

.signOut-btn {
  padding: 0.5rem 25%;
  font-weight: bold;
  font-size: 1.3rem;
  color: #2b348f;
  margin-bottom: 4rem;
}
.content-wrapper {
  padding: 3rem 3rem 0rem 3rem;
  width: 85%;
  height: 100%;
  position: fixed;
  background: #f0f7ff;
  right: 0;
  top: 0;
  overflow: scroll;
}
.user-area {
  width: 100%;
  display: flex;
  justify-content: flex-end;
  margin-bottom: 1%;
}
.user-action {
  padding: 0.5rem;
  display: flex;
  align-items: flex-end;
  align-items: center;

  background: white;
  width: fit-content;
  border-radius: 14px;
}
/* Your existing global styles... */

/* Styling for router-link elements */
.router-link {
  list-style: none; /* Remove default list styles */
  display: flex; /* Display as flexbox */
  align-items: center; /* Align items vertically */
  padding: 0.5rem; /* Adjust padding as needed */
  cursor: pointer; /* Show cursor on hover */
  transition: background-color 0.3s ease; /* Smooth background color transition */
}

.router-link:hover {
  background-color: #f0f0f0; /* Change background color on hover */
}

/* Style for the icons inside router-link */
.router-link .icon {
  margin-right: 0.5rem; /* Adjust spacing between icon and text */
  font-size: 2rem; /* Adjust icon size */
}
.router-link li
{

  padding: 0.5rem 25%;
  font-weight: bold;
  font-size: 1.3rem;
  color: #8a8a8a;
  display: flex;
  align-items: flex-end;
}

/* You can adjust these styles further based on your design preferences */

</style>
