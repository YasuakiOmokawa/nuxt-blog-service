<template>
  <section class="container posts-page">
    <el-card>
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table :data="showPosts" style="width: 100%" class="table" @row-click="handleClick">
        <el-table-column label="タイトル" prop="title"></el-table-column>
        <el-table-column label="投稿者" prop="user.id" width="180"></el-table-column>
        <el-table-column label="投稿日時" prop="created_at" width="240"></el-table-column>
      </el-table>
    </el-card>
  </section>
</template>

<script>
import moment from "~/plugins/moment"
import { mapGetters } from "vuex"

export default {
  async asyncData({ store }) {
    await store.dispatch("posts/fetchPosts")
  },
  computed: {
    showPosts() {
      return this.posts.map(post => {
        post.created_at = moment(post.created_at).format("YYYY/MM/DD HH:mm:ss")
        return post
      })
    },
    ...mapGetters("posts", ["posts"])
  },
  methods: {
    handleClick(post) {
      this.$router.push(`/posts/${post.id}`)
    }
  }
}
</script>

<style>
.posts-page .el-table__row {
  cursor: pointer;
}
</style>