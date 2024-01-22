<template>
  <div className='container'>
    <div className='options-container'>
      <img alt="Vue logo" class="logo" src="@/assets/logo.svg" />
      <nav class="nav">
        <RouterLink class="link" to="/">Home</RouterLink>
        <RouterLink class="link" to="/about">About</RouterLink>
        <RouterLink class="link" to="/characters">Characters</RouterLink>
      </nav>
    </div>
  </div>
 </template>
 
 <style scoped>
 .container {
  padding: 0.8rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #282c34;
  color: white;
}

.options-container {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.nav {
  gap: 2rem;
  display: flex;
}

.link {
  font-weight: bold;
  color: white;
  text-decoration: none;
  display: initial;

  &:hover {
    text-decoration: underline;
    background-color: unset;
  }
}

.logo {
  width: 50px;
}
 
 @media (max-width: 480px) {
  .nav {
    gap: 1rem;
  }
 }

 @media (max-width: 320px) {
  .nav {
    gap: 0;
  }
 }
 </style>
 