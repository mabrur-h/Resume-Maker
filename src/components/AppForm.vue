<template>
  <form className="card card-w30">
    <div className="form-control">
      <label htmlFor="type">Тип блока</label>
      <select id="type">
        <option value="title">Заголовок</option>
        <option value="subtitle">Подзаголовок</option>
        <option value="avatar">Аватар</option>
        <option value="text">Текст</option>
      </select>
    </div>

    <div className="form-control">
      <label htmlFor="value">Значение</label>
      <textarea id="value" rows="3"></textarea>
    </div>

    <button className="btn primary">Добавить</button>
  </form>
</template>

<script>
export default {
name: "AppForm"
}
</script>

<style scoped>

</style>