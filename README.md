<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sedang Pembaruan</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap');

        * {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #050508 0%, #101827 50%, #0b1120 100%);
            min-height: 100vh;
        }

        /* --- HALAMAN PEMELIHARAAN --- */
        .bg-effect {
            position: fixed;
            width: 200%;
            height: 200%;
            background: 
                radial-gradient(circle at 20% 20%, rgba(59, 130, 246, 0.08) 0%, transparent 40%),
                radial-gradient(circle at 80% 70%, rgba(16, 185, 129, 0.08) 0%, transparent 40%);
            animation: float 20s ease-in-out infinite alternate;
        }

        @keyframes float {
            0% { transform: translate(0, 0) rotate(0deg); }
            100% { transform: translate(-40px, -40px) rotate(5deg); }
        }

        .main-card {
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(75, 85, 99, 0.3);
            border-radius: 28px;
            position: relative;
            overflow: hidden;
        }

        .main-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, transparent, #3b82f6, #10b981, transparent);
            animation: loadingLine 3s linear infinite;
        }

        @keyframes loadingLine {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        .time-box {
            background: linear-gradient(145deg, rgba(30, 41, 59, 0.9), rgba(15, 23, 42, 0.9));
            border: 1px solid rgba(59, 130, 246, 0.25);
            border-radius: 16px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3), inset 0 1px 0 rgba(255,255,255,0.05);
            transition: all 0.3s ease;
        }

        .time-box:hover {
            transform: translateY(-4px);
            border-color: rgba(59, 130, 246, 0.5);
            box-shadow: 0 12px 40px rgba(59, 130, 246, 0.15);
        }

        .icon-rotate {
            animation: rotate 8s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .progress-bar {
            height: 6px;
            background: rgba(59, 130, 246, 0.15);
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #3b82f6, #10b981);
            border-radius: 10px;
            transition: width 0.5s ease;
        }

        /* --- HALAMAN SELESAI UPDATE --- */
        .bg-glow {
            position: fixed;
            width: 150%;
            height: 150%;
            background: radial-gradient(circle at 10% 20%, rgba(37, 99, 235, 0.08) 0%, transparent 20%),
                        radial-gradient(circle at 80% 80%, rgba(16, 185, 129, 0.08) 0%, transparent 20%);
            animation: moveGlow 15s ease-in-out infinite alternate;
        }

        @keyframes moveGlow {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-30px, -30px); }
        }

        .card-shine {
            position: relative;
            background: rgba(17, 25, 40, 0.85);
            backdrop-filter: blur(16px);
            border-radius: 24px;
            overflow: hidden;
        }

        .card-shine::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(16, 185, 129, 0.1), transparent);
            transform: rotate(45deg);
            animation: shine 4s linear infinite;
        }

        @keyframes shine {
            0% { transform: translateX(-100%) rotate(45deg); }
            100% { transform: translateX(100%) rotate(45deg); }
        }

        .icon-pulse {
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.4); }
            50% { box-shadow: 0 0 0 20px rgba(37, 211, 102, 0); }
        }

        .btn-wa {
            background: linear-gradient(135deg, #22c55e, #16a34a);
            box-shadow: 0 4px 20px rgba(34, 197, 94, 0.4);
            transition: all 0.3s ease;
        }

        .btn-wa:hover {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 8px 30px rgba(34, 197, 94, 0.5);
            background: linear-gradient(135deg, #16a34a, #15803d);
        }

        /* Sembunyikan secara bergantian */
        .halaman { display: none; }
        .aktif { display: flex; }
    </style>
</head>
<body>

    <!-- HALAMAN 1: SEDANG PEMELIHARAAN -->
    <div id="halamanPemeliharaan" class="halaman aktif">
        <div class="bg-effect"></div>
        <div class="main-card w-full max-w-lg p-8 md:p-10 z-10 text-center">
            <div class="icon-rotate w-24 h-24 mx-auto mb-5 rounded-full bg-gradient-to-br from-blue-500/20 to-emerald-500/20 flex items-center justify-center">
                <i class="fa fa-cog text-blue-400 text-4xl"></i>
            </div>

            <span class="inline-block px-5 py-1.5 bg-blue-500/10 text-blue-300 text-sm font-semibold rounded-full mb-4">
                ⚙️ SEDANG DALAM PEMELIHARAAN
            </span>

            <h2 class="text-2xl md:text-3xl font-bold text-white mb-3">Pembaruan Sistem & Patch</h2>
            <p class="text-gray-400 mb-7">
                Kami sedang meningkatkan fitur, memperbaiki kinerja, dan menyiapkan hal baru yang lebih baik. Sistem akan kembali segera setelah selesai.
            </p>

            <p class="text-gray-500 text-sm mb-4"><i class="fa fa-clock-o mr-1"></i> Diperkirakan Selesai Dalam:</p>

            <div class="grid grid-cols-4 gap-3 mb-8">
                <div class="time-box p-4">
                    <div id="hari" class="text-2xl md:text-3xl font-bold text-white mb-1">00</div>
                    <div class="text-gray-500 text-xs uppercase tracking-wider">Hari</div>
                </div>
                <div class="time-box p-4">
                    <div id="jam" class="text-2xl md:text-3xl font-bold text-white mb-1">00</div>
                    <div class="text-gray-500 text-xs uppercase tracking-wider">Jam</div>
                </div>
                <div class="time-box p-4">
                    <div id="menit" class="text-2xl md:text-3xl font-bold text-white mb-1">10</div>
                    <div class="text-gray-500 text-xs uppercase tracking-wider">Menit</div>
                </div>
                <div class="time-box p-4">
                    <div id="detik" class="text-2xl md:text-3xl font-bold text-white mb-1">00</div>
                    <div class="text-gray-500 text-xs uppercase tracking-wider">Detik</div>
                </div>
            </div>

            <div class="progress-bar mb-3">
                <div id="bar" class="progress-fill" style="width: 0%"></div>
            </div>
            <p id="status" class="text-gray-500 text-xs mb-7">Sedang memproses pembaruan...</p>

            <div class="p-5 bg-green-500/5 border border-green-500/20 rounded-xl">
                <p class="text-gray-400 text-sm mb-3">
                    <i class="fa fa-info-circle text-green-400 mr-1"></i> Dapatkan info terbaru kapan selesai & kabar pembaruan di sini:
                </p>
                <a href="https://whatsapp.com/channel/0029Vb8BNYv72WTwCFiq2k3p" target="_blank" rel="noopener noreferrer" 
                   class="inline-flex items-center justify-center w-full bg-gradient-to-r from-green-500 to-emerald-600 hover:from-green-600 hover:to-emerald-700 text-white font-semibold py-3 px-4 rounded-lg transition-all shadow-lg shadow-green-500/20">
                    <i class="fa fa-whatsapp mr-2"></i> Gabung Komunitas Pembaruan
                </a>
            </div>
        </div>
    </div>
    <!-- AKHIR HALAMAN PEMELIHARAAN -->


    <!-- HALAMAN 2: SUDAH SELESAI UPDATE -->
    <div id="halamanSelesai" class="halaman">
        <div class="bg-glow"></div>
        <div class="card-shine w-full max-w-md p-8 z-10 text-center">
            <div class="icon-pulse w-28 h-28 mx-auto mb-6 rounded-full bg-gradient-to-br from-green-400 to-emerald-600 flex items-center justify-center">
                <i class="fa fa-check-circle text-white text-5xl"></i>
            </div>

            <span class="inline-block px-4 py-1 bg-green-500/10 text-green-400 text-sm font-semibold rounded-full mb-4">
                ✨ PEMBARUAN TELAH SELESAI
            </span>

            <h2 class="text-3xl font-bold text-white mb-3">Versi Baru Telah Hadir!</h2>
            <p class="text-gray-400 leading-relaxed mb-2">
                Kami telah melakukan penyempurnaan, perbaikan masalah, dan penambahan fitur baru yang lebih menarik.
            </p>
            <p class="text-gray-500 text-sm mb-8">
                Dapatkan pembaruan ini secara eksklusif melalui Komunitas Resmi kami.
            </p>

            <a href="https://whatsapp.com/channel/0029Vb8BNYv72WTwCFiq2k3p" target="_blank" rel="noopener noreferrer" 
               class="btn-wa block w-full text-white font-bold py-4 px-6 rounded-xl text-lg">
                <i class="fa fa-paper-plane mr-2"></i> Bergabung Sekarang
            </a>

            <div class="mt-6 pt-4 border-t border-gray-700/50">
                <p class="text-gray-600 text-xs">
                    <i class="fa fa-shield mr-1"></i> Aman & Terpercaya • Dapatkan Info Terkini
                </p>
            </div>
        </div>
    </div>
    <!-- AKHIR HALAMAN SELESAI -->


    <script>
        // ⚙️ PENGATURAN WAKTU TETAP
        const waktuMulai = new Date(2026, 6, 9, 15, 30, 0).getTime(); // 9 Juli 2026 jam 15.30
        const durasiTotal = 10 * 60; // Durasi 10 Menit
        const waktuSelesai = waktuMulai + (durasiTotal * 1000);

        function gantiKeSelesai() {
            document.getElementById('halamanPemeliharaan').classList.remove('aktif');
            document.getElementById('halamanSelesai').classList.add('aktif');
        }

        function hitungMundur() {
            const sekarang = new Date().getTime();
            const sisaWaktu = waktuSelesai - sekarang;

            // Belum waktunya mulai
            if (sekarang < waktuMulai) {
                document.getElementById('hari').innerText = '00';
                document.getElementById('jam').innerText = '00';
                document.getElementById('menit').innerText = '10';
                document.getElementById('detik').innerText = '00';
                document.getElementById('bar').style.width = '0%';
                document.getElementById('status').innerText = `Pembaruan akan dimulai 9 Juli 15.30`;
                return;
            }

            // Waktu sudah habis -> GANTI KE HALAMAN SELESAI
            if (sisaWaktu <= 0) {
                gantiKeSelesai();
                return;
            }

            // Masih berjalan
            let hari = Math.floor(sisaWaktu / (1000 * 60 * 60 * 24));
            let jam = Math.floor((sisaWaktu % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            let menit = Math.floor((sisaWaktu % (1000 * 60 * 60)) / (1000 * 60));
            let detik = Math.floor((sisaWaktu % (1000 * 60)) / 1000);

            document.getElementById('hari').innerText = hari.toString().padStart(2, '0');
            document.getElementById('jam').innerText = jam.toString().padStart(2, '0');
            document.getElementById('menit').innerText = menit.toString().padStart(2, '0');
            document.getElementById('detik').innerText = detik.toString().padStart(2, '0');

            const berjalan = sekarang - waktuMulai;
            const persen = Math.min(100, (berjalan / (durasiTotal * 1000)) * 100);
            document.getElementById('bar').style.width = persen + '%';
            document.getElementById('status').innerText = `Sedang memproses... ${Math.round(persen)}%`;
        }

        // Jalankan terus
        hitungMundur();
        setInterval(hitungMundur, 1000);
    </script>

</body>
</html>
