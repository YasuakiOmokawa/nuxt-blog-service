<template>
  <div>
    <el-row v-if="user">
      <el-col :span="6">
        <el-card class="text-center" style="margin-right: 16px;">
          <div>
            <img src="https://placehold.it/150x150"
            style="witdh: 100%;margin-bottom: 16px;border-radius: 2px;"
            alt=""
            />
          </div>
          <h2>
            <b>{{user.id}}</b>
          </h2>
        </el-card>
      </el-col>
      <el-col :span="18">

      </el-col>
    </el-row>
  </div>
</template>