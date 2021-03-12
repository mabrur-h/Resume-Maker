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

    <button className="btn primary" :disabled="!(textArea.length > 3)">Добавить</button>
  </form>
</template>

<script>
export default {
  emits: ['add-block'],
  name: "AppForm",
  data() {
  return {
    textType: 'title',
    textArea: ''
  }
  },
  methods: {
  submitForm() {
    this.$emit('block-added', {
      type: this.textType,
      value: this.textArea,
      id: Date.now()
    })

    this.textArea = ''
    this.textType = 'title'
  },
  }
}
</script>

<style scoped>

</style>