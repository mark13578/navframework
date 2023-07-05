<template>
    <h1>
      <img class="icon" src="../assets/logo.png" alt="" />
      <slot>這是預設的內容喔</slot>
    </h1>
  </template>
  
  <style lang="scss">
  h1 {
    display: flex;
    align-items: center;
    color: cadetblue;
    > img.icon {
      display: block;
      width: 30px;
      margin-right: 10px;
    }
  }
  </style>
  