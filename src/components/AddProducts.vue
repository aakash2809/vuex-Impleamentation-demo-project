<template>
  <div class="add-product">
    <form @submit.prevent="onSubmit">
      <input type="text" v-model="item" placeholder="Add Product..." />
      <input type="text" v-model="price" placeholder="Add Price..." />
      <input type="submit" value="Submit" />
    </form>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "AddProduct",
  data() {
    return {
      item: "",
      price: "",
    };
  },
  methods: {
    ...mapActions(["addProduct"]),
    onSubmit() {
      this.addProduct({
        item: this.item,
        price: this.price,
      });
    },
  },
};
</script>

<style scoped>
.add-product {
  background: #fff;
  padding: 15px;
  border-radius: 5px;
  margin-bottom: 20px;
}
form {
  display: flex;
  justify-content: space-between;
}
input[type="text"] {
  width: 270px;
  padding: 10px;
  border: 1px solid #2c3e50;
  outline: 0;
}
input[type="submit"] {
  width: 120px;
  background: #2c3e50;
  color: #fff;
  border: 1px #2c3e50 solid;
  cursor: pointer;
}
</style>