<template>
    <div>
        <div class="form-control mt-56">
            <label class="label flex justify-center">
                <span class="label-text">>Your email</span>
            </label>
            <label class="input-group flex justify-center ">
                <span>email</span>
                <input type="text" class="input input-bordered">
            </label>
        </div>
        <div class="form-control mt-10">
            <label class="label flex justify-center">
                <span class="label-text">Your password</span>
            </label>
            <label class="input-group flex justify-center">
                <span>password</span>
                <input type="text" class="input input-bordered">
            </label>
        </div>
            <div class="flex justify-center -mr-96">
            <button class="btn mt-10 -mr-96">login</button>
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