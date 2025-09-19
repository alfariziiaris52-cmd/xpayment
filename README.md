<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Payment Gateway</title>
    <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
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
            width: 100%;
            max-width: 800px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            animation: fadeIn 0.8s ease;
        }

        .header {
            background: linear-gradient(to right, #2575fc, #6a11cb);
            color: white;
            padding: 25px;
            text-align: center;
        }

        .header h1 {
            font-size: 28px;
            margin-bottom: 10px;
        }

        .header p {
            font-size: 16px;
            opacity: 0.9;
        }

        .payment-container {
            padding: 30px;
        }

        .payment-option {
            background: white;
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
            display: flex;
            align-items: center;
        }

        .payment-option:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .payment-icon {
            width: 60px;
            height: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 12px;
            margin-right: 20px;
            font-size: 28px;
            color: white;
        }

        .dana {
            background: linear-gradient(to right, #0084ff, #00a2ff);
        }

        .gopay {
            background: linear-gradient(to right, #00a64f, #00c853);
        }

        .ovo {
            background: linear-gradient(to right, #4c2c92, #673ab7);
        }

        .qris {
            background: linear-gradient(to right, #ff6600, #ff9900);
        }

        .payment-details {
            flex: 1;
        }

        .payment-details h3 {
            font-size: 20px;
            margin-bottom: 8px;
            color: #333;
        }

        .payment-details p {
            color: #666;
            font-size: 16px;
            margin-bottom: 5px;
        }

        .copy-btn {
            background: #f5f5f5;
            border: none;
            padding: 8px 15px;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s ease;
            font-size: 14px;
            color: #444;
        }

        .copy-btn:hover {
            background: #e0e0e0;
        }

        .qr-container {
            text-align: center;
            margin-top: 10px;
            display: none;
            animation: fadeIn 0.5s ease;
        }

        .qr-code {
            max-width: 250px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin: 15px auto;
        }

        .footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 14px;
            border-top: 1px solid #eee;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 15px 25px;
            background: #4caf50;
            color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            animation: fadeIn 0.5s ease;
            display: none;
            z-index: 1000;
        }

        @media (max-width: 768px) {
            .payment-option {
                flex-direction: column;
                text-align: center;
            }

            .payment-icon {
                margin-right: 0;
                margin-bottom: 15px;
            }

            .container {
                border-radius: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Payment Gateway</h1>
            <p>Pilih metode pembayaran yang Anda inginkan</p>
        </div>

        <div class="payment-container">
            <div class="payment-option" onclick="toggleQR('dana')">
                <div class="payment-icon dana">
                    <i class="fas fa-wallet"></i>
                </div>
                <div class="payment-details">
                    <h3>DANA</h3>
                    <p>085714353387</p>
                    <button
                        class="copy-btn"
                        onclick="event.stopPropagation(); copyToClipboard('085714353387', 'Nomor DANA')"
                    >
                        <i class="fas fa-copy"></i> Salin Nomor
                    </button>
                </div>
            </div>

            <div class="payment-option" onclick="toggleQR('gopay')">
                <div class="payment-icon gopay">
                    <i class="fab fa-google-wallet"></i>
                </div>
                <div class="payment-details">
                    <h3>GOPAY</h3>
                    <p>Tidak tersedia</p>
                </div>
            </div>

            <div class="payment-option" onclick="toggleQR('ovo')">
                <div class="payment-icon ovo">
                    <i class="fas fa-money-bill-wave"></i>
                </div>
                <div class="payment-details">
                    <h3>OVO</h3>
                    <p>Tidak tersedia</p>
                </div>
            </div>

            <div class="payment-option" onclick="toggleQR('qris')">
                <div class="payment-icon qris">
                    <i class="fas fa-qrcode"></i>
                </div>
                <div class="payment-details">
                    <h3>QRIS</h3>
                    <p>Scan kode QR untuk pembayaran</p>
                </div>
            </div>

            <!-- QR Code Containers -->
            <div id="dana-qr" class="qr-container">
                <img
                    src="https://files.catbox.moe/7yokm2.jpg"
                    alt="DANA QR Code"
                    class="qr-code"
                />
                <p>Scan QR code di atas untuk pembayaran via DANA</p>
            </div>

            <div id="gopay-qr" class="qr-container">
                <p>Metode pembayaran GOPAY tidak tersedia saat ini.</p>
            </div>

            <div id="ovo-qr" class="qr-container">
                <p>Metode pembayaran OVO tidak tersedia saat ini.</p>
            </div>

            <div id="qris-qr" class="qr-container">
                <img
                    src="https://files.catbox.moe/7yokm2.jpg"
                    alt="QRIS Code"
                    class="qr-code"
                />
                <p>Scan QR code di atas untuk pembayaran via QRIS</p>
            </div>
        </div>

        <div class="footer">
            <p>© 2023 Payment Gateway. Semua hak dilindungi.</p>
        </div>
    </div>

    <!-- Notification popup -->
    <div class="notification" id="notification">
        <i class="fas fa-check-circle"></i> <span id="notification-text"></span>
    </div>

    <script>
        // Fungsi untuk menampilkan QR code sesuai pilihan
        function toggleQR(type) {
            // Sembunyikan semua QR container
            document.querySelectorAll('.qr-container').forEach((qr) => {
                qr.style.display = 'none';
            });

            // Tampilkan QR container yang dipilih
            const selectedQR = document.getElementById(`${type}-qr`);
            if (selectedQR) {
                selectedQR.style.display = 'block';
            }
        }

        // Fungsi untuk menyalin teks ke clipboard
        function copyToClipboard(text, type) {
            if (text === 'Tidak tersedia') {
                showNotification('Metode pembayaran tidak tersedia');
                return;
            }

            navigator.clipboard
                .writeText(text)
                .then(() => {
                    showNotification(`${type} berhasil disalin: ${text}`);
                })
                .catch((err) => {
                    console.error('Gagal menyalin teks: ', err);
                    showNotification('Gagal menyalin teks');
                });
        }

        // Fungsi menampilkan notifikasi sementara
        function showNotification(message) {
            const notification = document.getElementById('notification');
            const notificationText = document.getElementById('notification-text');

            notificationText.textContent = message;
            notification.style.display = 'block';

            setTimeout(() => {
                notification.style.display = 'none';
            }, 3000);
        }

        // Saat halaman dimuat, sembunyikan semua QR container
        document.addEventListener('DOMContentLoaded', function () {
            document.querySelectorAll('.qr-container').forEach((qr) => {
                qr.style.display = 'none';
            });
        });
    </script>
</body>
</html>
