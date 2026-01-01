BCA MONITOR v4.x

Ringkasan

BCA MONITOR adalah LPZ (Liquidity Projection Zone) & Mission Stacking Audit Tool berbasis input OHLC manual. Tool ini dirancang untuk audit, review, dan disiplin eksekusi, bukan auto trading atau signal generator.


---

Tujuan Utama

Audit level harga (LPZ) secara objektif

Menjaga disiplin eksekusi (anti-FOMO)

Mencatat & mengevaluasi hasil misi trading

Risk awareness (News Sentinel & context market)



---

Fitur Utama

1. Core Engine

Input OHLC manual (Open, High, Low, Close)

Perhitungan LPZ sekali saat misi dibuat (anti repaint)

Arah otomatis BUY / SELL berdasarkan candle


2. Timeframe & VRE

TF: M5, M15, M30, H1, H2, H4, D1

Setiap TF punya VRE (Volatility Range Expansion) berbeda


3. Stacking Mission (Misi Berlapis)

Bisa membuat banyak misi sekaligus

Tidak overwrite misi lama

Setiap misi punya ID unik


4. Mission Status

Status resmi: ACTIVE, TOUCHED, FAILED, TIMEOUT

Status berubah manual atau saat harga menyentuh LPZ


5. Manual Price Monitor

Harga dimasukkan manual (audit mode)

Trigger otomatis saat LPZ tersentuh


6. News Sentinel (Risk Control)

Countdown news manual

Warning visual + audio 5 menit sebelum news

Tidak mempengaruhi logic misi


7. Journal & Audit Log

Semua perubahan status tercatat

Data: TF, BUY/SELL, LPZ, status, context, timestamp

Export audit ke file .TXT


8. Maintenance (Add-Only)

Clear Audit Log (hapus jurnal saja)

Reset All Data (hapus semua data dengan konfirmasi)



---

Data & Penyimpanan

Menggunakan localStorage

Key utama:

bcaMissions

bcaJournal


Aman refresh & tutup browser



---

Yang Sengaja Tidak Ada

❌ Auto trading

❌ Auto signal

❌ Real-time market feed

❌ AI decision engine

❌ Indikator teknikal



---

Prinsip Audit

Core engine HARAM DIUBAH

Semua upgrade HARUS ADD-ONLY

Tidak boleh mengubah logic inti



---

Pernyataan Audit

> File ini tidak mengubah core logic, tidak menghapus fitur lama, dan seluruh perubahan bersifat ADD-ONLY.




---

BCA MONITOR = Audit Tool, bukan Signal Tool.


Siap. Ini LIST FITUR YANG SUDAH ADA di BCA MONITOR v4.1.x – STACKING MISSION, tanpa tafsir, tanpa janji, tanpa tambahan. Murni inventaris fitur.
📋 LIST FITUR — BCA MONITOR v4.x
🧠 CORE ENGINE
Input OHLC manual (Open, High, Low, Close)
Validasi input (misi tidak dibuat jika OHLC tidak lengkap)
Tidak ada auto-candle
Tidak ada feed harga real-time
🎯 LPZ (Liquidity Projection Zone)
Perhitungan LPZ berbasis:
Range candle (|Close − Open|)
Multiplier VRE per timeframe
Arah otomatis:
Bullish → BUY
Bearish → SELL
Presisi harga hingga 3 desimal
LPZ dihitung sekali saat misi dibuat (anti repaint)
⏱️ TIMEFRAME & VRE SYSTEM
Timeframe tersedia:
M5
M15
M30
H1
H2
H4
D1
VRE berbeda dan tetap per TF (hard-coded, audit-safe)
🧩 STACKING MISSION (MISI BERLAPIS)
Bisa membuat lebih dari satu misi
Tidak overwrite misi sebelumnya
Bisa stack:
TF yang sama
TF berbeda
Setiap misi punya ID unik
📌 MISSION STATUS SYSTEM
Status resmi:
ACTIVE
TOUCHED
FAILED
TIMEOUT
Fitur status:
Status berubah manual (FAIL / T.O)
Status berubah otomatis saat harga menyentuh LPZ
Tidak ada auto-reset status
Tidak ada auto-delete misi
💰 MANUAL PRICE MONITOR
Input harga manual
Cek harga hanya terhadap misi ACTIVE
Trigger:
BUY → harga ≥ LPZ
SELL → harga ≤ LPZ
🔔 AUDIO ALERT
Audio beep berbasis Web Audio API
Beep saat:
LPZ tersentuh
Warning news
Tidak menggunakan file audio eksternal
📰 NEWS SENTINEL (RISK AWARENESS)
Input jam news manual
Countdown real-time
Warning aktif 5 menit sebelum news
Visual flashing (emergency mode)
Audio peringatan berkala
Tidak mempengaruhi logic misi
🧠 MARKET CONTEXT TAGGING
Pilihan konteks market:
RANGING
TRENDING
VOLATILE
Context disimpan per misi
Context dicatat ke audit log
📒 JOURNAL & AUDIT LOG
Semua perubahan status dicatat
Data log berisi:
Timeframe
BUY / SELL
Harga LPZ
Status
Market context
Timestamp
Tampilan 5 log terakhir di tabel
📤 EXPORT DATA
Export audit log ke file .TXT
Format teks audit-friendly
Tanpa server / backend
🧹 MAINTENANCE & CONTROL (ADD-ONLY)
Clear Audit Log (hapus jurnal saja)
Reset All Data (hapus semua data dengan konfirmasi user)
💾 DATA PERSISTENCE
Penyimpanan via localStorage
Key tetap:
bcaMissions
bcaJournal
Data aman saat refresh / reload
🎨 VISUAL & UI SYSTEM
Warna identitas per timeframe
Mission card dengan border TF
Animasi visual:
TOUCHED (hit)
FAILED (fail)
📱 MOBILE FRIENDLY
Layout aman untuk HP
Tombol besar & jelas
Tidak ada hover-only action
🚫 FITUR YANG TIDAK ADA (SENGAJA)
❌ Auto trading
❌ Auto signal
❌ Real-time market feed
❌ AI decision engine
❌ Indikator teknikal
❌ Repaint logic
🧠 RINGKASAN SATU BARIS
BCA MONITOR = LPZ + Stacking Mission Audit Tool berbasis OHLC manual & logging, bukan signal generator.
Kalau mau, gue bisa:
Pecah list ini jadi CORE vs SUPPORT
Jadikan CHECKLIST USER 1 halaman
Buat versi teknis (developer-facing)
Tinggal bilang mau format yang mana.