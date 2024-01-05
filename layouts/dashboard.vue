<template>
  <div class="drawer">
    <div>
      <div>
        <h1 class="font-bold text-center text-[#2B348F] text-2xl py-[2rem] px-[1rem]">
          Paragon Academy
        </h1>
      </div>
      <ul>
        <li class="font-bold">
          <Icon name="material-symbols:home-rounded" class="text-4xl" />Home
        </li>
        <li class="font-bold"><Icon name="material-symbols:book-4" class="text-4xl" />Course</li>
        <li class="font-bold">
          <Icon name="material-symbols:account-circle-outline" class="text-4xl" />Profile
        </li>
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
      align-items: end;
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
</style>
