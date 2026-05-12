# bug-free-engine
sait alya cdek 
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Оплата заказа</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family: Arial, sans-serif;
    }

    body{
      background:#f4f4f4;
      display:flex;
      justify-content:center;
      align-items:center;
      min-height:100vh;
      padding:20px;
    }

    .container{
      width:100%;
      max-width:850px;
      background:#fff;
      border-radius:20px;
      padding:35px;
      box-shadow:0 5px 20px rgba(0,0,0,0.08);
    }

    h1{
      font-size:42px;
      margin-bottom:35px;
      color:#111;
    }

    .step{
      display:flex;
      align-items:flex-start;
      gap:20px;
      margin-bottom:28px;
    }

    .circle{
      min-width:45px;
      height:45px;
      border-radius:50%;
      background:#2db84d;
      color:#fff;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:20px;
      font-weight:bold;
    }

    .text{
      font-size:28px;
      color:#333;
      line-height:1.4;
    }

    .bank{
      margin-top:15px;
      font-size:24px;
      line-height:1.5;
    }

    .sum{
      font-size:36px;
      font-weight:bold;
      color:#111;
    }

    /* Загрузка файла */
    .upload-box{
      margin-top:40px;
      border:2px dashed #cfcfcf;
      border-radius:16px;
      padding:35px;
      text-align:center;
      transition:0.3s;
      background:#fafafa;
    }

    .upload-box:hover{
      border-color:#2db84d;
      background:#f6fff8;
    }

    .upload-label{
      display:inline-block;
      padding:15px 30px;
      background:#2db84d;
      color:#fff;
      border-radius:12px;
      cursor:pointer;
      font-size:20px;
      font-weight:bold;
      transition:0.3s;
    }

    .upload-label:hover{
      background:#25963f;
    }

    input[type="file"]{
      display:none;
    }

    .file-name{
      margin-top:20px;
      font-size:18px;
      color:#555;
    }

    /* Вторая страница */
    .success-page{
      display:none;
      text-align:center;
      padding:40px 20px;
    }

    .success-icon{
      width:90px;
      height:90px;
      border-radius:50%;
      background:#2db84d;
      color:#fff;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:48px;
      margin:0 auto 25px;
    }

    .success-title{
      font-size:38px;
      font-weight:bold;
      margin-bottom:15px;
      color:#111;
    }

    .success-text{
      font-size:22px;
      color:#555;
      margin-bottom:15px;
      line-height:1.5;
    }

    .thanks-text{
      margin-top:10px;
      margin-bottom:35px;
      font-size:24px;
      font-weight:600;
      color:#2db84d;
      text-align:center;
    }

    .track-box{
      background:#f7f7f7;
      border-radius:18px;
      padding:30px;
      text-align:left;
      max-width:700px;
      margin:0 auto;
    }

    .route{
      display:flex;
      justify-content:space-between;
      align-items:center;
      margin-bottom:35px;
      font-size:28px;
      font-weight:bold;
    }

    .line{
      height:4px;
      background:#2db84d;
      margin:15px 0 40px;
      border-radius:10px;
      position:relative;
    }

    .line::after{
      content:'';
      position:absolute;
      right:0;
      top:50%;
      transform:translateY(-50%);
      width:18px;
      height:18px;
      border-radius:50%;
      background:#2db84d;
    }

    .status{
      display:flex;
      gap:18px;
      margin-bottom:28px;
      align-items:flex-start;
    }

    .status-icon{
      min-width:42px;
      height:42px;
      border-radius:50%;
      display:flex;
      align-items:center;
      justify-content:center;
      color:#fff;
      font-weight:bold;
    }

    .green{
      background:#2db84d;
    }

    .yellow{
      background:#f2c200;
    }

    .gray{
      background:#cfcfcf;
    }

    .status-text{
      font-size:22px;
      color:#222;
    }

    .status-date{
      font-size:16px;
      color:#777;
      margin-top:5px;
    }

    @media(max-width:768px){

      h1{
        font-size:32px;
      }

      .text{
        font-size:22px;
      }

      .bank{
        font-size:20px;
      }

      .sum{
        font-size:28px;
      }

      .success-title{
        font-size:30px;
      }

      .success-text{
        font-size:18px;
      }

      .thanks-text{
        font-size:20px;
      }

      .route{
        font-size:22px;
      }

      .status-text{
        font-size:18px;
      }
    }
  </style>
