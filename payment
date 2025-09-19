<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Payment Gateway - Dana, Gopay, OVO, QRIS</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            animation: fadeIn 0.8s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        header {
            background: linear-gradient(to right, #2575fc, #6a11cb);
            color: white;
            text-align: center;
            padding: 25px 20px;
        }

        header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        header p {
            opacity: 0.9;
        }

        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 30px;
        }

        .payment-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .payment-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .card-header {
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 1.5rem;
        }

        .dana .card-header {
            background: linear-gradient(to right, #0095ff, #00a2ff);
        }

        .gopay .card-header {
            background: linear-gradient(to right, #00a64f, #00c853);
        }

        .ovo .card-header {
            background: linear-gradient(to right, #4c2c92, #673ab7);
        }

        .qris .card-header {
            background: linear-gradient(to right, #ff6600, #ff9900);
        }

        .card-body {
            padding: 20px;
            text-align: center;
        }

        .card-body i {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .dana .card-body i {
            color: #0095ff;
        }

        .gopay .card-body i {
            color: #00a64f;
        }

        .ovo .card-body i {
            color: #4c2c92;
        }

        .qris .card-body i {
            color: #ff6600;
        }

        .card-body p {
            font-size: 1.1rem;
            margin: 10px 0;
            color: #333;
            word-break: break-all;
        }

        .copy-btn {
            background: linear-gradient(to right, #2575fc, #6a11cb);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 50px;
            cursor: pointer;
            margin-top: 10px;
            transition: all 0.3s ease;
        }

        .copy-btn:hover {
            background: linear-gradient(to right, #6a11cb, #2575fc);
            transform: scale(1.05);
        }

        .qris-img {
            width: 100%;
            max-width: 200px;
            height: auto;
            border-radius: 10px;
            margin: 15px auto;
            display: block;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .qris-img:hover {
            transform: scale(1.05);
        }

        footer {
            text-align: center;
            padding: 20px;
            background: #f5f5f5;
            color: #666;
            font-size: 0.9rem;
        }

        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 25px;
            background: #4caf50;
            color: white;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transform: translateX(100%);
            transition: transform 0.3s ease;
            z-index: 1000;
        }

        .notification.show {
            transform: translateX(0);
        }

        @media (max-width: 768px) {
            .payment-methods {
                grid-template-columns: 1fr;
            }
            
            header h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Payment Gateway</h1>
            <p>Pilih metode pembayaran yang Anda inginkan</p>
        </header>

        <div class="payment-methods">
            <div class="payment-card dana">
                <div class="card-header">
                    <h2>DANA</h2>
                </div>
                <div class="card-body">
                    <i class="fas fa-wallet"></i>
                    <p>085714353387</p>
                    <button class="copy-btn" data-number="085714353387">Salin Nomor</button>
                </div>
            </div>

            <div class="payment-card gopay">
                <div class="card-header">
                    <h2>GOPAY</h2>
                </div>
                <div class="card-body">
                    <i class="fab fa-google-wallet"></i>
                    <p>82962829928</p>
                    <button class="copy-btn" data-number="82962829928">Salin Nomor</button>
                </div>
            </div>

            <div class="payment-card ovo">
                <div class="card-header">
                    <h2>OVO</h2>
                </div>
                <div class="card-body">
                    <i class="fas fa-money-bill-wave"></i>
                    <p>9289290010</p>
                    <button class="copy-btn" data-number="9289290010">Salin Nomor</button>
                </div>
            </div>

            <div class="payment-card qris">
                <div class="card-header">
                    <h2>QRIS</h2>
                </div>
                <div class="card-body">
                    <i class="fas fa-qrcode"></i>
                    <img src="https://files.catbox.moe/7yokm2.jpg" alt="QR Code" class="qris-img">
                    <p>Scan QR Code untuk pembayaran</p>
                </div>
            </div>
        </div>

        <footer>
            <p>&copy; 2023 Payment Gateway. Semua hak dilindungi.</p>
        </footer>
    </div>

    <div class="notification" id="notification">
        Nomor berhasil disalin!
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const copyButtons = document.querySelectorAll('.copy-btn');
            const notification = document.getElementById('notification');
            
            copyButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const number = this.getAttribute('data-number');
                    copyToClipboard(number);
                    showNotification();
                });
            });
            
            function copyToClipboard(text) {
                const textarea = document.createElement('textarea');
                textarea.value = text;
                document.body.appendChild(textarea);
                textarea.select();
                document.execCommand('copy');
                document.body.removeChild(textarea);
            }
            
            function showNotification() {
                notification.classList.add('show');
                setTimeout(() => {
                    notification.classList.remove('show');
                }, 2000);
            }
        });
    </script>
</body>
</html>
