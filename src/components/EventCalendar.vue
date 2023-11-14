<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Calendario de Eventos: Implementa un componente EventCalendar que tome una lista de eventos como prop, donde cada
      evento es un objeto con propiedades como título, fecha y descripción, y los muestre en una vista de calendario.
    </p>
    <h3>Lista</h3>
    <table>
      <thead>
        <tr>
          <th scope="col">Titulo</th>
          <th scope="col">Fecha</th>
          <th scope="col">Descripcion</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="evento in eventos" v-bind:key="evento">
          <td>
            <span>
              {{ evento.titulo }}
            </span>
          </td>
          <td>
            <span>
              {{ evento.fecha }}
            </span>
          </td>
          <td>
            <span>
              {{ evento.descripcion }}
            </span>
          </td>
        </tr>
      </tbody>
    </table>

  </div>
</template>

<script>
export default {
  name: 'EventCalendar',
  props: {
    msg: String,
    eventos: {
      titulo: String,
      fecha: Date,
      descripcion: String,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
table {
  margin: 0 auto;
  width: 50%;
  border-collapse: collapse;
  font-size: 1rem;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
}

table thead tr {
  background-color: var(--color-container);
  color: var(--color-background);
  text-align: center;
}

table thead tr th {
  border: none;
  font-size: 1.125rem;
  padding: 2rem 1.25rem;
  white-space: nowrap;
}

table tbody tr {
  border-bottom: none;
}

table tbody tr:nth-of-type(even) {
  background-color: var(--color-background);
}

table tbody tr:last-of-type {
  border-bottom: 4px solid var(--color-container);
}

table tbody tr td {
  padding: 1rem 1.25rem;
  border: none;
  white-space: wrap;
  color:var(--color-font);
}

table tbody tr td img {
  max-width: 100px;
  height: auto;
}


h3 {
  margin: 40px 0;
  margin-bottom: 40px;
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
</style>
