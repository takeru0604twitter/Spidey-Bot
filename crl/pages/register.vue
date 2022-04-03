<template>
  <div>
    <div class="form-control mt-64">
      <label class="input-group flex justify-center">
        <span>プレイヤータグ</span>
       <input type="text" class="input input-bordered">
      </label>
    </div>
    <div class="form-control mt-20">
      <label class="input-group flex justify-center">
        <span>メールアドレス</span>
        <input type="text" class="input input-bordered">
      </label>
    </div>
    <div class="form-control mt-20">
      <label class="input-group flex justify-center">
        <span>パスワード</span>
        <input type="text" class="input input-bordered">
      </label>
    </div>
    <div class="flex justify-center -mr-72">
      <button class="btn mt-10 -mr-96">作成</button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>