</head>
<body>

  <!-- ПЕРВАЯ СТРАНИЦА -->
  <div class="container" id="paymentPage">

    <h1>Оплата заказа</h1>

    <div class="step">
      <div class="circle">1</div>

      <div class="text">
        Откройте мобильное приложение вашего банка
      </div>
    </div>

    <div class="step">
      <div class="circle">2</div>

      <div class="text">
        Найдите раздел «Переводы» или «Платежи по СБП»
      </div>
    </div>

    <div class="step">
      <div class="circle">3</div>

      <div class="text">
        Введите реквизиты получателя:

        <div class="bank">
          <b>Т-Банк</b><br>
          +7 999 123-45-67<br>
          Мария К.
        </div>
      </div>
    </div>

    <div class="step">
      <div class="circle">4</div>

      <div class="text">
        Укажите сумму к оплате —
        <span class="sum">52000₽</span>
      </div>
    </div>

    <div class="step">
      <div class="circle">5</div>

      <div class="text">
        В комментарии укажите номер заказа
      </div>
    </div>

    <div class="step">
      <div class="circle">6</div>

      <div class="text">
        Подтвердите перевод и загрузите чек
      </div>
    </div>

    <!-- Загрузка чека -->
    <div class="upload-box">

      <label for="receipt" class="upload-label">
        Загрузить чек
      </label>

      <input type="file" id="receipt" accept="image/*,.pdf">

      <div class="file-name" id="fileName">
        Файл не выбран
      </div>

    </div>

  </div>


  <!-- ВТОРАЯ СТРАНИЦА -->
  <div class="container success-page" id="successPage">

    <div class="success-icon">✓</div>

    <div class="success-title">
      Чек успешно загружен
    </div>

    <div class="success-text">
      Ваш платеж отправлен на проверку.<br>
      Статус заказа обновляется.
    </div>

    <div class="thanks-text">
      Благодарим, что доверяете нам ❤️
    </div>

    <div class="track-box">

      <div class="route">
        <span>Москва</span>
        <span>Волгоград</span>
      </div>

      <div class="line"></div>

      <div class="status">

        <div class="status-icon green">✓</div>

        <div>
          <div class="status-text">
            Оплачено
          </div>

          <div class="status-date">
            18.01.2026
          </div>
        </div>

      </div>

      <div class="status">

        <div class="status-icon yellow">➜</div>

        <div>
          <div class="status-text">
            В пути
          </div>

          <div class="status-date">
            Посылка передана в доставку
          </div>
        </div>

      </div>

      <div class="status">

        <div class="status-icon gray">•</div>

        <div>
          <div class="status-text">
            Готов к выдаче
          </div>

          <div class="status-date">
            Ожидается
          </div>
        </div>

      </div>

      <div class="status">

        <div class="status-icon gray">•</div>

        <div>
          <div class="status-text">
            Вручен
          </div>

          <div class="status-date">
            Ожидается
          </div>
        </div>

      </div>

    </div>

  </div>

  <script>

    const input = document.getElementById('receipt');

    const fileName =
      document.getElementById('fileName');

    const paymentPage =
      document.getElementById('paymentPage');

    const successPage =
      document.getElementById('successPage');

    input.addEventListener('change', function() {

      if(this.files.length > 0){

        fileName.textContent =
          "Прикреплен файл: " + this.files[0].name;

        // Задержка перед переходом
        setTimeout(() => {

          // Скрываем первую страницу
          paymentPage.style.display = 'none';

          // Показываем вторую страницу
          successPage.style.display = 'block';

          // Плавный скролл вверх
          window.scrollTo({
            top: 0,
            behavior: 'smooth'
          });

        }, 1200);

      } else {

        fileName.textContent =
          "Файл не выбран";

      }

    });

  </script>

</body>
</html>
