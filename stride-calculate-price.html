<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>STRIDE. — Set Logic Sneaker Drop</title>
<style>
  :root{
    --bg:#0f0f10;
    --card:#19191b;
    --line:#2a2a2d;
    --ink:#f3f2ee;
    --sub:#9a9a9f;
    --accent:#e8ff5b;
    --accent-ink:#0f0f10;
  }
  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:'Segoe UI', system-ui, sans-serif;
  }
  header{
    display:flex;justify-content:space-between;align-items:center;
    padding:20px 28px;border-bottom:1px solid var(--line);
    position:sticky;top:0;background:var(--bg);z-index:10;
  }
  .logo{font-weight:800;letter-spacing:2px;font-size:20px;}
  nav{display:flex;gap:18px;flex-wrap:wrap;}
  nav button{
    background:none;border:1px solid var(--line);color:var(--sub);
    padding:6px 14px;border-radius:999px;cursor:pointer;font-size:13px;
  }
  nav button.active{background:var(--accent);color:var(--accent-ink);border-color:var(--accent);font-weight:700;}
  .cart{border:1px solid var(--line);border-radius:999px;padding:6px 14px;font-size:14px;}

  main{max-width:1000px;margin:0 auto;padding:32px 24px 80px;}
  h1{font-size:28px;margin:0 0 6px;}
  .desc{color:var(--sub);font-size:14px;max-width:640px;line-height:1.6;margin-bottom:24px;}

  .set-filters{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:28px;}
  .set-filters button{
    background:var(--card);border:1px solid var(--line);color:var(--ink);
    padding:8px 16px;border-radius:10px;cursor:pointer;font-size:13px;
  }
  .set-filters button.active{border-color:var(--accent);color:var(--accent);}

  .grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px;margin-bottom:36px;}
  .product{
    background:var(--card);border:1px solid var(--line);border-radius:14px;
    padding:16px;display:flex;flex-direction:column;gap:8px;position:relative;
  }
  .product .badge{position:absolute;top:12px;right:12px;font-size:11px;color:var(--sub);}
  .product h3{margin:0;font-size:15px;}
  .product .price{font-size:18px;font-weight:700;color:var(--accent);}
  .product label{display:flex;align-items:center;gap:8px;font-size:13px;color:var(--sub);cursor:pointer;}

  .checkout{
    background:var(--card);border:1px solid var(--line);border-radius:16px;
    padding:24px;display:flex;justify-content:space-between;align-items:center;gap:20px;flex-wrap:wrap;
  }
  .checkout .total-label{color:var(--sub);font-size:13px;}
  .checkout .total{font-size:28px;font-weight:800;}
  #calcBtn{
    background:var(--accent);color:var(--accent-ink);border:none;
    padding:14px 28px;border-radius:10px;font-weight:700;font-size:15px;
    cursor:pointer;
  }
  #calcBtn:active{transform:scale(0.98);}
  #orderBtn{
    background:transparent;color:var(--ink);border:1px solid var(--accent);
    padding:14px 28px;border-radius:10px;font-weight:700;font-size:15px;
    cursor:pointer;margin-left:10px;
  }
  #orderBtn:hover{background:rgba(232,255,91,0.08);}
  #orderBtn:disabled{opacity:0.4;cursor:not-allowed;}
  #orderBtn:active{transform:scale(0.98);}
</style>
</head>
<body>

<header>
  <div class="logo">STRIDE.</div>
  <nav id="categoryNav">
    <button class="active" data-cat="ทั้งหมด">ทั้งหมด</button>
    <button data-cat="วิ่ง">วิ่ง</button>
    <button data-cat="ลำลอง">ลำลอง</button>
    <button data-cat="บาสเก็ตบอล">บาสเก็ตบอล</button>
    <button data-cat="รองเท้าแตะ">รองเท้าแตะ</button>
  </nav>
  <div class="cart">🛒 <span id="cartCount">0</span></div>
</header>

<main>
  <h1>รองเท้าทุกคู่ คือสมาชิกของเซต</h1>
  <p class="desc">
    เลือกสินค้าที่ต้องการด้วยการติ๊กช่อง แล้วกด "คำนวณราคา" เพื่อรวมยอดของสินค้าที่เลือกทั้งหมด
    (เซต A = ลดราคา, เซต B = สินค้าแนะนำ)
  </p>

  <div class="set-filters" id="setFilters">
    <button class="active" data-set="all">ทั้งหมด</button>
    <button data-set="A">A (ลดราคา)</button>
    <button data-set="B">B (แนะนำ)</button>
    <button data-set="union">A ∪ B</button>
    <button data-set="inter">A ∩ B</button>
    <button data-set="Aonly">A − B</button>
    <button data-set="Bonly">B − A</button>
  </div>

  <div class="grid" id="productGrid"></div>

  <div class="checkout">
    <div>
      <div class="total-label">ยอดรวมสินค้าที่เลือก</div>
      <div class="total" id="totalDisplay">฿0</div>
    </div>
    <button id="calcBtn">คำนวณราคา</button>
    <button id="orderBtn">สั่งซื้อ</button>
  </div>

  <div id="orderMsg" style="margin-top:16px;font-size:14px;color:var(--accent);display:none;"></div>
</main>

