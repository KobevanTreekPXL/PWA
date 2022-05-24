<template>
  <div class="Items">
    <h3>Deze pagina laat het aantal calorieën zien per fruitstuk en zou offline ook moeten werken!</h3>
    <div class="tableFixHead">
        <table class="styled-table" aria-describedby="reviewers">
          <thead>
            <tr>
              <th>Naam</th>
              <th id="jumpLeft">aantal calorieën</th>
              <th id="jumpLeft">Hoeveelheid</th>

            </tr>
          </thead>
          <tbody>
            <tr v-for="row in data" :key="row.Name">
              <td>
                {{ row?.Name?.toUpperCase() }}
              </td>
              <td>{{ row.kcal }}</td>
                <td>{{ row.hoeveelheid }}</td>

            </tr>
          </tbody>
        </table>
      </div>
  </div>
</template>


<script>

import { defineComponent } from "vue";
export default defineComponent({
  data() {
    return {
      data: [
        { Name: "Appel", kcal: 76, hoeveelheid: "1 appel"},
        { Name: "Banaan", kcal: 152, hoeveelheid: "1 banaan"},
        { Name: "Peer", kcal: 124, hoeveelheid: "1 peer"},
        { Name: "Mango", kcal: 185, hoeveelheid: "1 mango"},
        { Name: "Kiwi", kcal: 51 , hoeveelheid: "1 kiwi"},
        { Name: "Frambozen ", kcal: 37 , hoeveelheid: "100 gram"},
        { Name: "Pruim", kcal: 44, hoeveelheid: "1 pruim"},
        { Name: "Bosbessen", kcal: 75, hoeveelheid: "100 gram"},
        { Name: "braambessen", kcal: 48 , hoeveelheid: "100 gram"},
      ]
    }
  },
})
</script>

<style scoped>
.styled-table {
margin: auto;
}
.styled-table thead tr {
  background-color: greenyellow;
  text-align: left;
}
.styled-table th,
.styled-table td {
  padding: 2vh 10vw 2vh 5vw;
}

.styled-table tr {
  padding-left: 2vw;
  
}
.styled-table th:last-child,
.styled-table td:last-child {
  padding: 2vh 10vw 2vh 2vw;
}

.styled-table tbody tr {
  border-bottom: 1px solid #dddddd;
}

.styled-table tbody tr:nth-of-type(even) {
  background-color: rgba(122, 122, 122, 0.185);
}

.styled-table tbody tr:last-of-type {
  border-bottom: thick solid greenyellow;
}

.styled-table tbody tr:hover {
  color: #009879;
  transition: 0.3s;
  transition-timing-function: linear;
}
</style>