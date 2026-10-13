<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KOPI DAKAS MANGKUTO 08.00-22.00</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@600;700;800&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Inter',sans-serif}
body{background:#f6f7fb}
header{position:sticky;top:0;z-index:99;background:#1e5bcf;color:white;height:60px;display:flex;align-items:center;justify-content:space-between;padding:0 16px}
.badge{position:absolute;top:-6px;right:-6px;background:#e11d26;color:white;font-size:10px;width:18px;height:18px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:800}
.banner{background:#dbeafe;color:#1e3a8a;padding:10px 16px;display:flex;justify-content:space-between;font-weight:700;font-size:13px;border-radius:0 0 16px 16px}
.wrap{max-width:480px;margin:0 auto;background:white;min-height:100vh}
.card-img{padding:16px}.card-img img{width:100%;border-radius:20px;background:white;height:380px;object-fit:contain}
.info{padding:0 18px 18px}
.title{font-size:22px;font-weight:800}.meta{color:#6b7280;font-size:13px;margin:8px 0;display:flex;gap:10px;align-items:center}
.price-label{color:#6b7280;font-size:13px;margin-top:10px}.price{font-size:32px;font-weight:800}
.desc{font-size:13px;color:#374151;margin-top:10px;line-height:1.5}
.btns{display:flex;gap:10px;margin-top:16px}
.btn{flex:1;border:none;border-radius:14px;padding:15px;font-weight:800;font-size:14px;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:6px}
.blue{background:#1877f2;color:white}.red{background:#e11d26;color:white}
.bottom{position:fixed;bottom:0;left:50%;transform:translateX(-50%);width:100%;max-width:480px;background:white;border-top:1px solid #e5e7eb;display:flex;justify-content:space-around;padding:8px 0}
.bottom div{font-size:11px;text-align:center;color:#6b7280}.bottom .active{color:#1877f2;font-weight:800}
.cart-drawer{position:fixed;bottom:70px;left:50%;transform:translateX(-50%);width:95%;max-width:460px;background:white;border-radius:20px;box-shadow:0 10px 40px rgba(0,0,0,.2);padding:16px;display:none;z-index:100}
.cart-drawer.on{display:block}
</style>
</head>
<body>
<div class="wrap">
<header>
<div style="display:flex;align-items:center;gap:12px"><span style="font-size:22px">☰</span><span style="font-weight:800;font-size:22px">KOPI DAKAS</span></div>
<div style="position:relative;background:white;width:36px;height:32px;border-radius:10px;display:flex;align-items:center;justify-content:center;color:#1e5bcf" onclick="openCart()">🛒<div class="badge" id="badge">0</div></div>
</header>
<div class="banner"><span>KOPI DAKAS MANGKUTO</span><span>🕒 Buka 08.00 - 22.00</span></div>

<div class="card-img"><img src="kopi-asli.jpg" alt="Kopi Dakas Mangkuto"></div>
<div class="info">
<div class="title">Kopi Dakas Mangkuto — Es Kopi Susu</div>
<div class="meta">⭐ 4.8 (1.2rb+ terjual) 📍 Mangkuto, Padang</div>
<div class="price-label">Harga Pas</div>
<div class="price">Rp 12.000</div>
<div class="desc">Es kopi susu khas Kopi Dakas Mangkuto. Paduan kopi robusta, susu segar, dan gula aren. Segar, manis pas, paling nemakan! <br><br><b>Yang Paling Memahami - IDUIK ISINYO BERJUANG TARUIH LAI NDAK PAHLAWAN WAK KO EH</b></div>
<div class="btns">
<button class="btn blue" onclick="buy()">👜 Beli Langsung</button>
<button class="btn red" onclick="add()">🛒 Masuk Keranjang</button>
</div>
<div style="text-align:center;font-size:11px;color:#6b7280;margin-top:16px">Pastikan alamat pengirimanmu sudah benar sebelum checkout<br>📍 Hotel Mangkuto • Buka 08.00-22.00 WIB • WA 083132891180</div>
</div>
</div>

<div class="cart-drawer" id="drawer">
<h3>Keranjang (<span id="c2">0</span>)</h3>
<div id="cartList" style="margin-top:10px"></div>
<div style="display:flex;justify-content:space-between;margin-top:12px;font-weight:800"><span>Total</span><span id="total">Rp 0</span></div>
<button class="btn blue" style="width:100%;margin-top:12px" onclick="waAll()">Pesan via WA 083132891180</button>
</div>

<div class="bottom">
<div class="active">🏠<br>Beranda</div><div>👜<br>Producto</div><div>📋<br>Pesanan</div><div>💬<br>Chat</div><div>👤<br>Akun</div>
</div>

<script>
const WA="6283132891180";let cart=[];
function add(){let f=cart.find(x=>x.name=="Es Kopi Susu");if(f)f.qty++;else cart.push({name:"Es Kopi Susu Clasic",price:12000,qty:1});upd();openCart(true)}
function buy(){window.open(`https://wa.me/${WA}?text=Halo Kopi Dakas Mangkuto 08.00-22.00%0ASaya pesan Es Kopi Susu Rp 12.000`,'_blank')}
function upd(){document.getElementById('badge').innerText=cart.reduce((a,b)=>a+b.qty,0);document.getElementById('c2').innerText=cart.reduce((a,b)=>a+b.qty,0);let tot=0;let h='';cart.forEach(c=>{tot+=c.price*c.qty;h+=`<div style="display:flex;justify-content:space-between;padding:8px 0;border-bottom:1px solid #eee;font-size:13px"><span>${c.qty}x ${c.name}</span><span>Rp ${(c.price*c.qty).toLocaleString('id-ID')}</span></div>`});document.getElementById('cartList').innerHTML=h||'Belum ada pesanan';document.getElementById('total').innerText='Rp '+tot.toLocaleString('id-ID')}
function openCart(f){document.getElementById('drawer').classList.toggle('on',f!==false?f:undefined)}
function waAll(){let t=`Halo Kopi Dakas Mangkuto 08.00-22.00%0A%0APesanan:%0A`;let tot=0;cart.forEach(c=>{t+=`- ${c.qty}x ${c.name} Rp ${(c.price*c.qty).toLocaleString('id-ID')}%0A`;tot+=c.price*c.qty});t+=`Total Rp ${tot}`;window.open(`https://wa.me/${WA}?text=${t}`,'_blank')}
</script>
</body>
</html>
