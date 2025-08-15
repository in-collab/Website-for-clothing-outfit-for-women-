# Website-for-clothing-outfit-for-women-
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Tripti — Ladies Clothing Boutique</title>
  <meta name="description" content="Tripti: Exclusive ladies clothing & outfits. Shop sarees, kurtis, dresses, and more." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --primary:#ff6f61;   /* coral */
      --accent:#ffb6b9;    /* soft pink */
      --bg:#fff8f5;        /* blush */
      --ink:#2f2a2a;       /* text */
      --muted:#7a6f6f;     /* secondary text */
      --card:#ffffff;      /* card bg */
      --ring: rgba(255,111,97,.35);
      --radius: 16px;
      --shadow: 0 10px 30px rgba(0,0,0,.08);
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;font-family:Poppins,system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif;color:var(--ink);background:var(--bg)}
    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}
    .container{width:clamp(300px,92vw,1200px);margin-inline:auto}/* Header */
header{
  position:sticky;top:0;z-index:50;background:rgba(255,255,255,.7);backdrop-filter: saturate(140%) blur(8px);
  border-bottom:1px solid #f1e7e5
}
.nav{display:flex;align-items:center;justify-content:space-between;padding:14px 10px}
.brand{display:flex;align-items:center;gap:10px}
.logo{width:38px;height:38px;border-radius:50%;background:linear-gradient(135deg,var(--primary),#ff8a80);display:grid;place-items:center;color:white;font-weight:700;box-shadow:var(--shadow)}
.brand h1{font-size:1.25rem;margin:0}
.navlinks{display:flex;gap:18px;align-items:center}
.navlinks a{padding:8px 12px;border-radius:999px}
.navlinks a:hover{background:var(--accent);color:#222}
.cart-button{position:relative;padding:10px 14px;border-radius:999px;background:var(--primary);color:white;font-weight:600;border:none;cursor:pointer;box-shadow:var(--shadow)}
.cart-count{position:absolute;top:-8px;right:-8px;background:#222;color:#fff;border-radius:999px;font-size:.7rem;padding:2px 6px}

/* Hero */
.hero{position:relative;isolation:isolate}
.hero .wrap{display:grid;grid-template-columns:1.1fr .9fr;gap:24px;align-items:center;padding:48px 10px}
.hero h2{font-size:clamp(1.6rem,4.2vw,2.8rem);line-height:1.15;margin:0 0 10px}
.hero p{color:var(--muted);margin:0 0 18px}
.hero .cta{display:flex;gap:12px;flex-wrap:wrap}
.btn{padding:12px 18px;border-radius:12px;border:2px solid transparent;font-weight:600;cursor:pointer;box-shadow:var(--shadow)}
.btn.primary{background:var(--primary);color:#fff}
.btn.ghost{background:#fff;border-color:#ffe0dc}
.hero-card{background:var(--card);border-radius:var(--radius);overflow:hidden;box-shadow:var(--shadow)}
.hero-card img{aspect-ratio:4/3;object-fit:cover}

/* Controls */
.controls{display:flex;gap:12px;flex-wrap:wrap;align-items:center;justify-content:space-between;margin:24px 0}
.search{flex:1;min-width:240px;display:flex;align-items:center;gap:10px;background:#fff;border-radius:999px;padding:10px 14px;border:1px solid #f0d8d5}
.search input{flex:1;border:none;outline:none;font-size:.95rem}
.select{background:#fff;border-radius:999px;border:1px solid #f0d8d5;padding:10px 14px}

/* Grid */
.grid{display:grid;grid-template-columns:repeat(12,1fr);gap:18px}
.product{grid-column:span 3;background:var(--card);border-radius:var(--radius);box-shadow:var(--shadow);overflow:hidden;display:flex;flex-direction:column}
.product img{aspect-ratio:3/4;object-fit:cover}
.pill{position:absolute;top:10px;left:10px;background:#fff;padding:6px 10px;border-radius:999px;font-size:.78rem;box-shadow:var(--shadow)}
.p-body{padding:12px 14px;display:grid;gap:8px}
.title{font-weight:600}
.price-row{display:flex;align-items:center;gap:10px}
.price{font-weight:700}
.strike{text-decoration:line-through;color:var(--muted);font-size:.9rem}
.rating{font-size:.85rem;color:#c07d00}
.p-actions{margin-top:auto;display:flex;gap:8px}
.qty{display:flex;align-items:center;gap:8px;border:1px solid #f0d8d5;border-radius:999px;padding:6px 10px}
.qty button{border:none;background:transparent;font-size:1.1rem;cursor:pointer}
.add{flex:1}

/* Sections */
section{padding:24px 10px}
h3.section-title{margin:0 0 12px;font-size:1.2rem}

/* Cart drawer */
.drawer{position:fixed;inset:0 0 0 auto;max-width:420px;width:100%;background:#fff;box-shadow:-20px 0 50px rgba(0,0,0,.15);transform:translateX(100%);transition:transform .35s ease;z-index:60;display:flex;flex-direction:column}
.drawer.open{transform:translateX(0)}
.drawer header{position:initial;background:#fff;border-bottom:1px solid #f3e2df}
.drawer .items{flex:1;overflow:auto;padding:12px}
.cart-item{display:grid;grid-template-columns:64px 1fr auto;gap:10px;align-items:center;padding:10px;border-radius:12px;border:1px solid #f3e2df;margin-bottom:8px}
.cart-item img{width:64px;height:80px;object-fit:cover;border-radius:8px}
.cart-footer{border-top:1px solid #f3e2df;padding:12px;display:grid;gap:10px}
.totals{display:flex;justify-content:space-between}
.empty{color:var(--muted);text-align:center;padding:24px}

/* About & Contact */
.about,.contact{background:linear-gradient(180deg,#fff, #fff7f5)}
.cards{display:grid;grid-template-columns:repeat(12,1fr);gap:16px}
.card{grid-column:span 4;background:#fff;border-radius:var(--radius);padding:18px;box-shadow:var(--shadow)}
.contact form{display:grid;gap:10px;max-width:560px}
.input{padding:12px 14px;border-radius:12px;border:1px solid #f0d8d5;width:100%}
.input:focus{outline:none;box-shadow:0 0 0 4px var(--ring)}

footer{background:#fff;border-top:1px solid #f3e2df;padding:20px 10px;color:var(--muted);font-size:.9rem}

/* Badges */
.badge{background:#111;color:#fff;border-radius:8px;padding:2px 8px;font-size:.72rem}

/* Responsive */
@media (max-width: 1100px){.product{grid-column:span 4}}
@media (max-width: 800px){
  .hero .wrap{grid-template-columns:1fr}
  .product{grid-column:span 6}
  .navlinks{display:none}
}
@media (max-width: 560px){.product{grid-column:span 12}}

  </style>
</head>
<body>
  <!-- Top Nav -->
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo">T</div>
        <h1>Tripti</h1>
      </div>
      <nav class="navlinks">
        <a href="#home">Home</a>
        <a href="#shop">Shop</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </nav>
      <button class="cart-button" id="openCart">🛍️ Cart <span class="cart-count" id="cartCount">0</span></button>
    </div>
  </header>  <!-- Hero -->  <section id="home" class="hero">
    <div class="container wrap">
      <div>
        <span class="badge">NEW • Festive '25</span>
        <h2>Fashion that speaks for you. Curated looks for every mood ✨</h2>
        <p>Discover sarees, kurtis, dresses, and co-ords crafted for comfort and style. Free shipping over ₹1,999.</p>
        <div class="cta">
          <a href="#shop" class="btn primary">Shop Collection</a>
          <a href="#about" class="btn ghost">Why Tripti?</a>
        </div>
      </div>
      <div class="hero-card">
        <img alt="Tripti outfits" src="https://images.unsplash.com/photo-1520975682049-8194a1d96f52?q=80&w=1200&auto=format&fit=crop"/>
      </div>
    </div>
  </section>  <!-- Shop -->  <section id="shop">
    <div class="container">
      <h3 class="section-title">Shop the Collection</h3><!-- Controls -->
  <div class="controls">
    <div class="search">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M21 21l-3.5-3.5" stroke="#555" stroke-width="2" stroke-linecap="round"/><circle cx="11" cy="11" r="7" stroke="#555" stroke-width="2"/></svg>
      <input id="search" type="search" placeholder="Search: saree, kurti, dress..." />
    </div>
    <select id="category" class="select">
      <option value="all">All Categories</option>
      <option value="Saree">Saree</option>
      <option value="Kurti">Kurti</option>
      <option value="Dress">Dress</option>
      <option value="Co-ord Set">Co-ord Set</option>
      <option value="Ethnic Set">Ethnic Set</option>
    </select>
    <select id="sort" class="select">
      <option value="featured">Sort: Featured</option>
      <option value="price-asc">Price: Low to High</option>
      <option value="price-desc">Price: High to Low</option>
      <option value="rating">Customer Rating</option>
      <option value="new">Newest</option>
    </select>
  </div>

  <!-- Grid -->
  <div id="grid" class="grid"></div>
</div>

  </section>  <!-- About -->  <section id="about" class="about">
    <div class="container">
      <h3 class="section-title">Why Tripti?</h3>
      <div class="cards">
        <div class="card"><h4>Quality Fabrics</h4><p>Soft, breathable and durable textiles chosen for Indian weather. No compromise on comfort.</p></div>
        <div class="card"><h4>Made with Love</h4><p>Designed by women, for women. Each piece is inspected by our in-house team.</p></div>
        <div class="card"><h4>Easy Exchanges</h4><p>7-day return or size exchange for eligible products. Hassle-free support.</p></div>
      </div>
    </div>
  </section>  <!-- Contact -->  <section id="contact" class="contact">
    <div class="container">
      <h3 class="section-title">Contact Us</h3>
      <p>Have a question or bulk order inquiry? We’d love to hear from you.</p>
      <form id="contactForm">
        <input class="input" type="text" id="name" placeholder="Your name" required>
        <input class="input" type="email" id="email" placeholder="Your email" required>
        <textarea class="input" id="message" rows="4" placeholder="Your message" required></textarea>
        <button type="submit" class="btn primary" style="width:max-content">Send Message</button>
        <p style="color:var(--muted);font-size:.95rem">Or email us at <a href="mailto:tripudubey@gmail.com">tripudubey@gmail.com</a></p>
      </form>
    </div>
  </section>  <footer>
    <div class="container" style="display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap">
      <span>© 2025 Tripti. All rights reserved.</span>
      <span>Made with ❤ in India</span>
    </div>
  </footer>  <!-- Cart Drawer -->  <aside id="cartDrawer" class="drawer" aria-hidden="true">
    <header>
      <div class="container nav">
        <div class="brand"><div class="logo">T</div><h1>Cart</h1></div>
        <button class="btn ghost" id="closeCart">Close</button>
      </div>
    </header>
    <div class="items" id="cartItems"></div>
    <div class="cart-footer">
      <div class="totals"><strong>Subtotal</strong><strong id="subtotal">₹0</strong></div>
      <button id="checkout" class="btn primary">Checkout</button>
      <small style="color:var(--muted)">Demo checkout only. Add your payment gateway later.</small>
    </div>
  </aside>  <script>
    // ------ Demo Product Data (edit freely) ------
    const products = [
      {id:1, title:"Floral Summer Dress", category:"Dress", price:1499, mrp:1999, rating:4.6, created:"2025-07-10", img:"https://images.unsplash.com/photo-1520975682049-8194a1d96f52?q=80&w=900&auto=format&fit=crop"},
      {id:2, title:"Classic Cotton Kurti", category:"Kurti", price:999, mrp:1299, rating:4.4, created:"2025-06-20", img:"https://images.unsplash.com/photo-1496747611176-843222e1e57c?q=80&w=900&auto=format&fit=crop"},
      {id:3, title:"Elegant Party Saree", category:"Saree", price:2799, mrp:3499, rating:4.8, created:"2025-08-01", img:"https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?q=80&w=900&auto=format&fit=crop"},
      {id:4, title:"Linen Co-ord Set", category:"Co-ord Set", price:2199, mrp:2599, rating:4.5, created:"2025-07-28", img:"https://images.unsplash.com/photo-1544441893-675973e31985?q=80&w=900&auto=format&fit=crop"},
      {id:5, title:"Festive Ethnic Set", category:"Ethnic Set", price:2499, mrp:3199, rating:4.7, created:"2025-08-10", img:"https://images.unsplash.com/photo-1503341455253-b2e723bb3dbb?q=80&w=900&auto=format&fit=crop"},
      {id:6, title:"Everyday Rayon Kurti", category:"Kurti", price:899, mrp:1199, rating:4.3, created:"2025-05-22", img:"https://images.unsplash.com/photo-1490481651871-ab68de25d43d?q=80&w=900&auto=format&fit=crop"},
      {id:7, title:"Chiffon Printed Saree", category:"Saree", price:1599, mrp:2199, rating:4.2, created:"2025-04-11", img:"https://images.unsplash.com/photo-1520975722975-29d08ab9b0d4?q=80&w=900&auto=format&fit=crop"},
      {id:8, title:"Boho Maxi Dress", category:"Dress", price:1799, mrp:2299, rating:4.5, created:"2025-07-05", img:"https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=900&auto=format&fit=crop"},
      {id:9, title:"Silk Blend Saree", category:"Saree", price:3299, mrp:3999, rating:4.9, created:"2025-08-12", img:"https://images.unsplash.com/photo-1520975693411-b4e2300bdc31?q=80&w=900&auto=format&fit=crop"},
      {id:10, title:"Casual Co-ord Set", category:"Co-ord Set", price:1899, mrp:2399, rating:4.1, created:"2025-06-02", img:"https://images.unsplash.com/photo-1520975738534-a92f1f4c30ce?q=80&w=900&auto=format&fit=crop"},
      {id:11, title:"Embroidered Kurti", category:"Kurti", price:1299, mrp:1699, rating:4.6, created:"2025-08-08", img:"https://images.unsplash.com/photo-1441986300917-64674bd600d8?q=80&w=900&auto=format&fit=crop"},
      {id:12, title:"A-Line Day Dress", category:"Dress", price:1399, mrp:1799, rating:4.0, created:"2025-03-18", img:"https://images.unsplash.com/photo-1512436991641-6745cdb1723f?q=80&w=900&auto=format&fit=crop"}
    ];

    // ------ State ------
    const state = {
      query: '',
      category: 'all',
      sort: 'featured',
      cart: JSON.parse(localStorage.getItem('tripti_cart')||'{}') // {id: qty}
    };

    // ------ Helpers ------
    const fmtINR = n => '₹' + n.toLocaleString('en-IN');
    const $(id) = document.getElementById.bind(document);

    function saveCart(){localStorage.setItem('tripti_cart', JSON.stringify(state.cart));renderCart();updateCartCount();}

    function filtered(){
      let list = products.filter(p=>{
        const q = state.query.toLowerCase();
        const matchQuery = p.title.toLowerCase().includes(q) || p.category.toLowerCase().includes(q);
        const matchCategory = state.category==='all' || p.category===state.category;
        return matchQuery && matchCategory;
      });
      switch(state.sort){
        case 'price-asc': list.sort((a,b)=>a.price-b.price); break;
        case 'price-desc': list.sort((a,b)=>b.price-a.price); break;
        case 'rating': list.sort((a,b)=>b.rating-a.rating); break;
        case 'new': list.sort((a,b)=> new Date(b.created)-new Date(a.created)); break;
        default: list.sort((a,b)=>b.rating*10 + (new Date(b.created)-new Date(a.created)) - (a.rating*10));
      }
      return list;
    }

    // ------ Render Products ------
    function renderGrid(){
      const grid = $('grid');
      const list = filtered();
      grid.innerHTML = list.map(p=>{
        const off = Math.max(0, Math.round((1 - p.price/p.mrp)*100));
        return `
          <article class="product">
            <div style="position:relative">
              ${off>0?`<span class="pill">${off}% OFF</span>`:''}
              <img src="${p.img}" alt="${p.title}">
            </div>
            <div class="p-body">
              <div class="title">${p.title}</div>
              <div class="rating">★ ${p.rating.toFixed(1)}</div>
              <div class="price-row">
                <div class="price">${fmtINR(p.price)}</div>
                <div class="strike">${fmtINR(p.mrp)}</div>
              </div>
              <div class="p-actions">
                <div class="qty" data-id="${p.id}">
                  <button class="dec" aria-label="Decrease">−</button>
                  <span class="q">1</span>
                  <button class="inc" aria-label="Increase">＋</button>
                </div>
                <button class="btn primary add" data-id="${p.id}">Add to Cart</button>
              </div>
            </div>
          </article>`
      }).join('');

      // qty controls per card
      grid.querySelectorAll('.qty').forEach(box=>{
        let q=1; const span=box.querySelector('.q');
        box.addEventListener('click',e=>{
          if(e.target.classList.contains('inc')){q++;span.textContent=q}
          if(e.target.classList.contains('dec')){q=Math.max(1,q-1);span.textContent=q}
        });
      });

      // add to cart buttons
      grid.querySelectorAll('.add').forEach(btn=>{
        btn.addEventListener('click',()=>{
          const id = +btn.dataset.id;
          const qty = +btn.closest('.p-body').querySelector('.q').textContent;
          state.cart[id] = (state.cart[id]||0) + qty;
          saveCart();
          openDrawer();
        });
      });
    }

    // ------ Cart ------
    function cartItems(){
      return Object.entries(state.cart).map(([id,qty])=>{
        const p = products.find(x=>x.id==id);
        return {...p, qty}
      });
    }

    function cartSubtotal(){
      return cartItems().reduce((s,i)=> s + i.price*i.qty, 0);
    }

    function renderCart(){
      const wrap = $('cartItems');
      const items = cartItems();
      if(items.length===0){wrap.innerHTML = `<div class="empty">Your cart is empty. Let\'s add some styles!</div>`; $('subtotal').textContent = fmtINR(0); return}
      wrap.innerHTML = items.map(i=>`
        <div class="cart-item">
          <img src="${i.img}" alt="${i.title}">
          <div>
            <div style="font-weight:600">${i.title}</div>
            <div style="color:var(--muted)">${i.category}</div>
            <div class="price-row"><div class="price">${fmtINR(i.price)}</div></div>
            <div class="qty" data-id="${i.id}" style="width:max-content;margin-top:6px">
              <button class="dec">−</button><span class="q">${i.qty}</span><button class="inc">＋</button>
            </div>
          </div>
          <button class="btn ghost rm" data-id="${i.id}">Remove</button>
        </div>`).join('');

      $('subtotal').textContent = fmtINR(cartSubtotal());

      // qty & remove handlers
      wrap.querySelectorAll('.qty').forEach(box=>{
        const id= +box.dataset.id; const span=box.querySelector('.q');
        box.addEventListener('click',e=>{
          if(e.target.classList.contains('inc')){state.cart[id]=(state.cart[id]||0)+1; span.textContent=state.cart[id]; saveCart();}
          if(e.target.classList.contains('dec')){state.cart[id]=Math.max(1,(state.cart[id]||1)-1); span.textContent=state.cart[id]; saveCart();}
        });
      });
      wrap.querySelectorAll('.rm').forEach(btn=>btn.addEventListener('click',()=>{delete state.cart[+btn.dataset.id]; saveCart(); renderCart();}));
    }

    function updateCartCount(){
      const n = Object.values(state.cart).reduce((s,v)=>s+v,0);
      $('cartCount').textContent = n;
    }

    // ------ Drawer ------
    const drawer = $('cartDrawer');
    function openDrawer(){drawer.classList.add('open'); drawer.setAttribute('aria-hidden','false');}
    function closeDrawer(){drawer.classList.remove('open'); drawer.setAttribute('aria-hidden','true');}

    // ------ Contact Form (demo) ------
    $('contactForm').addEventListener('submit', (e)=>{
      e.preventDefault();
      const data = {
        name: $('name').value.trim(),
        email: $('email').value.trim(),
        message: $('message').value.trim()
      };
      alert(`Thanks ${data.name}! We\'ll reach you at ${data.email}.`);
      e.target.reset();
    });

    // ------ Events ------
    $('search').addEventListener('input', (e)=>{state.query=e.target.value; renderGrid();});
    $('category').addEventListener('change', (e)=>{state.category=e.target.value; renderGrid();});
    $('sort').addEventListener('change', (e)=>{state.sort=e.target.value; renderGrid()
