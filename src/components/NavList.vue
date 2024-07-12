<!-- src/components/Nav.vue -->
<template>
    <nav>
      <ul>
        <li><router-link to="/">首页</router-link></li>
        <li><router-link to="/crit-calculator">暴击计算器</router-link></li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'NavList'
  }
  </script>
  
  <style>
  nav ul {
    list-style-type: none;
    padding: 0;
  }
  nav ul li {
    display: inline;
    margin-right: 10px;
  }
  </style>
  