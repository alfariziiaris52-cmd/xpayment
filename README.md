<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MURID STORE - Jasa Digital & Tools Premium</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #4a00e0;
            --secondary: #8e2de2;
            --accent: #00c6ff;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #28a745;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding-bottom: 2rem;
        }
        
        header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 1.5rem 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 0.5rem;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: var(--accent);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .hero {
            padding: 4rem 0;
            text-align: center;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1516387938699-a93567ec168e?ixlib=rb-4.0.3') center/cover;
            color: white;
            border-radius: 0 0 20px 20px;
            margin-bottom: 2rem;
        }
        
        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(0, 198, 255, 0.3);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 198, 255, 0.4);
        }
        
        .btn-primary {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            box-shadow: 0 4px 15px rgba(138, 43, 226, 0.3);
        }
        
        .btn-primary:hover {
            box-shadow: 0 6px 20px rgba(138, 43, 226, 0.4);
        }
        
        .categories {
            margin-bottom: 2rem;
            text-align: center;
        }
        
        .categories h2 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .category-buttons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        .category-btn {
            background: white;
            border: 2px solid var(--primary);
            color: var(--primary);
            padding: 0.6rem 1.2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 500;
        }
        
        .category-btn:hover, .category-btn.active {
            background: var(--primary);
            color: white;
        }
        
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .product-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .product-image {
            height: 180px;
            background: linear-gradient(45deg, #6a11cb 0%, #2575fc 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }
        
        .product-info p {
            color: #666;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }
        
        .product-price {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .buy-btn {
            width: 100%;
            padding: 0.8rem;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 8px;
            font-weight: 500;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .buy-btn:hover {
            background: var(--secondary);
        }
        
        .payment-section {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 2rem;
            text-align: center;
        }
        
        .payment-section h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
        }
        
        .payment-options {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }
        
        .payment-method {
            background: var(--light);
            padding: 1.5rem;
            border-radius: 10px;
            width: 280px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
        }
        
        .payment-method h3 {
            margin-bottom: 1rem;
            color: var(--dark);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }
        
        .qris-code {
            width: 200px;
            height: 200px;
            margin: 0 auto 1rem;
            background: white;
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .qris-code img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }
        
        .dana-info {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
        }
        
        .dana-logo {
            font-size: 3rem;
            color: var(--primary);
        }
        
        .dana-number {
            font-size: 1.2rem;
            font-weight: 600;
            background: var(--light);
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
        }
        
        footer {
            text-align: center;
            padding: 2rem 0;
            color: #666;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            nav ul {
                gap: 0.5rem;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 0.5rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .products {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
            
            .payment-options {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-store"></i>
                    MURID STORE
                </div>
                <nav>
                    <ul>
                        <li><a href="#products">Produk</a></li>
                        <li><a href="#payment">Pembayaran</a></li>
                        <li><a href="#contact">Kontak</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h1>MURID STORE</h1>
            <p>Jasa Digital & Tools Premium Terbaik dan Terpercaya</p>
            <a href="#products" class="btn">Lihat Produk</a>
        </div>
    </section>
    
    <div class="container">
        <section class="categories">
            <h2>Kategori Produk</h2>
            <div class="category-buttons">
                <button class="category-btn active" data-category="all">Semua Produk</button>
                <button class="category-btn" data-category="murid">Murid Products</button>
                <button class="category-btn" data-category="apk">APK</button>
                <button class="category-btn" data-category="sc">Source Code</button>
            </div>
        </section>
        
        <section id="products" class="products">
            <!-- Produk akan ditampilkan di sini -->
        </section>
        
        <section id="payment" class="payment-section">
            <h2>Metode Pembayaran</h2>
            <div class="payment-options">
                <div class="payment-method">
                    <h3><i class="fas fa-qrcode"></i> QRIS</h3>
                    <div class="qris-code">
                        <img src="https://files.catbox.moe/7yokm2.jpg" alt="QR Code Pembayaran QRIS">
                    </div>
                    <p>Scan QR code di atas untuk pembayaran via QRIS</p>
                </div>
                
                <div class="payment-method">
                    <h3><i class="fas fa-wallet"></i> DANA</h3>
                    <div class="dana-info">
                        <div class="dana-logo">
                            <i class="fas fa-wallet"></i>
                        </div>
                        <div class="dana-number">085714353387</div>
                        <p>Transfer ke nomor DANA di atas</p>
                    </div>
                </div>
            </div>
        </section>
    </div>
    
    <footer>
        <div class="container">
            <p>&copy; 2023 MURID STORE - All rights reserved</p>
        </div>
    </footer>

    <script>
        // Data produk
        const products = [
            { 
                id: 1, 
                name: "MURID UNBAND WHATSAPP", 
                description: "Layanan unband WhatsApp premium", 
                price: "Rp 50.000", 
                category: "murid",
                icon: "fab fa-whatsapp"
            },
            { 
                id: 2, 
                name: "MURID BAND WHATSAPP", 
                description: "Layanan band WhatsApp berkualitas", 
                price: "Rp 45.000", 
                category: "murid",
                icon: "fab fa-whatsapp"
            },
            { 
                id: 3, 
                name: "MURID BAND TIKTOK", 
                description: "Layanan band TikTok terpercaya", 
                price: "Rp 55.000", 
                category: "murid",
                icon: "fab fa-tiktok"
            },
            { 
                id: 4, 
                name: "MURID UNBAND TELEGRAM", 
                description: "Layanan unband Telegram premium", 
                price: "Rp 60.000", 
                category: "murid",
                icon: "fab fa-telegram"
            },
            { 
                id: 5, 
                name: "MURID BAND TELEGRAM", 
                description: "Layanan band Telegram terpercaya", 
                price: "Rp 55.000", 
                category: "murid",
                icon: "fab fa-telegram"
            },
            { 
                id: 6, 
                name: "MURID NOKOS", 
                description: "Layanan NOKOS berkualitas tinggi", 
                price: "Rp 65.000", 
                category: "murid",
                icon: "fas fa-phone"
            },
            { 
                id: 7, 
                name: "MURID SUNTIK ALL SOSMED", 
                description: "Layanan suntik semua sosial media", 
                price: "Rp 75.000", 
                category: "murid",
                icon: "fas fa-syringe"
            },
            { 
                id: 8, 
                name: "MURID LOGO", 
                description: "Jasa pembuatan logo profesional", 
                price: "Rp 100.000", 
                category: "murid",
                icon: "fas fa-paint-brush"
            },
            { 
                id: 9, 
                name: "MURID UP PAYMENT", 
                description: "Layanan upgrade payment gateway", 
                price: "Rp 85.000", 
                category: "murid",
                icon: "fas fa-credit-card"
            },
            { 
                id: 10, 
                name: "MURID RENAME APK", 
                description: "Jasa rename APK profesional", 
                price: "Rp 70.000", 
                category: "murid",
                icon: "fas fa-mobile"
            },
            { 
                id: 11, 
                name: "APK RANSOMWARE", 
                description: "Aplikasi ransomware premium", 
                price: "Rp 150.000", 
                category: "apk",
                icon: "fas fa-lock"
            },
            { 
                id: 12, 
                name: "SC JASEB", 
                description: "Source code JASEB lengkap", 
                price: "Rp 200.000", 
                category: "sc",
                icon: "fas fa-code"
            },
            { 
                id: 13, 
                name: "SC JASHER", 
                description: "Source code JASHER terbaru", 
                price: "Rp 180.000", 
                category: "sc",
                icon: "fas fa-code"
            },
            { 
                id: 14, 
                name: "SC CPANEL", 
                description: "Source code CPanel premium", 
                price: "Rp 220.000", 
                category: "sc",
                icon: "fas fa-server"
            },
            { 
                id: 15, 
                name: "SC UBOT(VIA PANEL)", 
                description: "Source code UBot dengan panel", 
                price: "Rp 250.000", 
                category: "sc",
                icon: "fas fa-robot"
            },
            { 
                id: 16, 
                name: "APK SADAP", 
                description: "Aplikasi sadap premium", 
                price: "Rp 175.000", 
                category: "apk",
                icon: "fas fa-bug"
            },
            { 
                id: 17, 
                name: "UBOT SADAP TELEGRAM", 
                description: "UBot untuk sadap Telegram", 
                price: "Rp 190.000", 
                category: "sc",
                icon: "fab fa-telegram"
            },
            { 
                id: 18, 
                name: "SC DDOS WEB", 
                description: "Source code DDOS website", 
                price: "Rp 160.000", 
                category: "sc",
                icon: "fas fa-shield-alt"
            },
            { 
                id: 19, 
                name: "BASE SC", 
                description: "Base source code lengkap", 
                price: "Rp 120.000", 
                category: "sc",
                icon: "fas fa-file-code"
            },
            { 
                id: 20, 
                name: "SC BUG", 
                description: "Source code bug terbaru", 
                price: "Rp 140.000", 
                category: "sc",
                icon: "fas fa-bug"
            },
            { 
                id: 21, 
                name: "FUNC BUG", 
                description: "Fungsi bug terkini", 
                price: "Rp 130.000", 
                category: "sc",
                icon: "fas fa-code-branch"
            },
            { 
                id: 22, 
                name: "MURBAND CH", 
                description: "Layanan MURBAND CH premium", 
                price: "Rp 90.000", 
                category: "murid",
                icon: "fas fa-comments"
            },
            { 
                id: 23, 
                name: "MURID RESET OTP", 
                description: "Layanan reset OTP profesional", 
                price: "Rp 85.000", 
                category: "murid",
                icon: "fas fa-sync"
            },
            { 
                id: 24, 
                name: "APK JB", 
                description: "Aplikasi JB terbaru", 
                price: "Rp 110.000", 
                category: "apk",
                icon: "fas fa-tools"
            },
            { 
                id: 25, 
                name: "APK FF BETA", 
                description: "Aplikasi FF Beta version", 
                price: "Rp 95.000", 
                category: "apk",
                icon: "fas fa-gamepad"
            },
            { 
                id: 26, 
                name: "APK BIOSKOP", 
                description: "Aplikasi bioskop premium", 
                price: "Rp 80.000", 
                category: "apk",
                icon: "fas fa-film"
            },
            { 
                id: 27, 
                name: "APK SPOTIFY PREM", 
                description: "Aplikasi Spotify premium", 
                price: "Rp 75.000", 
                category: "apk",
                icon: "fab fa-spotify"
            }
        ];

        // Fungsi untuk menampilkan produk
        function displayProducts(category = 'all') {
            const productsContainer = document.getElementById('products');
            productsContainer.innerHTML = '';
            
            const filteredProducts = category === 'all' 
                ? products 
                : products.filter(product => product.category === category);
            
            filteredProducts.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                productCard.innerHTML = `
                    <div class="product-image">
                        <i class="${product.icon}"></i>
                    </div>
                    <div class="product-info">
                        <h3>${product.name}</h3>
                        <p>${product.description}</p>
                        <div class="product-price">${product.price}</div>
                        <button class="buy-btn">Beli Sekarang</button>
                    </div>
                `;
                
                productsContainer.appendChild(productCard);
            });
        }
        
        // Event listener untuk kategori
        document.querySelectorAll('.category-btn').forEach(button => {
            button.addEventListener('click', function() {
                document.querySelectorAll('.category-btn').forEach(btn => btn.classList.remove('active'));
                this.classList.add('active');
                
                const category = this.getAttribute('data-category');
                displayProducts(category);
            });
        });
        
        // Inisialisasi tampilan
        document.addEventListener('DOMContentLoaded', function() {
            displayProducts();
            
            // Smooth scroll untuk navigasi
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>