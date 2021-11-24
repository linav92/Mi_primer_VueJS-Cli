<template>
  <div id="app">
     <h1>Tabla de Usuarios</h1>
    <table class="table table-striped table-hover table-bordered">
      <thead class="table-dark">
        <tr>
          <th>#</th>
          <th>Nombre</th>
          <th>Apellido</th>
          <th>RUN</th>
          <th>Nacimiento</th>
          <th>Edad</th>
        </tr>
      </thead>
       <tbody>
        <tr v-for="(item,index) in lista" :key="index">
          <td>{{index+1}}</td>
          <td>{{item.nombre}}</td>
          <td>{{item.apellido}}</td>
          <td>{{item.run}}</td>
          <td>{{item.nacimiento}}</td>
          <td>{{item.edad}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      lista: [
        {
          nombre: 'Jose',
          apellido: 'Perez',
          run: '123456-2',
          nacimiento: '12/04/1967',
          edad: '54'
        },
        {
          nombre: 'Maria',
          apellido: 'Rodríguez',
          run: '654321-1',
          nacimiento: '30/11/1990',
          edad: '31'
        },
        {
          nombre: 'Manuel',
          apellido: 'Patiño',
          run: '987654-5',
          nacimiento: '02/12/1959',
          edad: '62'
        }
      ],
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
  padding: 3rem;
}
</style>
