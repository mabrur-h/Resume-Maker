<template>
  <div className="container column">
    <AppForm @block-added="blockAdd"></AppForm>
    <AppInfo ></AppInfo>
  </div>
  <div className="container">
    <AppComments></AppComments>
  </div>
</template>

<script>
import AppForm from "@/components/AppForm";
import AppInfo from "@/components/AppInfo";
import AppComments from "@/components/AppComments";

export default {
  components: {AppComments, AppForm, AppInfo},
  data() {
    return {
      blocks: []
    }
  },
  methods: {
    blockAdd() {
      this.blocks.push('title')
      console.log(this.blocks)
    }
  }
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
