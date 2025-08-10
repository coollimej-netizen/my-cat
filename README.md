<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>애용 홈페이지</title>
<style>
  body { font-family: Arial, sans-serif; }
  .menu-btn {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    font-size: 16px;
  }
  .side-panel {
    position: fixed;
    top: 0;
    right: -300px;
    width: 300px;
    height: 100%;
    background-color: #f1f1f1;
    box-shadow: -2px 0 5px rgba(0,0,0,0.3);
    transition: right 0.3s ease;
    padding: 20px;
  }
  .side-panel.open {
    right: 0;
  }
  .close-btn {
    background-color: red;
    color: white;
    border: none;
    padding: 5px 10px;
    cursor: pointer;
    font-size: 14px;
  }
</style>
</head>
<body>

<h1>애용 홈페이지</h1>
<button class="menu-btn" onclick="openPanel()">메뉴</button>

<div class="side-panel" id="sidePanel">
  <button class="close-btn" onclick="closePanel()">X</button>
  <h2>같이 하는것.</h2>
  <ul>
    <li>같이 자기</li>
    <li>tv보기</li>
    <li>같이 놀기</li>
  </ul>
</div>

<script>
  function openPanel() {
    document.getElementById('sidePanel').classList.add('open');
  }
  function closePanel() {
    document.getElementById('sidePanel').classList.remove('open');
  }
</script>
<img src="images/photo.png" alt="naju.jpg." style="width:300px;">


</body>
</html>
