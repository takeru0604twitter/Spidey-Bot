<template>
  <div>
    <div class="form-control">
      <label class="label">
        <span class="label-text">your playertag</span>
      </label>
      <label class="input-group">
        <span>tag</span>
       <input type="text" class="input input-bordered">
      </label>
    </div>
    <div class="form-control">
      <label class="label">
        <span class="label-text">Your email</span>
      </label>
      <label class="input-group">
        <span>email</span>
        <input type="text" class="input input-bordered">
      </label>
    </div>
    <div class="form-control">
      <label class="label">
        <span class="label-text">Your password</span>
      </label>
      <label class="input-group">
        <span>password</span>
        <input type="text" class="input input-bordered">
      </label>
    </div>

  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>