<script>
  // ---- ตัวอย่างข้อมูลสินค้า (แก้ไข/แทนที่ด้วยข้อมูลจริงของคุณได้เลย) ----
  const products = [
    { id: 1, name: "Aero Runner",     price: 2590, category: "วิ่ง",         inA:true,  inB:false },
    { id: 2, name: "Cloud Walk",      price: 1890, category: "ลำลอง",       inA:false, inB:true  },
    { id: 3, name: "Court King",      price: 3290, category: "บาสเก็ตบอล", inA:true,  inB:true  },
    { id: 4, name: "Beach Slide",     price: 690,  category: "รองเท้าแตะ",  inA:false, inB:false },
    { id: 5, name: "Sprint Pro",      price: 2990, category: "วิ่ง",         inA:true,  inB:true  },
    { id: 6, name: "Street Ease",     price: 1590, category: "ลำลอง",       inA:true,  inB:false },
    { id: 7, name: "Dunk Flex",       price: 3590, category: "บาสเก็ตบอล", inA:false, inB:true  },
    { id: 8, name: "Trail Comfort",   price: 2190, category: "วิ่ง",         inA:false, inB:false },
  ];

  const grid = document.getElementById("productGrid");
  const cartCount = document.getElementById("cartCount");
  const totalDisplay = document.getElementById("totalDisplay");
  const calcBtn = document.getElementById("calcBtn");

  let activeCategory = "ทั้งหมด";
  let activeSet = "all";
  const selected = new Set(); // เก็บ id สินค้าที่ถูกติ๊กเลือก (ตะกร้า)

  function inSet(p, setKey) {
    switch (setKey) {
      case "A": return p.inA;
      case "B": return p.inB;
      case "union": return p.inA || p.inB;
      case "inter": return p.inA && p.inB;
      case "Aonly": return p.inA && !p.inB;
      case "Bonly": return p.inB && !p.inA;
      default: return true;
    }
  }

  function render() {
    grid.innerHTML = "";
    const visible = products.filter(p =>
      (activeCategory === "ทั้งหมด" || p.category === activeCategory) &&
      inSet(p, activeSet)
    );

    visible.forEach(p => {
      const card = document.createElement("div");
      card.className = "product";
      card.innerHTML = `
        <span class="badge">${p.inA ? "A " : ""}${p.inB ? "B" : ""}</span>
        <h3>${p.name}</h3>
        <div class="price">฿${p.price.toLocaleString()}</div>
        <label>
          <input type="checkbox" data-id="${p.id}" ${selected.has(p.id) ? "checked" : ""}>
          เพิ่มลงตะกร้า
        </label>
      `;
      grid.appendChild(card);
    });

    grid.querySelectorAll('input[type="checkbox"]').forEach(cb => {
      cb.addEventListener("change", (e) => {
        const id = Number(e.target.dataset.id);
        if (e.target.checked) selected.add(id);
        else selected.delete(id);
        cartCount.textContent = selected.size;
      });
    });
  }

  // ---- ปุ่ม "คำนวณราคา": รวมราคาสินค้าทุกชิ้นที่อยู่ในตะกร้า (selected) ----
  function calculatePrice() {
    let total = 0;
    selected.forEach(id => {
      const item = products.find(p => p.id === id);
      if (item) total += item.price;
    });
    totalDisplay.textContent = "฿" + total.toLocaleString();
  }
  calcBtn.addEventListener("click", calculatePrice);

  // ---- ปุ่ม "สั่งซื้อ": ยืนยันคำสั่งซื้อจากสินค้าที่อยู่ในตะกร้า ----
  const orderBtn = document.getElementById("orderBtn");
  const orderMsg = document.getElementById("orderMsg");

  orderBtn.addEventListener("click", () => {
    if (selected.size === 0) {
      orderMsg.style.color = "#ff6b6b";
      orderMsg.textContent = "กรุณาเลือกสินค้าอย่างน้อย 1 ชิ้นก่อนสั่งซื้อ";
      orderMsg.style.display = "block";
      return;
    }

    let total = 0;
    selected.forEach(id => {
      const item = products.find(p => p.id === id);
      if (item) total += item.price;
    });

    orderMsg.style.color = "var(--accent)";
    orderMsg.textContent = `สั่งซื้อสำเร็จ! ${selected.size} รายการ รวม ฿${total.toLocaleString()} — ขอบคุณที่อุดหนุน STRIDE.`;
    orderMsg.style.display = "block";

    // เคลียร์ตะกร้าหลังสั่งซื้อ
    selected.clear();
    cartCount.textContent = "0";
    totalDisplay.textContent = "฿0";
    render();
  });

  // หมวดหมู่
  document.getElementById("categoryNav").addEventListener("click", (e) => {
    if (e.target.tagName !== "BUTTON") return;
    document.querySelectorAll("#categoryNav button").forEach(b => b.classList.remove("active"));
    e.target.classList.add("active");
    activeCategory = e.target.dataset.cat;
    render();
  });

  // เซต A/B
  document.getElementById("setFilters").addEventListener("click", (e) => {
    if (e.target.tagName !== "BUTTON") return;
    document.querySelectorAll("#setFilters button").forEach(b => b.classList.remove("active"));
    e.target.classList.add("active");
    activeSet = e.target.dataset.set;
    render();
  });

  render();
</script>

</body>
</html>
