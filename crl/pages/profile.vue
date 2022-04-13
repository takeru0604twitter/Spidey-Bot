<template>
    <div class="form-control ">
      <div class="input-group">
        <input type="text" placeholder="Search" class="input input-bordered ">
        <button class="btn btn-square ">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 " fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
        </button>
        {{ name }}
      </div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

interface Data {
  name?: string
}

const token = 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiIsImtpZCI6IjI4YTMxOGY3LTAwMDAtYTFlYi03ZmExLTJjNzQzM2M2Y2NhNSJ9.eyJpc3MiOiJzdXBlcmNlbGwiLCJhdWQiOiJzdXBlcmNlbGw6Z2FtZWFwaSIsImp0aSI6ImFhNzM0NTYyLTg2OGQtNGE2OC05ZTdlLWZmZjM2YjU4NmE2MiIsImlhdCI6MTY0OTgzOTQyNCwic3ViIjoiZGV2ZWxvcGVyLzA5YzJmZmMxLTAyZjItMTI5My1hOWU5LTFmNWI5NTJjZjE5NCIsInNjb3BlcyI6WyJyb3lhbGUiXSwibGltaXRzIjpbeyJ0aWVyIjoiZGV2ZWxvcGVyL3NpbHZlciIsInR5cGUiOiJ0aHJvdHRsaW5nIn0seyJjaWRycyI6WyIyMDIuMTU3LjIzMC4xOTMiXSwidHlwZSI6ImNsaWVudCJ9XX0.CS3jKOgMr0BkWugZx9JbrQ8YfMb4UPNmMUhx1D93noZkMjvlj6uRe5WCculvODp2zdy7d0yy9ZjsYiNub00ziQ'

export default Vue.extend({
  name: 'IndexPage',
  data(): Data {
    return {
      name: undefined
    }
  },
  mounted() {
    const url = "/api/players/%238Q8Q08CC"
    this.$axios.get(url, {
      headers: {
        Authorization: `Bearer ${token}`
      }
    })
    .then(response => {
      console.log('response', response)
      this.name = response.data.name
    })
  }
})
</script>