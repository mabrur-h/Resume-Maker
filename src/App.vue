<template>
  <div className="container column">
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

    <div className="card card-w70">
      <h1>Резюме Nickname</h1>
      <div className="avatar">
        <img src="https://cdn.dribbble.com/users/5592443/screenshots/14279501/drbl_pop_r_m_rick_4x.png">
      </div>
      <h2>Опыт работы</h2>
      <p>
        главный герой американского мультсериала «Рик и Морти», гениальный учёный, изобретатель, атеист (хотя в
        некоторых сериях он даже молится Богу, однако, каждый раз после чудесного спасения ссылается на удачу и вновь
        отвергает его существование), алкоголик, социопат, дедушка Морти. На момент начала третьего сезона ему 70
        лет[1]. Рик боится пиратов, а его главной слабостью является некий - "Санчезиум". Исходя из того, что существует
        неограниченное количество вселенных, существует неограниченное количество Риков, герой сериала предположительно
        принадлежит к измерению С-137. В серии комикcов Рик относится к измерению C-132, а в игре «Pocket Mortys» — к
        измерению C-123[2]. Прототипом Рика Санчеза является Эмметт Браун, герой кинотрилогии «Назад в будущее»[3].
      </p>
      <h3>Добавьте первый блок, чтобы увидеть результат</h3>
    </div>
  </div>
  <div className="container">
    <p>
      <button className="btn primary">Загрузить комментарии</button>
    </p>
    <div className="card">
      <h2>Комментарии</h2>
      <ul className="list">
        <li className="list-item">
          <div>
            <p><strong>test@microsoft.com</strong></p>
            <small>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi, reiciendis.</small>
          </div>
        </li>
      </ul>
    </div>
    <div className="loader"></div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.avatar {
  display: flex;
  justify-content: center;
}

.avatar img {
  width: 150px;
  height: auto;
  border-radius: 50%;
}
</style>
