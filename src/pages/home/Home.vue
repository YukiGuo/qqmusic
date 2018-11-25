<template>
    <div>
        <home-head></home-head>
      <!--   <song-list :list = "playlist"></song-list> -->
    </div>
</template>
<script >
import HomeHead from './components/Head'
// import SongList from './components/SongList'
// import axios from 'axios'
export default {
  name: 'Home',
  data () {
    return {
      playlist: []
    }
  },
  components: {
    HomeHead,
    // SongList
  }
  /*methods: {
    getHomeInfo () {
      axios.get('/static/mock/data.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if(res.ret && res.data ) {
        const data = res.data
        this.playlist = data.playlist
      }


    }
  },
  mounted () {
    this.getHomeInfo()
  }*/
}
</script>

<style ></style>
