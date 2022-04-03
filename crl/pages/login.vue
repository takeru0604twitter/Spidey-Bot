<template>
    <div>
        <div class="form-control mt-64">
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
            <div class="flex justify-center -mr-96">
            <button class="btn mt-10 -mr-96">ログイン</button>
            <a class="link mt-36 mr-24">アカウントをお持ちでない方</a>
        </div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>