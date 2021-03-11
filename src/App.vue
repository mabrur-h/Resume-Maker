<template>
  <div className="container column">
    <app-form></app-form>
    <app-info></app-info>
  </div>
  <div className="container">
    <p>
      <button className="btn primary" @click="loadComments">Загрузить комментарии</button>
    </p>
    <app-comments></app-comments>
  </div>
</template>

<script>
import AppForm from "@/components/AppForm";
import AppInfo from "@/components/AppInfo";
import AppComments from "@/components/AppComments";

export default {
  components: {AppComments, AppForm, AppInfo}

}
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
