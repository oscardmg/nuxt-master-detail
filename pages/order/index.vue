<template >
  <div>
    <form action="" autocomplete="off">
      <div class="row">
        <div class="col-md-6">
          <div class="form-group">
            <label for="OrderNo" >Order No.</label >
            <div class="input-group">
              <div class="input-group-prepend">
                <div class="input-group-text">#</div>
                <input name="OrderNo" id="OrderNo" v-model="formData.orderNo" type="text" class="form-control" >
              </div>
            </div>
          </div>
          <div class="form-group ">
            <label for="Customer" >Customer</label >
            <input name="Customer" id="Customer" v-model="formData.customer" type="text" class="form-control" >
          </div>
        </div>
        <div class="col-md-6">
          <div class="form-group">
            <label for="PMethod" >Payment Method</label >
            <select name="PMethod" id="PMethod" v-model="formData.paymentMethod" class="form-control">
              <option value="" >-Select-</option >
              <option value="Cash" >Cash</option >
              <option value="Card" >Card</option >
            </select >
          </div>
          <div class="form-group">
            <label for="Total" >Grand Total</label >
            <div class="input-group">
              <div class="input-group-prepend">
                <div class="input-group-text">#</div>
                <input name="Total" id="Total" v-model="formData.total" type="text" class="form-control" >
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- Order items table -->
      <table class="table table-borderless">
        <thead class="thead-light">
        <th>Food</th>
        <th>Price</th>
        <th>Quantity</th>
        <th>Total</th>
        <th>
          <a class="btn btn-sm btn-success text-white" @click="AddOrEditOrderItem(null, formData.orderId)"><i class="fa fa-plus"></i> Add Item</a>
        </th>
        </thead>
        <tbody>
        <tr v-if="orderItems.length === 0">
          <td class="font-italic text-center" colspan="5">
            No food item selected for this order.
          </td>
        </tr>

        <tr v-for="(item, index) in orderItems">
          <td>{{item.ItemName}}</td>
          <td>{{item.Price}}</td>
          <td>{{item.Quantity}}</td>
          <td>{{item.Total}}</td>
          <td>
            <a class="btn btn-sm btn-info text-white" @click="AddOrEditOrderItem(index, formData.orderId)"><i class="fa fa-pencil"></i></a>
            <a class="btn btn-sm btn-danger text-white ml-1" @click="onDeleteOrderItem(item.orderItemId,index)"><i class="fa fa-trash"></i></a>
          </td>
        </tr>
        </tbody>
      </table>

      <div class="form-group">
        <button type="submit" class="btn btn-dark" >
          <i class="fa fa-database"></i>
          Submit
        </button >
      </div>
    </form >
  </div>
</template >

<script >
  export default {
    name: 'index',
    data() {
      return {
        formData: {
          orderId: 0,
          orderNo: 0,
          customer: '',
          paymentMethod: '',
          total: 0
        },
        orderItems: []
      }
    },
    methods: {
      AddOrEditOrderItem(index){

      },
      onDeleteOrderItem() {

      }
    }
  };
</script >

<style scoped >

</style >
