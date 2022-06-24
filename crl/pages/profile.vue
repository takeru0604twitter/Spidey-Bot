<template>
    <div class="form-control">
      <div class="ml-auto">
        <div class="input-group">
          <input type="text" placeholder="Search" class="input input-bordered ">
          <button class="btn btn-square ">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 " fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
          </button>
        </div> 
      </div>
      <div class="ml-48">
        プレイヤー情報
      </div>
      <div class="display flex">
        <div class="ml-48">
          名前
        </div>
       <div class="ml-16">
        クラン名
        </div>
       <div class="ml-32">
        プレイヤータグ
       </div>
       <div class="ml-6">
        トロフィー
       </div>
      </div>
      <div class="display flex">
        <div class="ml-48">
          {{ name }}
        </div>
        <div class="ml-10">
          {{clan}}
        </div>
      <div class="ml-10">
        {{tag}}
      </div>
      <div class="ml-10">
        {{trophy}}
      </div>
      </div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'

interface Card{
  name:string
  id:number
  level:number
  starlevel:number
  maxlevel:number
  count:number
  iconUrls:{
    medius: string
  }
}

interface Data {
  name?: string
  clan?: string
  tag?: string
  trophy?: string
  deck:Card[]
}

const token = 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiIsImtpZCI6IjI4YTMxOGY3LTAwMDAtYTFlYi03ZmExLTJjNzQzM2M2Y2NhNSJ9.eyJpc3MiOiJzdXBlcmNlbGwiLCJhdWQiOiJzdXBlcmNlbGw6Z2FtZWFwaSIsImp0aSI6ImZkYmVhYzU4LWI5MjgtNDUzMS05ZTBjLTYzYWNjOGIyMDcwZCIsImlhdCI6MTY1NjA4NDk0MCwic3ViIjoiZGV2ZWxvcGVyLzA5YzJmZmMxLTAyZjItMTI5My1hOWU5LTFmNWI5NTJjZjE5NCIsInNjb3BlcyI6WyJyb3lhbGUiXSwibGltaXRzIjpbeyJ0aWVyIjoiZGV2ZWxvcGVyL3NpbHZlciIsInR5cGUiOiJ0aHJvdHRsaW5nIn0seyJjaWRycyI6WyIyMjMuMjUyLjkzLjE0Il0sInR5cGUiOiJjbGllbnQifV19.KcvNoqCJHuB65Sw-lecRNTnj-MHYXAScnv4TK5rGzMqcbR1RbmndHAakuAAEYmhSLuBDsK1IJEKYmwiLw4PZ6w'

export default Vue.extend({
  name: 'IndexPage',
  data(): Data {
    return {
      name: undefined,
      clan: undefined,
      tag: undefined,
      trophy: undefined,
      deck: []
    }
  },
  mounted() {
    const url = "/api/players/%238Q8Q08CC"
    this.$axios.get(url, {
      headers: {
        Authorization: `Bearer ${token}`
      }
    })
    .then(response  => {
      console.log('response', response)
      this.name = response.data.name
      this.tag = response.data.tag
      this.trophy = response.data.trophies
      this.clan = response.data.clan.name
    })
  }


})
</script>