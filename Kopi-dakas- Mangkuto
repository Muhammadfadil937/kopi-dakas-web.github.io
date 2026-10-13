<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>KOPI DAKAS - YANG PALING MEMAHAMI</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:system-ui,sans-serif}
body{background:#f8fafc}
.header{background:#1e88e5;padding:12px 16px;display:flex;justify-content:space-between;align-items:center;color:#fff;position:sticky;top:0;z-index:10}
.logo{background:#ff1a1a;color:#fff;font-weight:900;padding:10px 18px;border-radius:16px;line-height:.9;font-size:18px}
.hero{padding:28px 16px 22px;text-align:center;background:#f8fafc}
.hero-box{background:#ff1a1a;color:#fff;padding:32px 20px;border-radius:28px;max-width:360px;margin:0 auto;font-weight:900;font-size:28px;line-height:1.1;box-shadow:0 0 0 5px #1e88e5}
.btn-blue{background:#1e88e5;color:#fff;border:0;padding:14px 36px;border-radius:28px;font-weight:800;font-size:16px;margin:20px auto 0;cursor:pointer}
.layanan{background:#1e88e5;color:#fff;padding:26px 16px;text-align:center;font-weight:900;font-size:21px}
.menu{padding:24px 12px 100px;max-width:440px;margin:0 auto}
.menu h2{text-align:center;font-weight:900;font-size:28px;margin-bottom:18px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.card{background:#fff;border-radius:18px;padding:14px 10px;text-align:center;box-shadow:0 4px 16px rgba(0,0,0,.06)}
.card img{width:100%;height:115px;object-fit:contain}
.card h3{font-size:13px;font-weight:800;margin:8px 0 4px;min-height:32px}
.price{color:#e53935;font-weight:900;font-size:16px;margin:4px 0}
.btn-pesan{background:#1e88e5;color:#fff;border:0;width:100%;padding:10px;border-radius:18px;font-weight:800;margin-top:8px;cursor:pointer}
.wa{position:fixed;bottom:16px;right:14px;background:#25d366;color:#fff;padding:12px 18px;border-radius:28px;font-weight:900;text-decoration:none;z-index:99}
</style>
</head>
<body>
<div class="header"><div class="logo">KOPI<br>DAKAS</div><div>🛒 Keranjang</div></div>
<div class="hero"><div class="hero-box">KOPI DAKAS<br>YANG PALING<br>MEMAHAMI</div><button class="btn-blue" onclick="document.getElementById('menu').scrollIntoView({behavior:'smooth'})">Lihat Menu</button></div>
<div class="layanan">Layanan Pengiriman &<br>Pengambilan</div>
<div class="menu" id="menu"><h2>MENU KOPI DAKAS</h2><div class="grid" id="grid"></div></div>
<a class="wa" href="https://wa.me/6283132891180?text=Halo%20KOPI%20DAKAS" target="_blank">💬 WA</a>
<script>
const WA="6283132891180";
const menu=[
{n:"Kopi Dakas Klasik",p:13000,f:"klasik_GAS.jpg",d:"Double Shot Espresso"},
{n:"Kopi Susu Soft",p:13000,f:"soft_GAS.jpg",d:"Balance Sweet"},
{n:"Kopi Susu Strong",p:13000,f:"strong_GAS.jpg",d:"Balance Flavor"},
{n:"Matcha",p:13000,f:"matcha_GAS.jpg",d:"Creamy Matcha"},
{n:"Coldbrew Peach",p:15000,f:"peach_GAS.jpg",d:"Segar Peach"},
{n:"Chocolate",p:13000,f:"coklat_GAS.jpg",d:"Rich Chocolate"},
{n:"Kopi Dakas Literan 1L",p:95000,f:"liter1_GAS.jpg",d:"1 Liter Botol"},
{n:"Kopi Dakas Literan 500mL",p:49000,f:"liter500_GAS.jpg",d:"500 mL Botol"}
];
document.getElementById('grid').innerHTML=menu.map(m=>`<div class="card"><img src="${m.f}"><h3>${m.n}</h3><div style="font-size:10px;color:#6b7a90">${m.d}</div><div class="price">Rp ${m.p.toLocaleString('id-ID')}</div><button class="btn-pesan" onclick="window.open('https://wa.me/'+WA+'?text=Halo%20KOPI%20DAKAS%20DEPAN%20HOTEL%20MANGKUTO%20mau%20pesan%20'+encodeURIComponent(m.n),'_blank')">Pesan WA</button></div>`).join('');
</script>
</body>
</html>
