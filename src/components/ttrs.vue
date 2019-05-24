<template>
  <div class="ttrs">
    <table>
      <tr v-for="hei in height" :key="hei.id">
        <td v-for="wid in width" :key="wid.id"></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data(){
    return{
      width:[
        " "," "," "," "," "," "," "," "," "," ",
      ],
      height:[
        " "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," "," ",
      ],
      intervalId: undefined
    }
  },
    mounted () {
      var array = [
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 1, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 1, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 1, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 1, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
          [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
      ];


      drow()
      this.intervalId = setInterval(function () {
        drow()
      }, 1000)
    },
    beforeDestroy () {
      console.log('clearInterval')
      clearInterval(this.intervalId)
    }
}
</script>

<style lang="scss" scoped>
table {
    margin: 0 auto; /* 中央寄せ */
    width: 200px;
    height: 400px;
}
td {
    width: 10%; /* 横10マス */
    height: 5%; /* 縦20マス */
}
.default {
    background-color: #455A64;
}
.stick {
    background-color: #03A9F4;
}
</style>
