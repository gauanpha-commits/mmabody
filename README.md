# mmabody
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MMA Strategy by Body Type</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #0f0f0f;
      color: #f1f1f1;
      max-width: 480px;
      margin: auto;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #f5c542;
    }
    p {
      text-align: center;
      font-size: 14px;
      color: #ccc;
    }
    label {
      margin-top: 15px;
      display: block;
    }
    input, select, button {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border-radius: 6px;
      border: none;
      font-size: 16px;
    }
    button {
      background: #f5c542;
      color: #000;
      font-weight: bold;
      margin-top: 20px;
      cursor: pointer;
    }
    .result {
      margin-top: 25px;
      padding: 15px;
      background: #1c1c1c;
      border-radius: 8px;
    }
    .result h3 {
      color: #f5c542;
    }
    .cta {
      margin-top: 20px;
      text-align: center;
    }
    .cta a {
      color: #f5c542;
      text-decoration: none;
      font-weight: bold;
    }
    .disclaimer {
      font-size: 12px;
      color: #888;
      margin-top: 20px;
      text-align: center;
    }
  </style>
</head>
<body>

<h1>MMA Body Strategy</h1>
<p>Nhập thể trạng để xem phong cách MMA phù hợp<br>
Enter your body stats to see your MMA style</p>

<label>Chiều cao / Height (cm)</label>
<input type="number" id="height">

<label>Cân nặng / Weight (kg)</label>
<input type="number" id="weight">

<label>Sải tay / Reach</label>
<select id="reach">
  <option value="short">Ngắn / Short</option>
  <option value="average">Trung bình / Average</option>
  <option value="long">Dài / Long</option>
</select>

<button onclick="analyze()">Phân tích / Analyze</button>

<div class="result" id="result"></div>

<div class="cta">
  👉 <a href="#" target="_blank">Follow TikTok để xem phân tích võ thuật</a>
</div>

<div class="disclaimer">
  Thông tin chỉ mang tính tham khảo – không thay thế huấn luyện chuyên nghiệp.<br>
  Educational purpose only. Not a training guide.
</div>

<script>
function analyze() {
  const height = document.getElementById("height").value;
  const weight = document.getElementById("weight").value;
  const reach = document.getElementById("reach").value;

  let result = "";

  if (height >= 175 && reach === "long" && weight <= 85) {
    result = `
    <h3>Distance Striker</h3>
    <ul>
      <li>Kiểm soát khoảng cách – Control range</li>
      <li>Di chuyển nhiều – Stay mobile</li>
      <li>Đánh chính xác, tiết kiệm sức – Focus on timing</li>
      <li>Tránh đối đầu sức mạnh – Avoid close pressure</li>
    </ul>`;
  } 
  else if (height < 170 && weight >= 80) {
    result = `
    <h3>Pressure & Control Fighter</h3>
    <ul>
      <li>Áp sát liên tục – Close the distance</li>
      <li>Kiểm soát thể lực – Physical control</li>
      <li>Đánh ngắn, chắc – Short and steady exchanges</li>
      <li>Làm đối thủ mệt dần – Wear opponent down</li>
    </ul>`;
  } 
  else {
    result = `
    <h3>Balanced Fighter</h3>
    <ul>
      <li>Linh hoạt theo tình huống – Adaptable style</li>
      <li>Kết hợp di chuyển và kiểm soát</li>
      <li>Tập trung cardio và sự ổn định</li>
      <li>Điều chỉnh chiến thuật theo đối thủ</li>
    </ul>`;
  }

  document.getElementById("result").innerHTML = result;
}
</script>

</body>
</html
