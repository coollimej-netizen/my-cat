<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <title>애용 홈페이지</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
    }

    /* 버튼 */
    .open-btn {
      position: fixed;
      top: 20px;
      left: 20px;
      background: #4CAF50;
      color: white;
      border: none;
      padding: 10px 15px;
      cursor: pointer;
      border-radius: 5px;
    }

    /* 사이드 패널 */
    .side-panel {
      position: fixed;
      top: 0;
      right: -300px; /* 처음엔 화면 밖 */
      width: 300px;
      height: 100%;
      background: #f9f9f9;
      box-shadow: -2px 0 5px rgba(0,0,0,0.3);
      padding: 20px;
      box-sizing: border-box;
      transition: right 0.3s ease;
    }

    /* 패널 열렸을 때 */
    .side-panel.open {
      right: 0;
    }

    /* 닫기 버튼 */
    .close-btn {
      position: absolute;
      top: 10px;
      right: 10px;
      background: red;
      color: white;
      border: none;
      border-radius: 50%;
      width: 25px;
      height: 25px;
      cursor: pointer;
      font-weight: bold;
    }

    /* 본문 내용 */
    .content {
      padding: 50px;
      text-align: center;
    }
  </style>
</head>
<body>

  <button class="open-btn" onclick="openPanel()">열기</button>

  <div class="content">
    <h1>애용이의 홈페이지</h1>
    <img src="naju.jpg" alt="나주 사진" width="400">
  </div>

  <div class="side-panel" id="panel">
    <button class="close-btn" onclick="closePanel()">X</button>
    <h2>애용이랑 할 수 있는 것</h2>
    <p>같이 자기, TV 보기, 같이 있기</p>
  </div>

  <script>
    function openPanel() {
      document.getElementById("panel").classList.add("open");
    }
    function closePanel() {
      document.getElementById("panel").classList.remove("open");
    }
  </script>

</body>
</html>
