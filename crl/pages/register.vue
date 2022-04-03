<template>
  <div>
    <div class="form-control mt-56">
      <label class="label flex justify-center">
        <span class="label-text">your playertag</span>
      </label>
      <label class="input-group flex justify-center">
        <span>tag</span>
       <input type="text" class="input input-bordered">
      </label>
    </div>
    <div class="form-control mt-10">
      <label class="label flex justify-center">
        <span class="label-text">Your email</span>
      </label>
      <label class="input-group flex justify-center">
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
    <button class="btn mt-10 flex justify-center">login</button>

  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>