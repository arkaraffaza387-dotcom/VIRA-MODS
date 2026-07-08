<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FF MAX ULTRA MOD MENU</title>
    <style>
        body { background: #0a0a0a; color: #fff; font-family: 'Arial', sans-serif; text-align: center; margin: 0; }
        .overlay { background: rgba(0,0,0,0.9); height: 100vh; padding: 20px; }
        .container { border: 2px solid #ff0000; padding: 20px; border-radius: 15px; box-shadow: 0 0 20px #ff0000; max-width: 400px; margin: auto; }
        h1 { color: #ff0000; text-transform: uppercase; letter-spacing: 2px; }
        
        /* ID Input Section */
        .auth-box { margin-bottom: 20px; padding: 15px; border: 1px solid #444; border-radius: 10px; }
        input { width: 80%; padding: 10px; margin: 10px 0; background: #222; color: lime; border: 1px solid #ff0000; text-align: center; font-weight: bold; }
        
        /* Menu Section */
        .menu-section { display: none; text-align: left; }
        .feature-group { background: #1a1a1a; margin: 10px 0; padding: 10px; border-radius: 5px; border-left: 4px solid #ff0000; }
        .feature-group h3 { margin: 0 0 10px 0; font-size: 14px; color: #aaa; }
        
        .option { display: flex; justify-content: space-between; margin: 5px 0; font-size: 13px; }
        select { background: #333; color: white; border: 1px solid #555; }
        
        .switch { position: relative; width: 40px; height: 20px; }
        .switch input { opacity: 0; width: 0; height: 0; }
        .slider { position: absolute; cursor: pointer; top: 0; left: 0; right: 0; bottom: 0; background: #444; transition: .4s; border-radius: 20px; }
        input:checked + .slider { background: #ff0000; }
        .slider:before { position: absolute; content: ""; height: 14px; width: 14px; left: 3px; bottom: 3px; background: white; transition: .4s; border-radius: 50%; }
        input:checked + .slider:before { transform: translateX(20px); }

        .btn-main { background: #ff0000; color: white; border: none; padding: 15px 30px; font-weight: bold; cursor: pointer; width: 100%; border-radius: 5px; margin-top: 20px; }
    </style>
</head>
<body>

<div class="overlay">
    <div class="container">
        <h1>FF MAX MOD</h1>
        
        <!-- Step 1: Auth ID -->
        <div id="authSection" class="auth-box">
            <p>Masukkan ID Akun FF MAX Anda:</p>
            <input type="number" id="playerID" placeholder="Contoh: 123456789">
            <button class="btn-main" onclick="verifyID()">VERIFIKASI AKUN</button>
        </div>

        <!-- Step 2: Cheat Menu -->
        <div id="menuSection" class="menu-section">
            <div class="feature-group">
                <h3>🎯 AIMBOT SETTINGS</h3>
                <div class="option">
                    <span>Aimbot Mode</span>
                    <select id="aimMode">
                        <option value="body">Body Only</option>
                        <option value="body_hs">Body + Headshot</option>
                        <option value="full_hs">Full Headshot</option>
                    </select>
                </div>
                <div class="option">
                    <span>POV Circle (FOV)</span>
                    <select id="fovSize">
                        <option value="small">Small (Accurate)</option>
                        <option value="medium">Medium</option>
                        <option value="large">Large (Wide)</option>
                    </select>
                </div>
            </div>

            <div class="feature-group">
                <h3>👁️ VISUALS (ESP)</h3>
                <div class="option">
                    <span>ESP Line (Enemy)</span>
                    <label class="switch"><input type="checkbox"><span class="slider"></span></label>
                </div>
                <div class="option">
                    <span>ESP Box (Enemy)</span>
                    <label class="switch"><input type="checkbox"><span class="slider"></span></label>
                </div>
                <div class="option">
                    <span>Show Distance</span>
                    <label class="switch"><input type="checkbox"><span class="slider"></span></label>
                </div>
            </div>

            <div class="feature-group">
                <h3>🛡️ SYSTEM</h3>
                <div class="option">
                    <span>Anti-Ban Bypass</span>
                    <label class="switch"><input type="checkbox" checked disabled><span class="slider"></span></label>
                </div>
                <div class="option">
                    <span>Bypass Login Error</span>
                    <label class="switch"><input type="checkbox" id="bypass"><span class="slider"></span></label>
                </div>
            </div>

            <button class="btn-main" onclick="inject()">INJECT TO FF MAX</button>
        </div>
    </div>
</div>

<script>
    function verifyID() {
        let id = document.getElementById('playerID').value;
        if(id.length < 5) {
            alert("ID Tidak Valid!");
        } else {
            document.getElementById('authSection').style.display = 'none';
            document.getElementById('menuSection').style.display = 'block';
        }
    }

    function inject() {
        alert("Connecting to FF MAX Process...");
        setTimeout(() => {
            alert("Injecting Memory Offsets... Aimbot, ESP, and Bypass Active!");
            // Di sini kamu seharusnya mengarahkan ke link download MOD APK yang sudah jadi
            window.location.href = "https://your-server.com/FF_MAX_MOD_REAL.apk";
        }, 3000);
    }
</script>

</body>
</html>
