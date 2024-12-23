<template>
  <div class="header__divider">
    <hr />
  </div>
</template>

<style scoped>
.header__divider {
  width: 100%;
  display: none;
}

.header__divider hr {
  height: 2px;
  background-color: #C3D1C6;
  border: none;
  margin: 18px 0;
  width: 100%;
}

@media screen and (max-width: 510px) {
  .header__divider {
    display: block;
  }
}
</style>
