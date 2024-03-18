```html
<meta charset="UTF-8">

<canvas width="1920" height ="1080"> </canvas>
    
<script>
    var tela = document.querySelector('canvas');
    var pincel = tela.getContext('2d');

    pincel.font = '36px Georgia'
    pincel.fillStyle = 'black'
    pincel.fillText('Clique aqui para desenhar o círculo azul',40,50)
    pincel.fillText('Clique aqui para apagar o círculo azul',40,90)

    // ponto de acesso

    pincel.fillStyle = 'red'
    pincel.beginPath()
    pincel.ellipse(10,40,10,10,2 * Math.PI, 0, 2 * Math.PI)
    pincel.ellipse(10,80,10,10,2 * Math.PI, 0, 2 * Math.PI)
    pincel.fill()

    function desenharElipse(){
        pincel.fillStyle = 'blue'
        pincel.beginPath()
        pincel.ellipse(200,200,50,40,2 * Math.PI, 0, 2 * Math.PI)
        pincel.fill() 
    }

    function apagarAElipse(){
        pincel.clearRect(150,160,100,80)
    }

    function lerCursor(evento){
        var x = evento.PageX - tela.offsetLeft
        var y = evento.PageY - tela.offsetTop

        if (x > 0 && x < 20 ){
            
        }
    }

</script>

```
