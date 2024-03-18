```html
<meta charset="UTF-8">
<canvas width="800" height ="400"> </canvas>
    
<script>
    var tela = document.querySelector('canvas')
    var pincel = tela.getContext('2d')

    pincel.font = '36px Georgia'
    pincel.fillStyle = 'black'
    pincel.fillText('Limpar a Tela',20,50)


    function desenharElipse(){
        pincel.fillStyle = 'blue'
        pincel.beginPath()
        pincel.ellipse(200,200,50,40,2 * Math.PI, 0, 2 * Math.PI)
        pincel.fill() 
    }

    function apagarAElipse(){
        pincel.clearRect(150,160,100,80)
    }

    var fase = "cheia"

    function desenhaLimpa(){
        if (fase == "cheia") {
            apagarAElipse()
            fase = "apagada"
        }
        else{
            desenharElipse()
            fase = "cheia"
        }
    }

    setInterval(desenhaLimpa, 2000)
          

</script>
```
