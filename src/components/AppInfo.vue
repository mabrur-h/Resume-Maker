<template>
  <div className="card card-w70">
    <app-title></app-title>
    <app-avatar></app-avatar>
    <app-text></app-text>
    <app-subtitle></app-subtitle>
  </div>
</template>

<script>
import AppAvatar from "@/components/Parts/AppAvatar";
import AppTitle from "@/components/Parts/AppTitle";
import AppText from "@/components/Parts/AppText";
import AppSubtitle from "@/components/Parts/AppSubtitle";

export default {
name: "AppInfo",
  components: {AppSubtitle, AppText, AppTitle, AppAvatar}
}
</script>

<style scoped>

</style>