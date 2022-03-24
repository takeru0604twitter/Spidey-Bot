<template>
    <div>
        <div class="form-control ">
            <label class="label  flex justify-center">
                <span class="label-text">>Your email</span>
            </label>
            <label class="input-group flex justify-center">
                <span>email</span>
                <input type="text" class="input input-bordered">
            </label>
        </div>
        <div class="form-control">
            <label class="label flex justify-center">
                <span class="label-text">Your password</span>
            </label>
            <label class="input-group flex justify-center">
                <span>password</span>
                <input type="text"  class="input input-bordered">
            </label>
        </div>
        <button class="btn">login</button>
        <a class="link">アカウントをお持ちでない方</a>


    </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>