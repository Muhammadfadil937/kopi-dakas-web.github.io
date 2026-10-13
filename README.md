<img width="1920" height="1280" alt="IMG-20261013-WA6826" src="https://github.com/user-attachments/assets/fcc83614-712b-4501-b879-c313a45a501b" />
<img width="1920" height="1280" alt="IMG-20261013-WA6826" src="https://github.com/user-attachments/assets/ad5d82b8-b889-4ff1-8613-79f4acffc41d" />
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KOPI DAKAS - Hotel Mangkuto</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@700;800&display=swap');
*{margin:0;padding:0;box-sizing:border-box;font-family:'Inter',sans-serif}
body{background:#f2f4f8;padding-top:56px}
header{position:fixed;top:0;left:0;right:0;height:56px;background:#1877F2;display:flex;align-items:center;justify-content:space-between;padding:0 14px;z-index:99}
.logo{width:58px;height:40px;background:#E11D26;border-radius:8px;display:flex;align-items:center;justify-content:center;color:white;font-weight:900;font-size:11px;line-height:.9;text-align:center}
.brand{color:white;font-weight:800;font-size:20px}.brand span{color:#FF2D2D}
.cart{background:white;width:38px;height:34px;border-radius:10px;display:flex;align-items:center;justify-content:center;position:relative}
.badge{position:absolute;top:-7px;right:-7px;background:#E11D26;color:white;font-size:11px;font-weight:800;width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center}
.wrap{max-width:480px;margin:0 auto;padding:14px}
.card{background:white;border-radius:20px;overflow:hidden;box-shadow:0 4px 16px rgba(0,0,0,.06);margin-bottom:16px}
.card img{width:100%;height:380px;object-fit:cover;background:white}
.info{padding:18px 20px}.t1{font-size:22px;font-weight:800}.t2{font-size:13px;color:#6B7280}
.line{border-top:1px dashed #E5E7EB;margin:14px 0}
.price-row{display:flex;justify-content:space-between}.price{font-size:22px;font-weight:800}
.btn{width:100%;border:none;border-radius:99px;padding:15px;font-weight:700;margin-top:12px;cursor:pointer}
.blue{background:#1877F2;color:white}.red{background:#E11D26;color:white}
.float{position:fixed;right:16px;bottom:18px;display:flex;flex-direction:column;gap:12px;z-index:90}
.circle{width:56px;height:56px;border-radius:50%;border:none;box-shadow:0 6px 18px rgba(0,0,0,.18);font-size:22px;background:white;cursor:pointer}
.wa{background:#25D366;color:white;font-weight:800;font-size:24px}
.drawer{position:fixed;bottom:0;left:50%;transform:translateX(-50%);width:100%;max-width:480px;background:white;border-radius:20px 20px 0 0;padding:16px;display:none;z-index:100;max-height:80vh;overflow:auto}
.drawer.on{display:block}.over{position:fixed;inset:0;background:rgba(0,0,0,.35);display:none;z-index:99}.over.on{display:block}
</style></head>
<body>
<header><div style="display:flex;gap:10px;align-items:center"><div class="logo">KOPI<br>DAKAS</div><div class="brand">KOPI <span>DAKAS</span></div></div><div class="cart" onclick="openCart()">👜<div class="badge" id="badge">0</div></div></header>
<div class="wrap" id="list"></div>
<div class="over" id="over" onclick="openCart()"></div>
<div class="dr<img width="3024" height="4032" alt="IMG-20261005-WA0009" src="https://github.com/user-attachments/assets/8702ecbe-a602-4b31-8d9a-59fae0202e69" />
<img width="720" height="1600" alt="Screenshot_2026_1013_133658" src="https://github.com/user-attachments/assets/635020f0-9481-48ce-8318-e52ca17534e7" />
awer" id="drawer"><h3 style="font-weight:800">Keranjang (<span id="c2">0</span>)</h3><div id="cartList" style="margin-top:10px"></div><div style="display:flex;justify-content:space-between;margin-top:12px;font-weight:800"><span>Total</span><span id="total">Rp 0</span></div><button class="btn blue" onclick="waAll()">Pesan via WA 083132891180</button></div>
<div class="float"><button class="circle" onclick="window.scrollTo({top:0,behavior:'smooth'})">↑</button><button class="circle wa" onclick="location.href='https://wa.me/6283132891180'">W</button></div>
<script>
const WA="6283132891180";const IMG="kopi-asli.jpg";
const prods=[{name:"Kopi Susu Clasic",desc:"Double Shoot Espresso",price:12000,img:IMG},{name:"Kopi Susu Strong",desc:"Balance Flavor",price:13000,img:IMG},{name:"Kopi Susu Soft",desc:"Sweet & Creamy",price:13000,img:IMG},{name:"Coldbrew Peach",desc:"Fresh Peach",price:15000,img:IMG},{name:"Matcha",desc:"Premium Matcha",price:13000,img:IMG},{name:"Chocolate",desc:"Rich Chocolate",price:13000,img:IMG},{name:"Literan 1L",desc:"Hemat Ramean",price:49000,img:IMG},{name:"Literan 2L",desc:"Paling Laris",price:95000,img:IMG}];
let cart=[];let list=document.getElementById('list');
prods.forEach((p,i)=>{list.innerHTML+=`<div class="card"><img src="${p.img}"><div class="info"><div class="t1">${p.name}</div><div class="t2">${p.desc}</div><div class="line"></div><div class="price-row"><span style="color:#6B7280;font-size:13px">Harga Pas</span><span class="price">Rp ${p.price.toLocaleString('id-ID')}</span></div><button class="btn blue" onclick="buy(${i})">Beli Langsung</button><button class="btn red" onclick="add(${i})">🛒 Masuk Keranjang</button></div></div>`});
function add(i){let f=cart.find(x=>x.i===i);if(f)f.qty++;else cart.push({i,qty:1});upd();openCart(true)}
function buy(i){let p=prods[i];window.open(`https://wa.me/${WA}?text=Halo Kopi Dakas%0ASaya pesan 1x ${p.name} Rp ${p.price}`,'_blank')}
function upd(){document.getElementById('badge').innerText=cart.reduce((a,b)=>a+b.qty,0);document.getElementById('c2').innerText=cart.reduce((a,b)=>a+b.qty,0);let tot=0;let h='';cart.forEach(c=>{let p=prods[c.i];tot+=p.price*c.qty;h+=`<div style="display:flex;justify-content:space-between;padding:8px 0;border-bottom:1px solid #eee;font-size:13px"><span>${c.qty}x ${p.name}</span><span>Rp ${(p.price*c.qty).toLocaleString('id-ID')}</span></div>`});document.getElementById('cartList').innerHTML=h||'Belum ada pesanan';document.getElementById('total').innerText='Rp '+tot.toLocaleString('id-ID')}
function openCart(f){let d=document.getElementById('drawer'),o=document.getElementById('over');if(f===true){d.classList.add('on');o.classList.add('on');return}d.classList.toggle('on');o.classList.toggle('on')}
function waAll(){let t=`Halo Kopi Dakas Hotel Mangkuto%0A`;let tot=0;cart.forEach(c=>{let p=prods[c.i];t+=`- ${c.qty}x ${p.name}%0A`;tot+=p.price*c.qty});t+=`Total Rp ${tot}`;window.open(`https://wa.me/${WA}?text=${t}`,'_blank')}
</script></body></html>
