<template>
  <section class="container">
    <el-card style="flex: 1">
      <div slot="header" class="clearfix">
        <span>ログイン</span>
      </div>
      <form>
        <div class="form-content">
          <span>ユーザー ID</span>
          <el-input v-model="formData.id" placeholder />
        </div>
        <div class="form-content"></div>
      </form>
    </el-card>
  </section>
</template>

<script>
export default {}
</script>

<style>
</style>