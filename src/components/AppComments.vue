<template>
  <app-loader v-if="loading"></app-loader>
  <div className="card" v-else>
    <h2>Комментарии</h2>
    <ul className="list">
      <li className="list-item" v-for="comment in comments" :key="comment.id">
        <div>
          <p><strong>{{ comment.email }}</strong></p>
          <small>{{ comment.body }}</small>
        </div>
      </li>
    </ul>
    <button @click="loadComments">load</button>
  </div>
</template>

<script>
import AppLoader from "@/components/AppLoader";
export default {
name: "AppComments",
  components: {AppLoader},
  data() {
    return {
      comments: [],
      loading: false
    }
  },
  methods: {
    async loadComments() {
      try {
        this.loading = true
        const response = await fetch('https://jsonplaceholder.typicode.com/comments?_limit=42', {
          method: 'GET',
          headers: {
            'Content-Type': 'application/json'
          },
        })

        const commentsData = await response.json()
        commentsData.map(comment => {
          this.comments.push({
            postId: comment.postId,
            id: comment.id,
            firstName: comment.firstName,
            email: comment.email,
            body: comment.body
          })
          this.loading = false
        })

        console.log(this.comments)
      } catch (e) {
        console.log(e)
      }
    }
  }
}
</script>

<style scoped>

</style>