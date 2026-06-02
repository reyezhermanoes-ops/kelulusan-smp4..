<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portal Kelulusan SMPN 4</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f6f9; text-align: center; padding: 50px 20px; }
        .container { max-width: 500px; background: white; padding: 30px; margin: auto; border-radius: 8px; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        h2 { color: #333; margin-bottom: 20px; }
        input[type="text"] { width: 90%; padding: 12px; margin: 10px 0; border: 1px solid #ccc; border-radius: 4px; font-size: 16px; box-sizing: border-box; }
        button { width: 90%; padding: 12px; background-color: #007bff; color: white; border: none; border-radius: 4px; font-size: 16px; cursor: pointer; font-weight: bold; }
        button:hover { background-color: #0056b3; }
        .result { margin-top: 25px; padding: 15px; border-radius: 5px; display: none; text-align: left; }
        .failed { background-color: #f8d7da; color: #721c24; border: 1px solid #f5c6cb; }
        .status-badge { display: inline-block; padding: 5px 10px; background-color: #dc3545; color: white; border-radius: 4px; font-weight: bold; margin-top: 5px; }
    </style>
</head>
<body>

<div class="container">
    <h2>Sistem Informasi Kelulusan <br>SMPN 4</h2>
    <p>Masukkan NISN atau Nama Lengkap Siswa untuk mengecek status kelulusan tahun ajaran ini.</p>
    
    <input type="text" id="userInput" placeholder="Contoh: 0081234567 atau Budi Santoso">
    <button onclick="cekKelulusan()">CARI DATA</button>

    <div id="resultBox" class="result failed">
        <p><strong>Hasil Pencarian:</strong></p>
        <p>Nama / NISN: <span id="searchKey" style="font-weight: bold; color: #333;"></span></p>
        <p>Status Kelulusan:</p>
        <span class="status-badge">TIDAK LULUS</span>
        <p style="font-size: 13px; margin-top: 10px; color: #666;">*Silakan hubungi pihak sekolah atau wali kelas untuk informasi lebih lanjut.</p>
    </div>
</div>

<script>
function cekKelulusan() {
    var input = document.getElementById("userInput").value.trim();
    if (input === "") {
        alert("Mohon masukkan Nama atau NISN terlebih dahulu!");
        return;
    }
    document.getElementById("searchKey").innerText = input;
    document.getElementById("resultBox").style.display = "block";
}
</script>

</body>
</html>