<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/">Home Page</nuxt-link></li>
        <li><nuxt-link to="/products">Products</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style>
  header {
    width: 100%;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(9,32,60,0.85);
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  li {
    margin: 0 10px;
  }

  a {
    text-decoration: none;
    color: white;
  }

</style>
