<template>
  <section class="container posts-page">
    <el-card>
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table :data="showPosts" style="width: 100%" class="table">
        <el-table-column label="タイトル" prop="title"></el-table-column>
        <el-table-column label="投稿者" prop="user.id" width="180"></el-table-column>
        <el-table-column label="投稿日時" prop="created_at" width="240"></el-table-column>
      </el-table>
    </el-card>
  </section>
</template>

<script>
export default {
  computed: {
    showPosts() {
      return [
        {
          id: '001',
          title: 'How to develop Nuxt',
          body: 'Lorem ipsum dolor sit amet , ',
          created_at: '2018/08/10 12:00:00',
          user: {
            id: 'potato4d'
          }
        },
        {
          id: '002',
          title: 'Dev to app Nuxt to Heroku',
          body: 'Lorem ipsum dolor sit amet, consectetur adipsiscing elit...',
          created_at: '2018/08/10 13:00:00',
          user: {
            id: 'potato4d'
          }
        },
      ]
    }
  }
}
</script>

<style>
.posts-page .el-table__row {
  cursor: pointer;
}
</style>