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
            <label class="label ">
                <span class="label-text flex juify-center">Your password</span>
            </label>
            <label class="input-group flex juify-center">
                <span>password</span>
                <input type="text"  class="input input-bordered">
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