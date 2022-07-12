<template>

  <section class="src-components-final">
        
     <div class= "container">
    
    <span>Color: <input type="text" v-model="color"></span>
    <span>Fondo: <input type="text" v-model="fondo"></span>
    <span>Size: <input type="text" v-model="tamanio"></span>
    <br>
    <br>
    <span>Texto: </span><input :style="{color: color,background: fondo, fontSize: tamanio}" type="text" v-model.trim ="texto">
    <br>
    <br>
    <span style = "text-align:center;">Cantidad de palabras: {{ cantidadDePalabras }} </span>
          
    </div>
    <br>
    <br>

    <table>
      <thead>
        <tr>  
          <th>Pregunta </th><br>
          <th> Respuesta </th>
        </tr>
      </thead>
      <tbody>
        <tr>  
          <td> 1 </td><br>
          <td> B </td>
        </tr>
         <tr>  
          <td> 2 </td><br>
          <td> C </td>
        </tr>
        <tr>  
          <td> 3 </td><br>
          <td> B </td>
        </tr>
        <tr>  
          <td> 4 </td><br>
          <td> D </td>
        </tr>
        <tr>  
          <td> 5 </td><br>
          <td> D </td>
        </tr>
      </tbody>

    </table>
  </section>

</template>

<script>

  export default  {
    name: 'src-components-final',
    props: [],
    mounted () {

    },
    data () {
      return {
        color: "",
        fondo: "",
        tamanio: "",
        texto: "",
      }
    },
    methods: {

    },
    computed: {
      cantidadDePalabras() {
      let cantidadPalabras = 0
        if( this.texto !== "") {
          const palabras = this.texto.split(" ");
          cantidadPalabras = palabras.length;
        }
      return cantidadPalabras;
      }
    }
    }



</script>

<style scoped lang="css">
  .container{
    text-align: left;
    margin-left: 15px;
    margin-top: 20px;
  }
  span {
    margin-right: 10px;
  }
</style>
