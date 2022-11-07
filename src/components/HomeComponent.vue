<script>

export default {

  data() {
    return {
      carteras: [{
        color: '#bf360c',
        precio: 12,
        nombre: 'Juego Marrón',
        imagen: './assets/carteras/pc1.jpg'
      },
      {
        color: '#9c0000',
        precio: 12,
        nombre: 'Juego Rojo',
        imagen: './assets/carteras/pc2.jpg',
      },
      {
        color: '#000000',
        precio: 12,
        nombre: 'Juego Negro',
        imagen: './assets/carteras/pc3.jpg'
      }],
      bikinis: [{
        color: '#ffffff',
        precio: 5,
        nombre: 'Bikini Blanco',
        talla: 'U: Única',
        imagen: './assets/bikini/pb1.jpg',
      },
      {
        color: '#d50000',
        precio: 5,
        nombre: 'Bikini Rojo',
        talla: 'U: Única',
        imagen: './assets/bikini/pb2.jpg'
      },
      {
        color: '#f8bbd0',
        precio: 5,
        nombre: 'Bikini Rosa',
        talla: 'U: Única',
        imagen: './assets/bikini/pb3.jpg'
      }],
      bandoleros: [/*{
        color: '#bf360c',
        precio: 5,
        nombre: 'Estampados',
        imagen: './assets/bandoleros/prospect1.jpg'
      },*/
      {
        color: '#9c0000',
        precio: 5,
        nombre: 'Anillos',
        imagen: './assets/bandoleros/prospect2.jpg'
      },
      {
        color: '#000000',
        precio: 5,
        nombre: 'Casuales',
        imagen: './assets/bandoleros/prospect3.jpg'
      },
      {
        color: '#bf360c',
        precio: 5,
        nombre: 'Estampado Blanco',
        imagen: './assets/bandoleros/prospect4.jpg'
      },
      {
        color: '#9c0000',
        precio: 5,
        nombre: 'Casual Negro',
        imagen: './assets/bandoleros/prospect5.jpg'
      },
      {
        color: '#000000',
        precio: 5,
        nombre: 'Vestido',
        imagen: './assets/bandoleros/prospect6.jpg'
      }],
    }
  },
  methods: {
    comprar(producto) {
      window.open(`https://api.whatsapp.com/send/?phone=584148654284&text=Hola! estoy interesado por el producto: ${ producto.nombre }`);      
    }
  }

}

</script>

<template>
  <div class="container">
    <div class="carteras" id="carteras">
      <h1>CARTERAS</h1>
      <div v-for="cartera in carteras">
        <div class="card">
          <div class="card-header">
            <p>{{ cartera.nombre }}</p>
          </div>
          <div class="card-body">
            <div class="img" :style="{ backgroundImage: `url(${ cartera.imagen })` }"></div>
          </div>
          <div class="card-footer">
            <div class="field-card-bottom">
              <button @click="comprar(cartera)">COMPRAR</button>
              <b><p class="price-paragraph">{{ cartera.precio }}$</p></b>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bikini" id="bikini">
      <h1>ROPA ÍNTIMA</h1>
      <div v-for="bikini in bikinis">
        <div class="card">
          <div class="card-header">
            <p>{{ bikini.nombre }}</p>
          </div>
          <div class="card-body">
            <div class="img" :style="{ backgroundImage: `url(${ bikini.imagen })` }"></div>
          </div>
          <div class="card-footer">
            <div class="field-card-bottom">
              <button @click="comprar(bikini)">COMPRAR</button>              
              <b><p class="price-paragraph">{{ bikini.precio }}$</p></b>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bandoleros" id="bandoleros">
      <h1>BANDOLEROS</h1>
      <div v-for="bandolero in bandoleros">
        <div class="card">
          <div class="card-header">
            <p>{{ bandolero.nombre }}</p>
          </div>
          <div class="card-body">
            <div class="img" :style="{ backgroundImage: `url(${ bandolero.imagen })`}"></div>
          </div>
          <div class="card-footer">
            <div class="field-card-bottom">
              <button @click="comprar(bandolero)">COMPRAR</button>              
              <b><p class="price-paragraph">{{ bandolero.precio }}$</p></b>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>
