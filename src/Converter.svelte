<script>
import VoltarMenu from './VoltarMenu.svelte'

let temperatura = ["",""]
let c = 0
let f = 0
//C = (F-32)/1,8

     function C() {
        c = (temperatura[0] - 32) / 1.8
        alert (c)
}

  // F = C * 1,8+32
  function F() {
        f = (temperatura[1] * 1.8) + 32
        alert (f)
  }


</script>
    
    <body>
        <div id="container">
            <h1>Converter Temperatura</h1>
            <label>
            <h3>Converter Fahrenheit para Celsius: </h3>
            <input type="number" id="fahrenheit" placeholder="Fahrenheit" bind:value={temperatura[0]} />
            <button on:click={C}> Converter</button>
            </label><br>
    
            <label>
            <h3>Converter Celsius para Fahrenheit: </h3>
            <input type="text" id="celsius" placeholder="Celsius" bind:value={temperatura[1]} />
            <button on:click={F}> Converter</button>
            </label>
        
            <button id="clear">Redefinir</button>
        </div>
    </body>
    <VoltarMenu/>
    
    <style>
        body {
            text-align: center;
            padding: 1em;
            color: #ff3e00;
            margin: 0 auto;
        }
    
        h1 {
            color: #ff3e00;
            text-transform: uppercase;
            font-weight: 100;
        }
    </style>