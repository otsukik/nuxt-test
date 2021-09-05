<template>
  <div class="container">
    <div class="students-area">
      <h2>生徒一覧</h2>
      <NuxtLink to="/students">生徒の情報を見る</NuxtLink>
    </div>
    <div class="management-area">
      <h2>管理者</h2>
      <NuxtLink to="/management">管理画面を見る</NuxtLink>
    </div>
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>

<style scoped>
h2 {
  margin-bottom: 0;
}
.students-area {
  margin-right: 60px;
}
</style>
