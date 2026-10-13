<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KOPI DAKAS - Hotel Mangkuto</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Inter',sans-serif}
body{background:#f6f8fb;color:#0f172a;padding-top:62px}
header{position:fixed;top:0;left:0;right:0;height:62px;background:#1976ff;display:flex;align-items:center;justify-content:space-between;padding:0 14px;z-index:100;box-shadow:0 2px 10px rgba(0,0,0,.15)}
.left{display:flex;align-items:center;gap:10px}
.logo-box{background:#e11d26;width:52px;height:44px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-weight:900;color:white;font-size:10px;line-height:.9;text-align:center}
.brand{color:white;font-weight:800;font-size:22px;letter-spacing:.5px}.brand span{color:#ff3b3b}
.right{display:flex;align-items:center;gap:14px}
.cart-icon{position:relative;background:white;width:36px;height:32px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:18px}
.cart-badge{position:absolute;top:-8px;right:-8px;background:#e11d26;color:white;font-size:11px;font-weight:800;width:20px;height:20px;border-radius:50%;display:flex;align-items:center;justify-content:center}
.hamburger{width:28px;height:20px;display:flex;flex-direction:column;justify-content:space-between}.hamburger div{height:3px;background:white;border-radius:99px}
.container{max-width:480px;margin:0 auto;padding:12px}
.card{background:white;border-radius:18px;overflow:hidden;box-shadow:0 4px 18px rgba(0,0,0,.06);margin-bottom:18px;border:1px solid #eef2f7}
.card img{width:100%;height:320px;object-fit:cover;display:block}
.card-body{padding:16px 18px 18px}
.title{font-size:21px;font-weight:800}.desc{font-size:13px;color:#64748b;margin:6px 0 14px}.divider{border-top:1px dashed #e2e8f0;margin:10px 0}
.price-row{display:flex;justify-content:space-between;align-items:center;margin:10px 0 14px}.price-label{color:#64748b;font-size:13px}.price{font-size:21px;font-weight:800}
.btn{width:100%;border:none;border-radius:99px;padding:14px;font-weight:700;font-size:14px;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:6px;margin-bottom:10px}
.btn-blue{background:#1976ff;color:white}.btn-red{background:#e11d26;color:white}
.floating{position:fixed;bottom:18px;right:18px;display:flex;flex-direction:column;gap:12px;z-index:90}.float-btn{width:56px;height:56px;border-radius:50%;border:none;display:flex;align-items:center;justify-content:center;box-shadow:0 6px 18px rgba(0,0,0,.2);font-size:22px;cursor:pointer}.float-top{background:white}.float-wa{background:#25D366;color:white;font-size:28px}
.cart-drawer{position:fixed;bottom:0;left:50%;transform:translateX(-50%);width:100%;max-width:480px;background:white;border-radius:22px 22px 0 0;box-shadow:0 -10px 40px rgba(0,0,0,.15);padding:16px;z-index:101;max-height:80vh;overflow:auto;display:none}.cart-drawer.active{display:block}
.overlay{position:fixed;inset:0;background:rgba(0,0,0,.4);z-index:100;display:none}.overlay.active{display:block}
.cart-item{display:flex;justify-content:space-between;align-items:center;padding:10px 0;border-bottom:1px solid #f1f5f9;font-size:13px}
.checkout{margin-top:12px;background:#1976ff;color:white;border:none;width:100%;padding:14px;border-radius:99px;font-weight:800;font-size:15px}
</style>
</head>
<body>
<header>
<div class="left"><div class="logo-box">KOPI<br>DAKAS</div><div class="brand">KOPI <span>DAKAS</span></div></div>
<div class="right"><div class="cart-icon" onclick="toggleCart()">👜 <span class="cart-badge" id="badge">0</span></div><div class="hamburger"><div></div><div></div><div></div></div></div>
</header>
<div class="container" id="products"></div>
<div class="overlay" id="overlay" onclick="toggleCart()"></div>
<div class="cart-drawer" id="drawer">
<h3 style="font-weight:800;margin-bottom:10px">Keranjang (<span id="count2">0</span>)</h3>
<div id="cartList"><div style="color:#94a3b8;font-size:13px">Belum ada pesanan</div></div>
<div style="display:flex;justify-content:space-between;margin-top:12px;font-weight:800"><span>Total</span><span id="total">Rp 0</span></div>
<button class="checkout" onclick="checkoutWA()">Pesan via WhatsApp 083132891180</button>
</div>
<div class="floating">
<button class="float-btn float-top" onclick="window.scrollTo({top:0,behavior:'smooth'})">↑</button>
<button class="float-btn float-wa" onclick="openWA()">W</button>
</div>
<script>
const waNumber="6283132891180";
const products=[{id:1,name:"Kopi Susu Clasic",desc:"Double Shoot Espresso",price:12000,img:"https://images.unsplash.com/photo-1461023058943-07fcbe16d735?w=800"},{id:2,name:"Kopi Susu Strong",desc:"Balance Flavor",price:13000,img:"https://images.unsplash.com/photo-1485808191679-5f86510681a2?w=800"},{id:3,name:"Kopi Susu Soft",desc:"Sweet & Creamy",price:13000,img:"https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?w=800"},{id:4,name:"Coldbrew Peach",desc:"Fresh Peach Coldbrew",price:15000,img:"https://images.unsplash.com/photo-1517701604599-bb29b565090c?w=800"},{id:5,name:"Matcha",desc:"Premium Japanese Matcha",price:13000,img:"https://images.unsplash.com/photo-1576092768241-dec231879fc3?w=800"},{id:6,name:"Chocolate",desc:"Rich Chocolate",price:13000,img:"https://images.unsplash.com/photo-1544787219-7f47cc556762?w=800"},{id:7,name:"Kopi Dakas Literan 1L",desc:"Hemat Untuk Ramean",price:49000,img:"https://images.unsplash.com/photo-1551024709-8f23befc6f87?w=800"},{id:8,name:"Kopi Dakas Literan 2L",desc:"Paling Laris",price:95000,img:"https://images.unsplash.com/photo-1551024709-8f23befc6f87?w=800"}];
let cart=[];const container=document.getElementById('products');products.forEach(p=>{container.innerHTML+=`<div class="card"><img src="${p.img}"><div class="card-body"><div class="title">${p.name}</div><div class="desc">${p.desc}</div><div class="divider"></div><div class="price-row"><div class="price-label">Harga Pas</div><div class="price">Rp ${p.price.toLocaleString('id-ID')}</div></div><button class="btn btn-blue" onclick="beli(${p.id})">Beli Langsung</button><button class="btn btn-red" onclick="add(${p.id})">🛒 Masuk Keranjang</button></div></div>`;});
function add(id){const pr=products.find(x=>x.id===id);const f=cart.find(c=>c.id===id);if(f)f.qty++;else cart.push({...pr,qty:1});update();toggleCart(true);}
function beli(id){const pr=products.find(x=>x.id===id);const txt=`Halo Kopi Dakas Hotel Mangkuto%0A%0ASaya mau pesan:%0A- 1x ${pr.name} = Rp ${pr.price.toLocaleString('id-ID')}%0A%0A*Total: Rp ${pr.price.toLocaleString('id-ID')}*%0ANama: %0ALokasi: `;window.open(`https://wa.me/${waNumber}?text=${txt}`,'_blank');}
function update(){document.getElementById('badge').innerText=cart.reduce((a,b)=>a+b.qty,0);document.getElementById('count2').innerText=cart.reduce((a,b)=>a+b.qty,0);let tot=0;let html='';if(cart.length===0)html='<div style="color:#94a3b8;font-size:13px">Belum ada pesanan</div>';cart.forEach(c=>{tot+=c.price*c.qty;html+=`<div class="cart-item"><span>${c.qty}x ${c.name}</span><span>Rp ${(c.price*c.qty).toLocaleString('id-ID')} <b onclick="removeItem(${c.id})" style="color:#ef4444;cursor:pointer;margin-left:8px">✕</b></span></div>`});document.getElementById('cartList').innerHTML=html;document.getElementById('total').innerText='Rp '+tot.toLocaleString('id-ID');}
function removeItem(id){cart=cart.filter(x=>x.id!==id);update();}
function toggleCart(forceOpen){const d=document.getElementById('drawer');const o=document.getElementById('overlay');if(forceOpen===true){d.classList.add('active');o.classList.add('active');return;}d.classList.toggle('active');o.classList.toggle('active');}
function checkoutWA(){if(cart.length===0)return;let txt=`Halo Kopi Dakas Hotel Mangkuto%0A%0ASaya mau pesan:%0A`;let tot=0;cart.forEach(c=>{txt+=`- ${c.qty}x ${c.name} = Rp ${(c.price*c.qty).toLocaleString('id-ID')}%0A`;tot+=c.price*c.qty;});txt+=`%0A*Total: Rp ${tot.toLocaleString('id-ID')}*%0A%0ANama: %0ALokasi: `;window.open(`https://wa.me/${waNumber}?text=${txt}`,'_blank');}
function openWA(){window.open(`https://wa.me/${waNumber}?text=Halo%20Kopi%20Dakas%20Hotel%20Mangkuto,%20saya%20mau%20pesan`,'_blank');}
</script>
</body>
</html>
