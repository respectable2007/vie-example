<template>
  <div class="canvas"
       @mouseenter='showHigh'
       @mouseout='showDown'>
    <canvas id='five' width="800" height="800"></canvas>
  </div>
</template>

<script>
export default {
  name: 'canvas',
  mounted () {
    let contain = document.getElementById('five')
    let cxt = contain.getContext('2d')
    this.canvas = cxt
    this.showDown()
  },
  data () {
    return {
      canvas: null
    }
  },
  methods: {
    showHigh () {
      let cxt = this.canvas
      cxt.clearRect(0, 0, 800, 800)
      for (let i = 0; i < 5; i++) {
        cxt.beginPath()
        cxt.lineWidth = 1
        cxt.moveTo(127 + 150 * Math.cos((i * 72) / 180 * Math.PI), 200 + 150 * Math.sin((i * 72) / 180 * Math.PI))
        cxt.lineTo(127 + 150 * Math.cos(((i + 1) * 72) / 180 * Math.PI), 200 + 150 * Math.sin(((i + 1) * 72) / 180 * Math.PI))
        cxt.strokeStyle = 'rgb(54,138,242)'
        cxt.stroke()
        cxt.fill()
        cxt.beginPath()
        cxt.lineWidth = 1
        cxt.arc(127 + 150 * Math.cos((i * 72) / 180 * Math.PI), 200 + 150 * Math.sin((i * 72) / 180 * Math.PI), 4, 0, 2 * Math.PI, false)
        cxt.strokeStyle = 'rgb(54,138,242)'
        cxt.fillStyle = '#fff'
        cxt.stroke()
        cxt.fill()
      }
    },
    showDown () {
      let cxt = this.canvas
      cxt.clearRect(0, 0, 800, 800)
      let coors = [
      [127 + 150 * Math.cos((0 * 72) / 180 * Math.PI), 200 + 150 * Math.sin((0 * 72) / 180 * Math.PI)],
       [127 + 140 * Math.cos((1 * 72) / 180 * Math.PI), 200 + 140 * Math.sin((1 * 72) / 180 * Math.PI)],
        [127 + 130 * Math.cos((2 * 72) / 180 * Math.PI), 200 + 130 * Math.sin((2 * 72) / 180 * Math.PI)],
         [127 + 140 * Math.cos((3 * 72) / 180 * Math.PI), 200 + 140 * Math.sin((3 * 72) / 180 * Math.PI)],
          [127 + 150 * Math.cos((4 * 72) / 180 * Math.PI), 200 + 150 * Math.sin((4 * 72) / 180 * Math.PI)]]
      for (let i = 0; i < coors.length; i++) {
        cxt.beginPath()
        cxt.lineWidth = 1
        cxt.moveTo(coors[i][0], coors[i][1])
        if (i !== 4) {
          cxt.lineTo(coors[i + 1][0], coors[i + 1][1])
        } else {
          cxt.lineTo(coors[0][0], coors[0][1])
        }
        cxt.strokeStyle = 'rgb(54,138,242)'
        cxt.stroke()
        cxt.fill()
        cxt.beginPath()
        cxt.lineWidth = 1
        cxt.arc(coors[i][0], coors[i][1], 4, 0, 2 * Math.PI, false)
        cxt.strokeStyle = 'rgb(54,138,242)'
        if (i % 2) {
          cxt.strokeStyle = 'red'
          cxt.fillStyle = 'red'
        } else {
          cxt.fillStyle = '#fff'
        }
        cxt.stroke()
        cxt.fill()
      }
    }
  }
}
</script>

<style scoped>
.canvas{
  background-image: url('./../assets/rate.png');
  background-repeat: no-repeat;
}
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
.kefu{
  position: fixed;
  top: 50%;
  margin-top: -40px;
  right: 10px;
}
</style>
