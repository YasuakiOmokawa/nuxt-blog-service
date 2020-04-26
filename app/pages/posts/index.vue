<template>
  <section class="container posts-page">
    <el-card>
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table
        :data="showPosts"
        style="width: 100%"
        class="table"
      >
        <el-table-column
          label="タイトル"
          prop="title"
        >
        </el-table-column>
        <el-table-column
          label="投稿者"
          prop="user.id"
          width="180"
        >
        </el-table-column>
        <el-table-column
          label="投稿日時"
          prop="created_at"
          width="240"
        >
        </el-table-column>
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

        }
      ]
    }
  }
}
</script>