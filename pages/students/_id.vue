<template>
  <div class="student_id">
    <div class="student_id-detail">
      <h2>{{ getStudentName }}</h2>
      <ul class="link-list">
        <li class="link"><NuxtLink to="/students">生徒一覧に戻る</NuxtLink></li>
        <li class="link"><NuxtLink to="/">トップページへ</NuxtLink></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    // return this.students.some(student => student.id === params.id)
    return /^[0-9a-z]{16}$/.test(params.id);
  },
  data() {
    return {
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  },
  computed: {
    getStudentName() {
      return this.students.filter(student => student.id === this.$route.params.id)[0].name;
    }
  }
};
</script>

<style>
.student_id {
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
.link-list {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  padding: 0;
}
.link:not(:last-child)::after {
  content: "|";
  display: inline-block;
  padding: 0 6px;
}
</style>
