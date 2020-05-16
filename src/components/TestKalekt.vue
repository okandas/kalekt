<template>
  <div class="hello">
    <h1>{{msg}}</h1>
    <div class="container-wrapper">
      <table class="container pure-table  pure-table-bordered">
      <thead>        
        <draggable v-model="headers" tag="tr">
            <th v-for="header in headers" :key="header" scope="col">
              {{ header }}
              <font-awesome-icon icon="arrows-alt" />
            </th>
        </draggable>
      </thead>
      <tbody>
        
        <tr v-for="(product, key) in products"  :key="key" :class="{'pure-table-odd': (key % 2 == 0)}">
          <td v-for="header in headers" :key="header">{{ product[header] }}</td>
        </tr>
     
          
      </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import data from '../data'
import draggable from 'vuedraggable'

export default {
  name: 'TestKalekt',
  components: {
      draggable,
  },
  data () {
    return {
      msg: 'Welcome to the Answer',
      products: data,
      headers: ['_id','type', 'price', 'taxable', 'taxCode', 'title', 'inventoryQuantity', 'inventoryManagement']
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.container-wrapper {
  overflow-x: scroll;
  margin: 0 auto;
  width: 500px;
}


.pure-table th {
 min-width: 200px;
 text-align: center;
 cursor: move;
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


</style>
