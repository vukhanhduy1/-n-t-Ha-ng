<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Đặt hàng - Công Ty Cổ Phần Xuất Nhập Hoá Chất Miền Nam</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }
  .container {
    width: 80%;
    margin: 20px auto;
  }
  form {
    border: 1px solid #ccc;
    padding: 20px;
    border-radius: 5px;
  }
  input[type=text], input[type=number] {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
  }
  input[type=submit] {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  input[type=submit]:hover {
    background-color: #45a049;
  }
</style>
</head>
<body>

<div class="container">
  <h2>Đặt hàng - Công Ty Cổ Phần Xuất Nhập Hoá Chất Miền Nam</h2>
  <form id="orderForm">
    <label for="customerName">Tên khách hàng:</label>
    <input type="text" id="customerName" name="customerName" required><br>

    <label for="product">Sản phẩm:</label>
    <input type="text" id="product" name="product" required><br>

    <label for="quantity">Số lượng:</label>
    <input type="number" id="quantity" name="quantity" required><br>

    <label for="price">Giá tiền (VNĐ):</label>
    <input type="number" id="price" name="price" required><br>

    <label for="pickupLocation">Nơi nhận hàng:</label>
    <input type="text" id="pickupLocation" name="pickupLocation" required><br>

    <input type="submit" value="Đặt hàng">
  </form>
</div>

<script>
document.getElementById("orderForm").addEventListener("submit", function(event) {
  event.preventDefault();
  const formData = new FormData(event.target);
  const customerName = formData.get("customerName");
  const product = formData.get("product");
  const quantity = formData.get("quantity");
  const price = formData.get("price");
  const pickupLocation = formData.get("pickupLocation");

  // Gửi dữ liệu đặt hàng đến server (hoặc xử lý dữ liệu theo nhu cầu của bạn)
  console.log("Tên khách hàng:", customerName);
  console.log("Sản phẩm:", product);
  console.log("Số lượng:", quantity);
  console.log("Giá tiền (VNĐ):", price);
  console.log("Nơi nhận hàng:", pickupLocation);

  // Sau khi xử lý, bạn có thể chuyển hướng hoặc hiển thị thông báo thành công tùy theo yêu cầu
});
</script>

</body>
</html>
