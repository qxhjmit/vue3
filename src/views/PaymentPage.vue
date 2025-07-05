<template>
  <div class="payment-container">
    <h1>支付页面</h1>
    <form @submit.prevent="handleSubmit">
      <div class="form-group">
        <label for="card-number">卡号:</label>
        <input type="text" id="card-number" v-model="cardNumber" required />
      </div>
      <div class="form-group">
        <label for="expiry-date">过期日期:</label>
        <input type="text" id="expiry-date" v-model="expiryDate" required />
      </div>
      <div class="form-group">
        <label for="cvv">CVV:</label>
        <input type="text" id="cvv" v-model="cvv" required />
      </div>
      <button type="submit">提交支付</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'PaymentPage',
  data() {
    return {
      cardNumber: '',
      expiryDate: '',
      cvv: ''
    };
  },
  methods: {
    handleSubmit() {
      // 处理支付逻辑
      console.log('Card Number:', this.cardNumber);
      console.log('Expiry Date:', this.expiryDate);
      console.log('CVV:', this.cvv);

      // 在这里可以添加调用支付网关的代码
      alert('支付成功！');
    }
  }
};
</script>

<style scoped>
.payment-container {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input[type="text"] {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

button {
  padding: 10px 15px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>