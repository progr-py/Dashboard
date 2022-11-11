<template>
  <h2>Recent Orders</h2>
  <table>
    <thead>
      <tr>
        <th>Product Name</th>
        <th>Product Number</th>
        <th>Payment</th>
        <th>Status</th>
        <th>Details</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for=" data in tableData">
        <td class="text-muted">{{ data.productName }}</td>
        <td class="text-muted">{{ data.ProductNumber }}</td>
        <td class="text-muted">{{ data.ProductNumber }}</td>
        <td class="warning">{{ data.shipping }}</td>
        <td class="primary">Details</td>
      </tr>

    </tbody>
  </table>
  <a href="#">Show All</a>

</template>
<script>
export default {
  data() {
    return {
      tableData: [{
        "productName": "enim sit",
        "ProductNumber": 81,
        "paymentStatus": "quam",
        "shipping": "Candy"
      }, {
        "productName": "sagittis sapien",
        "ProductNumber": 40,
        "paymentStatus": "viverra",
        "shipping": "Denice"
      }, {
        "productName": "turpis sed",
        "ProductNumber": 87,
        "paymentStatus": "non",
        "shipping": "Forest"
      }, {
        "productName": "in leo",
        "ProductNumber": 89,
        "paymentStatus": "et",
        "shipping": "Tatum"
      }, {
        "productName": "maecenas tristique",
        "ProductNumber": 82,
        "paymentStatus": "donec",
        "shipping": "Charin"
      }]


    }
  },
}
</script>
