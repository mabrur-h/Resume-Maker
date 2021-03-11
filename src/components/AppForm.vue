<template>
  <form className="card card-w30" @submit.prevent="submitForm">
    <div className="form-control">
      <label htmlFor="type">Тип блока</label>
      <select id="type" v-model="textType">
        <option value="title">Заголовок</option>
        <option value="subtitle">Подзаголовок</option>
        <option value="avatar">Аватар</option>
        <option value="text">Текст</option>
      </select>
    </div>

    <div className="form-control">
      <label htmlFor="value">Значение</label>
      <textarea id="value" rows="3" v-model="textArea"></textarea>
    </div>

    <button className="btn primary">Добавить</button>
  </form>
</template>

<script>
export default {
name: "AppForm",
  data() {
  return {
    textType: '',
    textArea: ''
  }
  },
  methods: {
  submitForm() {
    console.log(this.textType)
    console.log(this.textArea)
  }
  }
}
</script>

<style scoped>

</style>