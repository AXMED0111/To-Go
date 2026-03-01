# To-Go[Uploading somali-store-firebase.html…]()
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Somali Store</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Syne:wght@700;800&display=swap" rel="stylesheet">

    <!-- ✅ FIREBASE SDK -->
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";
        import {
            getFirestore, collection, doc, getDocs, setDoc, deleteDoc,
            onSnapshot, query, orderBy
        } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-firestore.js";

        // ============================================================
        // 🔥 PASTE YOUR FIREBASE CONFIG HERE
        // Go to Firebase Console → Project Settings → Your Apps → Web
        // ============================================================
        const firebaseConfig = {
             apiKey: "AIzaSyDlXVPPuZgIizz0daPFGK80H_rPAcHhqZk",
             authDomain: "to-go-so.firebaseapp.com",
             projectId: "to-go-so",
             storageBucket: "to-go-so.firebasestorage.app",
             messagingSenderId: "314570632893",
             appId: "1:314570632893:web:3b28085ad8c1a8754fd1d4",
             measurementId: "G-2RZV6FJVF6"
        };
            
        // ============================================================

        const app = initializeApp(firebaseConfig);
        const db  = getFirestore(app);

        // ---- Expose helpers to window so rest of script can use them ----
        window.FB = {
            // Products
            async getProducts() {
                const snap = await getDocs(collection(db, "products"));
                return snap.docs.map(d => ({ id: d.id, ...d.data() }));
            },
            async saveProduct(product) {
                const id = String(product.id || Date.now());
                await setDoc(doc(db, "products", id), { ...product, id });
                return id;
            },
            async deleteProduct(id) {
                await deleteDoc(doc(db, "products", String(id)));
            },
            // Settings
            async getSettings() {
                const snap = await getDocs(collection(db, "settings"));
                const result = {};
                snap.docs.forEach(d => { result[d.id] = d.data(); });
                return result;
            },
            async saveSetting(key, value) {
                await setDoc(doc(db, "settings", key), { value });
            },
            // Real-time product listener
            listenProducts(callback) {
                return onSnapshot(collection(db, "products"), snap => {
                    callback(snap.docs.map(d => ({ id: d.id, ...d.data() })));
                });
            }
        };

        // Fire init event when Firebase is ready
        window.dispatchEvent(new Event("firebase-ready"));
    </script>

    <style>
        :root {
            --green: #00b87a;
            --green-dark: #008f5e;
            --green-light: #e6f9f2;
            --surface: #ffffff;
            --bg: #f5f7fa;
            --text: #0f1923;
            --muted: #6b7280;
            --border: #e5e9f0;
        }
        * { box-sizing: border-box; }
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: var(--bg);
            color: var(--text);
            min-height: 100vh;
            padding-bottom: 5rem;
        }
        .font-display { font-family: 'Syne', sans-serif; }

        /* Glass header */
        .glass-header {
            background: rgba(255,255,255,0.93);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(0,184,122,0.12);
            box-shadow: 0 2px 20px rgba(0,0,0,0.05);
        }

        /* Gradients */
        .brand-gradient { background: linear-gradient(135deg, #00b87a 0%, #00d68f 100%); }
        .whatsapp-gradient { background: linear-gradient(135deg, #25d366 0%, #128c7e 100%); }

        /* Cards */
        .card {
            background: white;
            border-radius: 20px;
            border: 1px solid var(--border);
            box-shadow: 0 2px 12px rgba(0,0,0,0.04);
        }

        /* Product card */
        .product-card {
            background: white;
            border-radius: 20px;
            border: 1px solid var(--border);
            overflow: hidden;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }
        .product-card:hover {
            transform: translateY(-6px) scale(1.01);
            box-shadow: 0 20px 40px rgba(0,0,0,0.12);
            border-color: rgba(0,184,122,0.3);
        }

        /* Add to cart btn */
        .add-btn {
            width: 36px; height: 36px;
            border-radius: 12px;
            background: var(--green);
            color: white; border: none;
            display: flex; align-items: center; justify-content: center;
            cursor: pointer;
            transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
            box-shadow: 0 4px 12px rgba(0,184,122,0.4);
        }
        .add-btn:hover { transform: scale(1.15); background: var(--green-dark); }

        /* Category pills */
        .cat-pill {
            padding: 0.45rem 1.1rem;
            border-radius: 50px;
            border: 1.5px solid var(--border);
            background: white; color: var(--muted);
            cursor: pointer; font-size: 0.82rem; font-weight: 600;
            white-space: nowrap; transition: all 0.2s;
        }
        .cat-pill:hover { border-color: var(--green); color: var(--green); }
        .cat-pill.active {
            background: var(--green); color: white;
            border-color: var(--green);
            box-shadow: 0 4px 12px rgba(0,184,122,0.3);
        }

        .no-scroll::-webkit-scrollbar { display: none; }
        .no-scroll { -ms-overflow-style: none; scrollbar-width: none; }

        /* Animations */
        @keyframes slideUp { from { transform: translateY(30px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        @keyframes fadeIn  { from { opacity: 0; } to { opacity: 1; } }
        @keyframes popIn   { 0% { transform: scale(0.85); opacity: 0; } 70% { transform: scale(1.03); } 100% { transform: scale(1); opacity: 1; } }
        @keyframes spin    { to { transform: rotate(360deg); } }
        @keyframes pulse   { 0%,100% { opacity: 1; } 50% { opacity: .4; } }

        .slide-up { animation: slideUp 0.35s cubic-bezier(0.34, 1.2, 0.64, 1) both; }
        .pop-in   { animation: popIn 0.4s cubic-bezier(0.34, 1.56, 0.64, 1) both; }
        .spinner  { animation: spin 0.8s linear infinite; }
        .pulse    { animation: pulse 1.5s ease infinite; }

        /* Modals */
        .modal-overlay {
            position: fixed; inset: 0; z-index: 60;
            background: rgba(15,25,35,0.65);
            backdrop-filter: blur(6px);
            display: none; align-items: flex-end; justify-content: center;
        }
        .modal-overlay.active { display: flex; animation: fadeIn 0.2s ease; }
        .modal-overlay.center { align-items: center; }
        .modal-sheet {
            background: white; border-radius: 28px 28px 0 0;
            width: 100%; max-width: 480px;
            max-height: 92vh; overflow-y: auto; padding: 1.5rem;
        }
        .modal-overlay.center .modal-sheet { border-radius: 28px; margin: 1rem; }

        /* USSD */
        .ussd-display {
            background: #0f1923; color: #00e676;
            font-family: 'Courier New', monospace;
            font-size: 1.25rem; letter-spacing: 2px;
            padding: 1rem 1.5rem; border-radius: 14px;
            text-align: center;
            text-shadow: 0 0 10px rgba(0,230,118,0.5);
        }

        /* Cart drawer */
        .cart-overlay { position: fixed; inset: 0; z-index: 55; display: none; }
        .cart-overlay.open { display: block; }
        .cart-backdrop { position: absolute; inset: 0; background: rgba(15,25,35,0.5); backdrop-filter: blur(4px); }
        .cart-panel {
            position: absolute; right: 0; top: 0; bottom: 0;
            width: 100%; max-width: 420px; background: white;
            display: flex; flex-direction: column;
            transform: translateX(100%);
            transition: transform 0.35s cubic-bezier(0.34, 1.1, 0.64, 1);
            box-shadow: -10px 0 60px rgba(0,0,0,0.15);
        }
        .cart-overlay.open .cart-panel { transform: translateX(0); }

        /* Payment cards */
        .pay-card {
            border: 2px solid var(--border); border-radius: 16px;
            padding: 1rem; cursor: pointer; transition: all 0.2s;
        }
        .pay-card:hover { border-color: var(--green); background: var(--green-light); }
        .pay-card.selected { border-color: var(--green); background: var(--green-light); }
        .check-dot {
            width: 22px; height: 22px; border-radius: 50%;
            border: 2px solid var(--border);
            display: flex; align-items: center; justify-content: center;
            transition: all 0.2s; flex-shrink: 0;
        }

        /* Buttons */
        .btn-green {
            background: var(--green); color: white; border: none;
            border-radius: 14px; font-family: 'Plus Jakarta Sans', sans-serif;
            font-weight: 700; cursor: pointer;
            transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
        }
        .btn-green:hover { background: var(--green-dark); transform: translateY(-1px); box-shadow: 0 6px 20px rgba(0,184,122,0.4); }
        .btn-green:disabled { opacity: 0.4; cursor: not-allowed; transform: none; }

        .btn-wa {
            background: linear-gradient(135deg, #25d366, #128c7e);
            color: white; border: none; border-radius: 14px;
            font-family: 'Plus Jakarta Sans', sans-serif; font-weight: 700;
            cursor: pointer; transition: all 0.2s;
            box-shadow: 0 4px 20px rgba(37,211,102,0.35);
        }
        .btn-wa:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(37,211,102,0.5); }
        .btn-wa:disabled { opacity: 0.45; cursor: not-allowed; transform: none; box-shadow: none; }

        /* Toast */
        .toast {
            position: fixed; bottom: 5.5rem; left: 50%;
            transform: translateX(-50%) translateY(20px);
            background: #0f1923; color: white;
            padding: 0.75rem 1.5rem; border-radius: 50px;
            font-size: 0.88rem; font-weight: 600;
            opacity: 0; transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            z-index: 999; white-space: nowrap;
            box-shadow: 0 8px 30px rgba(0,0,0,0.25);
            pointer-events: none;
        }
        .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

        /* Form */
        .form-input {
            width: 100%; padding: 0.65rem 0.85rem;
            border: 1.5px solid var(--border); border-radius: 12px;
            font-family: 'Plus Jakarta Sans', sans-serif;
            font-size: 0.9rem; outline: none; transition: border-color 0.2s;
            background: white;
        }
        .form-input:focus { border-color: var(--green); box-shadow: 0 0 0 3px rgba(0,184,122,0.1); }

        /* Loading overlay */
        .loading-screen {
            position: fixed; inset: 0; z-index: 100;
            background: white;
            display: flex; flex-direction: column;
            align-items: center; justify-content: center; gap: 1rem;
        }
        .loading-screen.hidden { display: none; }

        /* Firebase status badge */
        .firebase-badge {
            display: inline-flex; align-items: center; gap: 0.4rem;
            background: #fff8e1; color: #f57c00;
            padding: 0.25rem 0.75rem; border-radius: 50px;
            font-size: 0.72rem; font-weight: 700;
        }
        .firebase-badge.connected { background: #e6f9f2; color: var(--green-dark); }

        /* Admin badge */
        .admin-badge {
            background: linear-gradient(135deg, #f59e0b, #ef4444);
            color: white; font-size: 0.65rem; font-weight: 800;
            padding: 2px 8px; border-radius: 50px;
            letter-spacing: 1px; text-transform: uppercase;
        }

        .img-wrap { position: relative; aspect-ratio: 1; overflow: hidden; background: #f3f4f6; }
        .img-wrap img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.4s; }
        .product-card:hover .img-wrap img { transform: scale(1.06); }

        .oos-overlay {
            position: absolute; inset: 0;
            background: rgba(0,0,0,0.5);
            display: flex; align-items: center; justify-content: center;
        }

        .stat-card { background: white; border-radius: 18px; border: 1px solid var(--border); padding: 1.1rem; }
        .admin-row {
            background: white; border-radius: 16px; border: 1px solid var(--border);
            padding: 0.85rem; display: flex; align-items: center; gap: 0.85rem;
            transition: all 0.2s;
        }
        .admin-row:hover { border-color: rgba(0,184,122,0.3); box-shadow: 0 4px 16px rgba(0,0,0,0.07); }
        .pay-config { border-radius: 16px; padding: 1.1rem; border: 2px solid; }
        .empty-state { text-align: center; padding: 3rem 1rem; color: var(--muted); }
        input[type="file"].hidden-file { display: none; }

        /* Sync indicator */
        .sync-dot { width: 8px; height: 8px; border-radius: 50%; background: #fbbf24; }
        .sync-dot.synced { background: var(--green); }
        .sync-dot.error  { background: #ef4444; }
    </style>
</head>
<body>

<!-- LOADING SCREEN -->
<div id="loading-screen" class="loading-screen">
    <div class="brand-gradient w-16 h-16 rounded-2xl flex items-center justify-center shadow-xl">
        <i class="fas fa-store text-white text-2xl"></i>
    </div>
    <div class="text-center">
        <p class="font-display font-800 text-xl text-gray-900">Somali Store</p>
        <p id="loading-msg" class="text-sm text-gray-400 mt-1 pulse">Connecting to Firebase...</p>
    </div>
    <i class="fas fa-circle-notch spinner text-green-500 text-xl"></i>
</div>

<!-- FIREBASE CONFIG WARNING -->
<div id="config-warning" class="loading-screen hidden" style="gap:1.5rem; padding:2rem; text-align:center;">
    <div class="w-16 h-16 bg-orange-100 rounded-2xl flex items-center justify-center">
        <i class="fas fa-fire text-orange-500 text-2xl"></i>
    </div>
    <div>
        <p class="font-display font-800 text-xl text-gray-900 mb-2">Firebase Not Configured</p>
        <p class="text-sm text-gray-500 leading-relaxed max-w-xs mx-auto">
            You need to add your Firebase config to the HTML file.<br><br>
            Open the file, find <code class="bg-gray-100 px-1 rounded">firebaseConfig</code> near the top, and replace the placeholder values with your real Firebase project credentials.
        </p>
    </div>
    <div class="bg-gray-50 rounded-2xl p-4 text-left text-xs font-mono text-gray-600 max-w-xs w-full">
        <p class="text-green-600 font-bold mb-2">// Steps:</p>
        <p>1. firebase.google.com</p>
        <p>2. Create project</p>
        <p>3. Firestore → Create DB</p>
        <p>4. Project Settings → Web App</p>
        <p>5. Copy config → paste here</p>
    </div>
    <button onclick="document.getElementById('config-warning').classList.add('hidden'); document.getElementById('loading-screen').classList.remove('hidden'); initApp();"
        class="btn-green px-6 py-3 text-sm">
        I've Added My Config — Try Again
    </button>
</div>

<!-- ============ HEADER ============ -->
<header class="glass-header fixed top-0 left-0 right-0 z-50">
    <div class="max-w-lg mx-auto px-4 py-3 flex items-center justify-between">
        <div class="flex items-center gap-2.5 min-w-0">
            <div class="brand-gradient w-10 h-10 rounded-2xl flex items-center justify-center shadow-lg flex-shrink-0">
                <i class="fas fa-store text-white"></i>
            </div>
            <div class="min-w-0">
                <div class="flex items-center gap-2">
                    <h1 id="store-name-display" class="font-display font-800 text-lg text-gray-900 truncate leading-tight">Somali Store</h1>
                    <span id="admin-badge" class="admin-badge hidden">Admin</span>
                </div>
                <div class="flex items-center gap-1.5">
                    <div id="sync-dot" class="sync-dot"></div>
                    <p id="role-label" class="text-xs text-gray-400 font-medium">Connecting...</p>
                </div>
            </div>
        </div>
        <div class="flex items-center gap-1">
            <button id="admin-lock-btn" onclick="toggleAdminLogin()" class="p-2.5 hover:bg-gray-100 rounded-xl transition-colors">
                <i id="lock-icon" class="fas fa-lock text-gray-400 text-sm"></i>
            </button>
            <button id="cart-btn" onclick="openCart()" class="customer-only relative p-2.5 hover:bg-gray-100 rounded-xl transition-colors">
                <i class="fas fa-shopping-bag text-gray-700 text-xl"></i>
                <span id="cart-badge" class="absolute -top-0.5 -right-0.5 bg-red-500 text-white text-xs font-bold w-5 h-5 rounded-full items-center justify-center hidden">0</span>
            </button>
            <button id="admin-menu-btn" onclick="scrollToSettings()" class="admin-only hidden p-2.5 hover:bg-gray-100 rounded-xl transition-colors">
                <i class="fas fa-sliders-h text-gray-700"></i>
            </button>
        </div>
    </div>
</header>

<!-- ============ CUSTOMER VIEW ============ -->
<main id="customer-view" class="customer-only max-w-lg mx-auto pt-20 px-4 space-y-5 pb-24">
    <div class="brand-gradient rounded-2xl p-4 text-white flex items-center justify-between shadow-lg mt-2">
        <div>
            <div class="font-display font-800 text-xl leading-tight" id="hero-store-name">Somali Store</div>
            <p class="text-white/75 text-xs mt-0.5">Free delivery · WhatsApp ordering · 🔥 Live data</p>
        </div>
        <div class="text-4xl">🛍️</div>
    </div>

    <div class="relative">
        <i class="fas fa-search absolute left-4 top-1/2 -translate-y-1/2 text-gray-400 text-sm pointer-events-none"></i>
        <input type="text" id="search-input" class="form-input w-full py-3 pl-11" placeholder="Search products..." oninput="renderShop()">
    </div>

    <div class="flex gap-2 overflow-x-auto no-scroll pb-1" id="categories-row"></div>

    <div>
        <div class="flex justify-between items-center mb-3">
            <h2 class="font-bold text-gray-800">Products</h2>
            <span id="product-count" class="text-xs text-gray-400 font-medium bg-gray-100 px-3 py-1 rounded-full">Loading...</span>
        </div>
        <div id="products-grid" class="grid grid-cols-2 gap-3">
            <!-- Loading skeletons -->
            <div class="product-card h-48 bg-gray-100 animate-pulse rounded-2xl"></div>
            <div class="product-card h-48 bg-gray-100 animate-pulse rounded-2xl"></div>
            <div class="product-card h-48 bg-gray-100 animate-pulse rounded-2xl"></div>
            <div class="product-card h-48 bg-gray-100 animate-pulse rounded-2xl"></div>
        </div>
    </div>

    <div class="card p-4 bg-gradient-to-br from-blue-50 to-white border-blue-100">
        <h4 class="font-bold text-blue-800 text-sm flex items-center gap-2 mb-1.5">
            <i class="fas fa-mobile-alt text-blue-500"></i> Lacag Bixinta (Payment)
        </h4>
        <p class="text-xs text-blue-700 leading-relaxed">
            Waxaan aqbalnaa <strong>ZAAD</strong>, <strong>SAHAL</strong>, <strong>E-DAHAB</strong>, iyo <strong>Crypto</strong>. Sugitaanka waa bilaash!
        </p>
    </div>
</main>

<!-- ============ ADMIN VIEW ============ -->
<main id="admin-view" class="admin-only hidden max-w-lg mx-auto pt-20 px-4 space-y-5 pb-24">
    <div class="flex items-center justify-between">
        <div>
            <h2 class="font-display font-800 text-2xl text-gray-900">Dashboard</h2>
            <p class="text-sm text-gray-500 mt-0.5">Live Firebase data</p>
        </div>
        <button onclick="showAddModal()" class="btn-green flex items-center gap-2 px-4 py-2.5 text-sm">
            <i class="fas fa-plus"></i> Add Product
        </button>
    </div>

    <!-- Sync status -->
    <div class="card p-3 flex items-center gap-3">
        <i class="fas fa-fire text-orange-500"></i>
        <div class="flex-1">
            <p class="text-sm font-700 text-gray-800">Firebase Firestore</p>
            <p id="firebase-status-text" class="text-xs text-gray-400">Connected — data saves instantly to cloud</p>
        </div>
        <div id="firebase-dot" class="sync-dot synced"></div>
    </div>

    <!-- Stats -->
    <div class="grid grid-cols-3 gap-3">
        <div class="stat-card text-center">
            <div class="text-2xl font-display font-800 text-green-600" id="stat-products">0</div>
            <div class="text-xs text-gray-500 font-medium mt-0.5">Products</div>
        </div>
        <div class="stat-card text-center">
            <div class="text-2xl font-display font-800 text-blue-600" id="stat-cats">0</div>
            <div class="text-xs text-gray-500 font-medium mt-0.5">Categories</div>
        </div>
        <div class="stat-card text-center">
            <div class="text-2xl font-display font-800 text-orange-500" id="stat-active">0</div>
            <div class="text-xs text-gray-500 font-medium mt-0.5">In Stock</div>
        </div>
    </div>

    <!-- Store Settings -->
    <div id="store-settings-section" class="card p-5 space-y-4">
        <h3 class="font-bold text-gray-800 flex items-center gap-2 text-sm">
            <i class="fas fa-store text-green-500"></i> Store Settings
            <span class="text-xs text-green-600 font-normal ml-auto">Saved to Firebase</span>
        </h3>
        <div>
            <label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">Store Name</label>
            <div class="flex gap-2">
                <input type="text" id="admin-store-name" class="form-input flex-1">
                <button onclick="saveStoreName()" class="btn-green px-4 py-2 text-sm flex-shrink-0"><i class="fas fa-save"></i></button>
            </div>
        </div>
        <div>
            <label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">
                <i class="fab fa-whatsapp text-green-500"></i> WhatsApp Number
            </label>
            <div class="flex gap-2">
                <input type="text" id="admin-whatsapp" class="form-input flex-1" placeholder="252xxxxxxxxx">
                <button onclick="saveWhatsApp()" class="btn-green px-4 py-2 text-sm flex-shrink-0"><i class="fas fa-save"></i></button>
            </div>
            <p class="text-xs text-gray-400 mt-1">Format: 252xxxxxxxx (no + or spaces)</p>
        </div>
        <div>
            <label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">Currency</label>
            <select id="admin-currency" onchange="saveCurrency()" class="form-input">
                <option value="$">USD ($)</option>
                <option value="€">EUR (€)</option>
                <option value="£">GBP (£)</option>
                <option value="SOS">SOS (Sh)</option>
            </select>
        </div>
        <div>
            <label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">Admin Password</label>
            <div class="flex gap-2">
                <input type="password" id="admin-new-password" class="form-input flex-1" placeholder="New password">
                <button onclick="changePassword()" class="btn-green px-4 py-2 text-sm flex-shrink-0"><i class="fas fa-key"></i></button>
            </div>
        </div>
    </div>

    <!-- Shipping -->
    <div class="card p-5">
        <div class="flex items-center justify-between mb-4">
            <h3 class="font-bold text-gray-800 text-sm flex items-center gap-2">
                <i class="fas fa-shipping-fast text-green-500"></i> Shipping Prices
            </h3>
            <button onclick="openShippingModal()" class="text-xs font-600 text-green-600 hover:underline">Edit</button>
        </div>
        <div class="space-y-2.5">
            <div class="flex justify-between text-sm"><span class="text-gray-600">🏙️ Local (Mogadishu)</span><span id="ship-local-display" class="font-bold">$0</span></div>
            <div class="flex justify-between text-sm"><span class="text-gray-600">🇸🇴 Regional (Somalia)</span><span id="ship-regional-display" class="font-bold">$0</span></div>
            <div class="flex justify-between text-sm"><span class="text-gray-600">✈️ International</span><span id="ship-intl-display" class="font-bold">$0</span></div>
        </div>
    </div>

    <!-- Payments -->
    <div class="card p-5">
        <div class="flex items-center justify-between mb-4">
            <h3 class="font-bold text-gray-800 text-sm flex items-center gap-2">
                <i class="fas fa-credit-card text-green-500"></i> Lacag Bixinta (Payments)
            </h3>
        </div>
        <div id="admin-payment-list" class="space-y-2 mb-4"></div>
        <button onclick="openPaymentSetup()" class="w-full py-2.5 bg-gray-50 border border-dashed border-gray-300 rounded-xl text-sm font-600 text-gray-600 hover:bg-green-50 hover:border-green-300 hover:text-green-700 transition-all">
            <i class="fas fa-cog mr-2"></i> Configure Payment Accounts
        </button>
    </div>

    <!-- Products list -->
    <div>
        <h3 class="font-bold text-gray-800 mb-3">All Products <span class="text-xs text-green-500 font-normal">(live sync)</span></h3>
        <div id="admin-product-list" class="space-y-2.5"></div>
    </div>

    <button onclick="exitAdmin()" class="w-full py-3 bg-gray-100 text-gray-600 rounded-2xl font-600 hover:bg-gray-200 transition-all flex items-center justify-center gap-2">
        <i class="fas fa-sign-out-alt"></i> Exit Admin Mode
    </button>
</main>

<!-- ============ CART DRAWER ============ -->
<div id="cart-drawer" class="cart-overlay">
    <div class="cart-backdrop" onclick="closeCart()"></div>
    <div class="cart-panel">
        <div class="p-4 border-b border-gray-100 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <h2 class="font-bold text-lg">Your Cart</h2>
                <span id="cart-item-count" class="bg-green-100 text-green-700 text-xs font-700 px-2 py-0.5 rounded-full">0</span>
            </div>
            <button onclick="closeCart()" class="p-2 hover:bg-gray-100 rounded-xl"><i class="fas fa-times text-gray-500"></i></button>
        </div>
        <div id="cart-items-list" class="flex-1 overflow-y-auto p-4 space-y-3"></div>
        <div class="p-4 border-t bg-gray-50 space-y-3">
            <div class="flex justify-between"><span class="text-gray-500 text-sm">Subtotal</span><span id="cart-subtotal-val" class="font-bold">$0.00</span></div>
            <div class="flex justify-between text-lg"><span class="font-bold">Total</span><span id="cart-total-val" class="font-display font-800 text-green-600">$0.00</span></div>
            <button onclick="openPaymentModal()" class="btn-wa w-full py-3.5 flex items-center justify-center gap-2 text-sm font-700 rounded-2xl">
                <i class="fas fa-credit-card"></i> Proceed to Payment
            </button>
        </div>
    </div>
</div>

<!-- PRODUCT VIEW MODAL -->
<div id="product-view-modal" class="modal-overlay" onclick="if(event.target===this)closeProductView()">
    <div class="modal-sheet slide-up">
        <div class="flex justify-between items-center mb-4">
            <div class="w-8"></div>
            <div class="w-12 h-1 bg-gray-200 rounded-full"></div>
            <button onclick="closeProductView()" class="w-8 h-8 flex items-center justify-center hover:bg-gray-100 rounded-lg">
                <i class="fas fa-times text-gray-400 text-sm"></i>
            </button>
        </div>
        <img id="pv-img" src="" class="w-full aspect-square object-cover rounded-2xl mb-4 bg-gray-100">
        <div class="flex items-start justify-between mb-2">
            <h3 id="pv-name" class="font-display font-800 text-xl text-gray-900 flex-1 pr-2"></h3>
            <span id="pv-price" class="font-display font-800 text-xl text-green-600 flex-shrink-0"></span>
        </div>
        <span id="pv-cat" class="inline-block text-xs font-700 text-gray-500 bg-gray-100 px-3 py-1 rounded-full capitalize mb-3"></span>
        <p id="pv-desc" class="text-sm text-gray-500 leading-relaxed mb-5"></p>
        <button id="pv-add-btn" class="btn-green w-full py-3.5 flex items-center justify-center gap-2 font-700 text-sm">
            <i class="fas fa-shopping-bag"></i> Add to Cart
        </button>
    </div>
</div>

<!-- PAYMENT MODAL -->
<div id="payment-modal" class="modal-overlay" onclick="if(event.target===this)closePaymentModal()">
    <div class="modal-sheet slide-up">
        <div class="text-center mb-5">
            <div class="w-14 h-14 brand-gradient rounded-2xl flex items-center justify-center mx-auto mb-3 shadow-lg">
                <i class="fab fa-whatsapp text-white text-2xl"></i>
            </div>
            <h3 class="font-display font-800 text-xl text-gray-900">Dhamaystir Dalabka</h3>
            <p class="text-sm text-gray-400 mt-0.5">Complete your order</p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-4 mb-4 space-y-2.5">
            <div class="flex justify-between text-sm"><span class="text-gray-500">Wadarta (Subtotal)</span><span id="pm-subtotal" class="font-bold">$0.00</span></div>
            <div class="flex justify-between text-sm items-center">
                <span class="text-gray-500">Shipping</span>
                <select id="pm-shipping-select" onchange="calcPaymentTotal()" class="text-xs border border-gray-200 rounded-lg px-2 py-1 font-600 bg-white">
                    <option value="local">🏙️ Local</option>
                    <option value="regional">🇸🇴 Regional</option>
                    <option value="international">✈️ International</option>
                </select>
            </div>
            <div id="pm-shipping-line" class="flex justify-between text-sm"></div>
            <div class="border-t border-gray-200 pt-2.5 flex justify-between items-center">
                <span class="font-bold text-base">TOTAL</span>
                <span id="pm-total" class="font-display font-800 text-xl text-green-600">$0.00</span>
            </div>
        </div>
        <p class="text-xs font-700 text-gray-400 uppercase tracking-widest mb-3">Choose Payment</p>
        <div id="pm-methods-list" class="space-y-2.5 mb-5"></div>
        <button id="pm-whatsapp-btn" onclick="proceedToWhatsApp()" disabled class="btn-wa w-full py-4 flex items-center justify-center gap-2 font-700">
            <i class="fab fa-whatsapp text-xl"></i> Send Order via WhatsApp
        </button>
    </div>
</div>

<!-- USSD MODAL -->
<div id="ussd-modal" class="modal-overlay center" onclick="if(event.target===this)closeUSSD()">
    <div class="modal-sheet pop-in text-center space-y-4">
        <div class="w-14 h-14 bg-gray-900 rounded-2xl flex items-center justify-center mx-auto">
            <i class="fas fa-mobile-alt text-green-400 text-2xl"></i>
        </div>
        <div>
            <h3 class="font-bold text-gray-900 text-lg">Fadlan Geli (Dial This)</h3>
            <p class="text-sm text-gray-400 mt-0.5">Copy and dial to complete payment</p>
        </div>
        <div class="ussd-display" id="ussd-code-text">*883*252656884433*100#</div>
        <button onclick="copyUSSD()" class="w-full py-3 bg-gray-900 text-white rounded-2xl font-700 flex items-center justify-center gap-2 hover:bg-gray-800 transition-colors">
            <i class="fas fa-copy"></i> Copy Code
        </button>
        <button onclick="closeUSSD()" class="w-full py-2 text-gray-400 text-sm font-500">Close</button>
    </div>
</div>

<!-- ADD/EDIT PRODUCT MODAL -->
<div id="product-modal" class="modal-overlay" onclick="if(event.target===this)closeProductModal()">
    <div class="modal-sheet slide-up">
        <div class="flex justify-between items-center mb-5">
            <h3 id="product-modal-title" class="font-bold text-lg">Add Product</h3>
            <button onclick="closeProductModal()" class="p-2 hover:bg-gray-100 rounded-xl"><i class="fas fa-times text-gray-400"></i></button>
        </div>
        <form onsubmit="saveProduct(event)" class="space-y-4">
            <input type="hidden" id="edit-product-id">
            <div class="relative aspect-square bg-gray-100 rounded-2xl overflow-hidden">
                <img id="product-img-preview" src="https://placehold.co/400x400/f3f4f6/9ca3af?text=Add+Photo" class="w-full h-full object-cover">
                <input type="file" id="product-img-file" accept="image/*" class="hidden-file" onchange="loadProductImage(this)">
                <button type="button" onclick="document.getElementById('product-img-file').click()" class="absolute inset-0 flex flex-col items-center justify-center bg-black/20 hover:bg-black/30 gap-2">
                    <i class="fas fa-camera text-white text-2xl drop-shadow"></i>
                    <span class="text-white text-sm font-600 drop-shadow">Upload Photo</span>
                </button>
            </div>
            <input type="url" id="product-img-url" placeholder="Or paste image URL" class="form-input text-sm" oninput="document.getElementById('product-img-preview').src=this.value||'https://placehold.co/400x400/f3f4f6/9ca3af?text=Add+Photo'">
            <input type="text" id="p-name" placeholder="Product name *" required class="form-input">
            <input type="number" id="p-price" placeholder="Price *" step="0.01" min="0" required class="form-input">
            <select id="p-category" class="form-input">
                <option value="general">General</option>
                <option value="electronics">Electronics</option>
                <option value="fashion">Fashion</option>
                <option value="home">Home</option>
                <option value="beauty">Beauty</option>
                <option value="food">Food</option>
                <option value="sports">Sports</option>
                <option value="kids">Kids</option>
            </select>
            <textarea id="p-desc" placeholder="Description (optional)" rows="2" class="form-input resize-none"></textarea>
            <label class="flex items-center gap-3 cursor-pointer">
                <div class="relative">
                    <input type="checkbox" id="p-instock" checked class="sr-only peer">
                    <div class="w-11 h-6 bg-gray-200 rounded-full peer-checked:bg-green-500 transition-colors"></div>
                    <div class="absolute left-1 top-1 w-4 h-4 bg-white rounded-full transition-transform peer-checked:translate-x-5 shadow"></div>
                </div>
                <span class="text-sm font-600 text-gray-700">In Stock</span>
            </label>
            <button type="submit" id="save-product-btn" class="btn-green w-full py-3.5 font-700">Save to Firebase</button>
        </form>
    </div>
</div>

<!-- PAYMENT SETUP MODAL -->
<div id="payment-setup-modal" class="modal-overlay" onclick="if(event.target===this)closePaymentSetup()">
    <div class="modal-sheet slide-up">
        <div class="flex justify-between items-center mb-5">
            <h3 class="font-bold text-lg">Configure Payments</h3>
            <button onclick="closePaymentSetup()" class="p-2 hover:bg-gray-100 rounded-xl"><i class="fas fa-times text-gray-400"></i></button>
        </div>
        <div class="space-y-4">
            <div class="pay-config border-blue-200 bg-blue-50">
                <div class="flex items-center gap-2 font-bold text-blue-700 mb-3"><span class="text-xl">📱</span> ZAAD <span class="text-xs font-normal text-blue-500">(Telesom)</span></div>
                <input type="text" id="setup-zaad" placeholder="ZAAD number (2526xxxxxxxx)" class="form-input text-sm">
                <p class="text-xs text-blue-400 mt-1.5">USSD: *883*NUMBER*AMOUNT#</p>
            </div>
            <div class="pay-config border-orange-200 bg-orange-50">
                <div class="flex items-center gap-2 font-bold text-orange-700 mb-3"><span class="text-xl">📱</span> SAHAL <span class="text-xs font-normal text-orange-500">(Somtel)</span></div>
                <input type="text" id="setup-sahal" placeholder="SAHAL number" class="form-input text-sm">
                <p class="text-xs text-orange-400 mt-1.5">USSD: *884*NUMBER*AMOUNT#</p>
            </div>
            <div class="pay-config border-red-200 bg-red-50">
                <div class="flex items-center gap-2 font-bold text-red-700 mb-3"><span class="text-xl">📱</span> E-DAHAB <span class="text-xs font-normal text-red-500">(Dahabshiil)</span></div>
                <input type="text" id="setup-edahab" placeholder="E-DAHAB number" class="form-input text-sm">
                <p class="text-xs text-red-400 mt-1.5">USSD: *113*NUMBER*AMOUNT#</p>
            </div>
            <div class="pay-config border-purple-200 bg-purple-50">
                <div class="flex items-center gap-2 font-bold text-purple-700 mb-3"><span class="text-xl">🎁</span> EVoucher</div>
                <input type="text" id="setup-evoucher" placeholder="EVoucher number" class="form-input text-sm">
            </div>
            <div class="pay-config border-yellow-200 bg-yellow-50">
                <div class="flex items-center gap-2 font-bold text-yellow-700 mb-3"><span class="text-xl">₿</span> Cryptocurrency</div>
                <select id="setup-crypto-type" class="form-input text-sm mb-2">
                    <option value="USDT">USDT (Tether)</option>
                    <option value="BTC">Bitcoin (BTC)</option>
                    <option value="ETH">Ethereum (ETH)</option>
                </select>
                <input type="text" id="setup-crypto-addr" placeholder="Wallet address" class="form-input text-sm">
                <label class="flex items-center gap-2 mt-2 cursor-pointer">
                    <input type="checkbox" id="setup-crypto-enabled" checked class="w-4 h-4 text-green-500 rounded">
                    <span class="text-xs text-yellow-700 font-600">Enable Crypto Payments</span>
                </label>
            </div>
        </div>
        <button onclick="savePaymentMethods()" class="btn-green w-full py-3.5 font-700 mt-5">Save to Firebase</button>
    </div>
</div>

<!-- SHIPPING MODAL -->
<div id="shipping-modal" class="modal-overlay center" onclick="if(event.target===this)closeShippingModal()">
    <div class="modal-sheet pop-in">
        <div class="flex justify-between items-center mb-5">
            <h3 class="font-bold text-lg">Shipping Prices</h3>
            <button onclick="closeShippingModal()" class="p-2 hover:bg-gray-100 rounded-xl"><i class="fas fa-times text-gray-400"></i></button>
        </div>
        <div class="space-y-4">
            <div><label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">🏙️ Local (Mogadishu)</label><input type="number" id="ship-local-val" step="0.01" min="0" class="form-input" value="0"></div>
            <div><label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">🇸🇴 Regional (Somalia)</label><input type="number" id="ship-regional-val" step="0.01" min="0" class="form-input" value="5"></div>
            <div><label class="text-xs font-700 text-gray-500 uppercase tracking-wide mb-1.5 block">✈️ International</label><input type="number" id="ship-intl-val" step="0.01" min="0" class="form-input" value="15"></div>
        </div>
        <button onclick="saveShipping()" class="btn-green w-full py-3.5 font-700 mt-5">Save to Firebase</button>
    </div>
</div>

<!-- ADMIN LOGIN MODAL -->
<div id="admin-login-modal" class="modal-overlay center" onclick="if(event.target===this)closeAdminLogin()">
    <div class="modal-sheet pop-in w-full max-w-sm mx-4 text-center">
        <div class="w-14 h-14 brand-gradient rounded-2xl flex items-center justify-center mx-auto mb-4 shadow-lg">
            <i class="fas fa-lock text-white text-xl"></i>
        </div>
        <h3 class="font-display font-800 text-xl mb-1">Admin Access</h3>
        <p class="text-sm text-gray-400 mb-5">Enter password to manage your store</p>
        <input type="password" id="admin-password-input" placeholder="Password" class="form-input mb-3" onkeydown="if(event.key==='Enter')checkAdminPassword()">
        <button onclick="checkAdminPassword()" class="btn-green w-full py-3 font-700">Unlock Admin</button>
        <button onclick="closeAdminLogin()" class="w-full mt-2 py-2 text-sm text-gray-400">Cancel</button>
    </div>
</div>

<!-- TOAST -->
<div id="toast" class="toast"><i class="fas fa-check-circle text-green-400 mr-1.5"></i><span id="toast-text">Done</span></div>

<script>
// ===== STATE =====
let ADMIN_PASSWORD = localStorage.getItem('store-admin-pw') || '6884433@@';
let products = [];
let settings = { name: 'Somali Store', whatsapp: '252656884433', currency: '$' };
let payments = {
    zaad:    { number: '', enabled: false },
    sahal:   { number: '', enabled: false },
    edahab:  { number: '', enabled: false },
    evoucher:{ number: '', enabled: false },
    crypto:  { type: 'USDT', address: '', enabled: false }
};
let shipping = { local: 0, regional: 5, international: 15 };
let cart = [];
let currentCategory = 'all';
let isAdmin = false;
let selectedPayment = null;
let currentUSSDCode = '';
let unsubscribeProducts = null;

// ===== INIT =====
window.addEventListener('firebase-ready', initApp);

async function initApp() {
    try {
        document.getElementById('loading-msg').textContent = 'Loading store data...';
        // Load settings from Firebase
        const fbSettings = await window.FB.getSettings();
        if (fbSettings.store?.value) Object.assign(settings, fbSettings.store.value);
        if (fbSettings.payments?.value) Object.assign(payments, fbSettings.payments.value);
        if (fbSettings.shipping?.value) Object.assign(shipping, fbSettings.shipping.value);
        if (fbSettings.adminPw?.value) ADMIN_PASSWORD = fbSettings.adminPw.value;

        // Real-time product listener
        unsubscribeProducts = window.FB.listenProducts(prods => {
            products = prods;
            renderShop();
            if (isAdmin) { renderAdminProducts(); updateAdminStats(); }
        });

        applySettings();
        document.getElementById('loading-screen').classList.add('hidden');
        document.getElementById('sync-dot').classList.add('synced');
        document.getElementById('role-label').textContent = 'Customer View';

    } catch (err) {
        console.error(err);
        if (err.message?.includes('projectId') || err.message?.includes('API key') || err.code === 'invalid-argument') {
            document.getElementById('loading-screen').classList.add('hidden');
            document.getElementById('config-warning').classList.remove('hidden');
        } else {
            document.getElementById('loading-msg').textContent = 'Connection error. Using offline mode.';
            document.getElementById('sync-dot').classList.add('error');
            // Fallback to localStorage
            const lsSettings = JSON.parse(localStorage.getItem('store-settings') || '{}');
            Object.assign(settings, lsSettings);
            products = JSON.parse(localStorage.getItem('store-products') || '[]');
            applySettings();
            setTimeout(() => document.getElementById('loading-screen').classList.add('hidden'), 1500);
        }
    }
}

function applySettings() {
    document.title = settings.name;
    ['store-name-display','hero-store-name'].forEach(id => {
        const el = document.getElementById(id);
        if (el) el.textContent = settings.name;
    });
    const nameEl = document.getElementById('admin-store-name');
    if (nameEl) nameEl.value = settings.name;
    const waEl = document.getElementById('admin-whatsapp');
    if (waEl) waEl.value = settings.whatsapp;
    const curEl = document.getElementById('admin-currency');
    if (curEl) curEl.value = settings.currency;
    updateShippingDisplay();
    renderAdminPayments();
}

// ===== FIREBASE HELPERS =====
async function fbSaveSetting(key, value) {
    try {
        await window.FB.saveSetting(key, value);
    } catch (e) {
        // fallback localStorage
        localStorage.setItem('store-' + key, JSON.stringify(value));
    }
}

// ===== ADMIN AUTH =====
function toggleAdminLogin() {
    if (isAdmin) { exitAdmin(); return; }
    document.getElementById('admin-password-input').value = '';
    document.getElementById('admin-login-modal').classList.add('active');
    setTimeout(() => document.getElementById('admin-password-input').focus(), 300);
}
function closeAdminLogin() { document.getElementById('admin-login-modal').classList.remove('active'); }

function checkAdminPassword() {
    const pw = document.getElementById('admin-password-input').value;
    if (pw === ADMIN_PASSWORD) { closeAdminLogin(); enableAdmin(); }
    else {
        const inp = document.getElementById('admin-password-input');
        inp.value = ''; inp.classList.add('border-red-400');
        inp.placeholder = 'Wrong password, try again';
        setTimeout(() => { inp.classList.remove('border-red-400'); inp.placeholder = 'Password'; }, 2000);
    }
}

function enableAdmin() {
    isAdmin = true;
    document.getElementById('customer-view').classList.add('hidden');
    document.getElementById('admin-view').classList.remove('hidden');
    document.querySelectorAll('.admin-only').forEach(el => el.classList.remove('hidden'));
    document.querySelectorAll('.customer-only').forEach(el => el.classList.add('hidden'));
    document.getElementById('role-label').textContent = 'Admin Mode';
    document.getElementById('admin-badge').classList.remove('hidden');
    document.getElementById('lock-icon').className = 'fas fa-unlock text-green-500 text-sm';
    document.getElementById('admin-menu-btn').classList.remove('hidden');
    document.getElementById('cart-btn').classList.add('hidden');
    applySettings();
    renderAdminProducts();
    updateAdminStats();
    showToast('Welcome back, Admin! 👋');
}

function exitAdmin() {
    isAdmin = false;
    document.getElementById('admin-view').classList.add('hidden');
    document.getElementById('customer-view').classList.remove('hidden');
    document.querySelectorAll('.admin-only').forEach(el => el.classList.add('hidden'));
    document.querySelectorAll('.customer-only').forEach(el => el.classList.remove('hidden'));
    document.getElementById('role-label').textContent = 'Customer View';
    document.getElementById('admin-badge').classList.add('hidden');
    document.getElementById('lock-icon').className = 'fas fa-lock text-gray-400 text-sm';
    document.getElementById('admin-menu-btn').classList.add('hidden');
    document.getElementById('cart-btn').classList.remove('hidden');
    renderShop();
    showToast('Exited admin mode');
}

function scrollToSettings() {
    document.getElementById('store-settings-section').scrollIntoView({ behavior: 'smooth' });
}

async function changePassword() {
    const newPw = document.getElementById('admin-new-password').value.trim();
    if (!newPw || newPw.length < 4) return showToast('Password too short!');
    ADMIN_PASSWORD = newPw;
    await fbSaveSetting('adminPw', newPw);
    localStorage.setItem('store-admin-pw', newPw);
    document.getElementById('admin-new-password').value = '';
    showToast('Password changed & saved to Firebase!');
}

// ===== SETTINGS =====
async function saveStoreName() {
    const name = document.getElementById('admin-store-name').value.trim();
    if (!name) return;
    settings.name = name;
    await fbSaveSetting('store', settings);
    applySettings();
    showToast('Store name saved to Firebase!');
}

async function saveWhatsApp() {
    const num = document.getElementById('admin-whatsapp').value.trim();
    if (!num) return;
    settings.whatsapp = num;
    await fbSaveSetting('store', settings);
    showToast('WhatsApp saved to Firebase!');
}

async function saveCurrency() {
    settings.currency = document.getElementById('admin-currency').value;
    await fbSaveSetting('store', settings);
    renderShop(); renderAdminProducts();
    showToast('Currency updated!');
}

function fmt(price) { return settings.currency + parseFloat(price).toFixed(2); }

// ===== SHOP =====
function renderShop() {
    const search = (document.getElementById('search-input')?.value || '').toLowerCase();
    const filtered = products.filter(p =>
        (currentCategory === 'all' || p.category === currentCategory) &&
        p.name.toLowerCase().includes(search) &&
        p.inStock !== false
    );
    document.getElementById('product-count').textContent = filtered.length + ' items';

    const grid = document.getElementById('products-grid');
    if (filtered.length === 0) {
        grid.innerHTML = `<div class="col-span-2 text-center py-12 text-gray-400">
            <div class="text-5xl mb-3 opacity-20">🛍️</div>
            <p class="font-600">${products.length === 0 ? 'No products yet' : 'No results'}</p>
        </div>`;
    } else {
        grid.innerHTML = filtered.map(p => `
            <div class="product-card" onclick="viewProduct('${p.id}')">
                <div class="img-wrap">
                    <img src="${p.image||'https://placehold.co/400x400/f3f4f6/9ca3af?text=No+Image'}"
                         onerror="this.src='https://placehold.co/400x400/f3f4f6/9ca3af?text=No+Image'">
                    ${!p.inStock ? '<div class="oos-overlay"><span class="bg-red-500 text-white text-xs font-700 px-2 py-1 rounded-full">Out of Stock</span></div>' : ''}
                    <button class="add-btn absolute bottom-2 right-2" onclick="event.stopPropagation();addToCart('${p.id}')">
                        <i class="fas fa-plus text-sm"></i>
                    </button>
                </div>
                <div class="p-3">
                    <h4 class="font-700 text-gray-900 text-sm truncate leading-tight">${p.name}</h4>
                    <div class="flex justify-between items-center mt-1.5">
                        <span class="font-display font-800 text-green-600">${fmt(p.price)}</span>
                        <span class="text-xs text-gray-400 capitalize">${p.category}</span>
                    </div>
                </div>
            </div>
        `).join('');
    }

    const cats = ['all', ...new Set(products.map(p => p.category).filter(Boolean))];
    document.getElementById('categories-row').innerHTML = cats.map(c => `
        <button onclick="setCategory('${c}')" class="cat-pill ${currentCategory===c?'active':''} capitalize">${c}</button>
    `).join('');
}

function setCategory(cat) { currentCategory = cat; renderShop(); }

// ===== PRODUCT VIEW =====
function viewProduct(id) {
    const p = products.find(x => x.id == id); if (!p) return;
    document.getElementById('pv-img').src = p.image || 'https://placehold.co/400x400/f3f4f6/9ca3af?text=No+Image';
    document.getElementById('pv-name').textContent = p.name;
    document.getElementById('pv-price').textContent = fmt(p.price);
    document.getElementById('pv-cat').textContent = p.category;
    document.getElementById('pv-desc').textContent = p.description || 'No description available.';
    document.getElementById('pv-add-btn').onclick = () => { addToCart(id); closeProductView(); };
    document.getElementById('pv-add-btn').disabled = p.inStock === false;
    document.getElementById('pv-add-btn').innerHTML = p.inStock === false ? 'Out of Stock' : '<i class="fas fa-shopping-bag"></i> Add to Cart';
    document.getElementById('product-view-modal').classList.add('active');
}
function closeProductView() { document.getElementById('product-view-modal').classList.remove('active'); }

// ===== CART =====
function addToCart(id) {
    const p = products.find(x => x.id == id);
    if (!p || p.inStock === false) return showToast('Out of stock!');
    const ex = cart.find(x => x.id == id);
    if (ex) ex.qty++; else cart.push({ ...p, qty: 1 });
    updateCartUI(); showToast('Added to cart! 🛍️');
}

function changeQty(id, delta) {
    const item = cart.find(x => x.id == id); if (!item) return;
    item.qty += delta;
    if (item.qty <= 0) cart = cart.filter(x => x.id != id);
    updateCartUI();
}

function removeFromCart(id) { cart = cart.filter(x => x.id != id); updateCartUI(); }

function updateCartUI() {
    const totalQty = cart.reduce((s,x) => s+x.qty, 0);
    const subtotal = cart.reduce((s,x) => s+x.price*x.qty, 0);
    const badge = document.getElementById('cart-badge');
    badge.textContent = totalQty;
    totalQty > 0 ? (badge.classList.remove('hidden'), badge.classList.add('flex')) : (badge.classList.add('hidden'), badge.classList.remove('flex'));
    document.getElementById('cart-item-count').textContent = totalQty;

    const list = document.getElementById('cart-items-list');
    list.innerHTML = cart.length === 0
        ? `<div class="text-center py-16 text-gray-400"><div class="text-5xl mb-3 opacity-20">🛒</div><p class="font-600">Cart is empty</p></div>`
        : cart.map(x => `
            <div class="flex gap-3 bg-gray-50 rounded-2xl p-3 items-center">
                <img src="${x.image||''}" onerror="this.src='https://placehold.co/80x80/f3f4f6/9ca3af?text=?'"
                     class="w-16 h-16 object-cover rounded-xl flex-shrink-0">
                <div class="flex-1 min-w-0">
                    <p class="font-700 text-sm text-gray-900 truncate">${x.name}</p>
                    <p class="font-display font-800 text-green-600 text-sm">${fmt(x.price*x.qty)}</p>
                    <div class="flex items-center gap-2 mt-1.5">
                        <button onclick="changeQty('${x.id}',-1)" class="w-7 h-7 bg-white border border-gray-200 rounded-lg flex items-center justify-center hover:bg-gray-100">−</button>
                        <span class="text-sm font-700 w-5 text-center">${x.qty}</span>
                        <button onclick="changeQty('${x.id}',1)" class="w-7 h-7 bg-white border border-gray-200 rounded-lg flex items-center justify-center hover:bg-gray-100">+</button>
                    </div>
                </div>
                <button onclick="removeFromCart('${x.id}')" class="p-2 hover:bg-red-50 rounded-xl">
                    <i class="fas fa-trash-alt text-red-400 text-sm"></i>
                </button>
            </div>`).join('');

    document.getElementById('cart-subtotal-val').textContent = fmt(subtotal);
    document.getElementById('cart-total-val').textContent = fmt(subtotal);
}

function openCart()  { document.getElementById('cart-drawer').classList.add('open'); }
function closeCart() { document.getElementById('cart-drawer').classList.remove('open'); }

// ===== PAYMENT MODAL =====
function openPaymentModal() {
    if (!cart.length) return; closeCart();
    const subtotal = cart.reduce((s,x) => s+x.price*x.qty, 0);
    document.getElementById('pm-subtotal').textContent = fmt(subtotal);
    calcPaymentTotal();

    const container = document.getElementById('pm-methods-list');
    const defs = [
        { key:'zaad',     label:'ZAAD',     sub: payments.zaad.number,     icon:'📱' },
        { key:'sahal',    label:'SAHAL',    sub: payments.sahal.number,    icon:'📱' },
        { key:'edahab',   label:'E-DAHAB',  sub: payments.edahab.number,   icon:'📱' },
        { key:'evoucher', label:'EVoucher', sub: payments.evoucher.number, icon:'🎁' },
        { key:'crypto',   label:`${payments.crypto.type} Crypto`, sub:'Cryptocurrency', icon:'₿' }
    ];
    let html = '';
    defs.forEach(m => {
        if (payments[m.key]?.enabled && (payments[m.key]?.number || payments[m.key]?.address)) {
            html += `<div class="pay-card" id="pay-opt-${m.key}" onclick="selectPayment('${m.key}')">
                <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <span class="text-2xl">${m.icon}</span>
                        <div><div class="font-700 text-base">${m.label}</div><div class="text-xs text-gray-400">${m.sub}</div></div>
                    </div>
                    <div class="check-dot" id="check-${m.key}"></div>
                </div>
            </div>`;
        }
    });
    if (!html) html = `<div class="text-center py-6 text-sm text-gray-400"><i class="fas fa-exclamation-circle text-2xl block mb-2 opacity-30"></i>No payment methods configured.</div>`;
    container.innerHTML = html;
    selectedPayment = null;
    document.getElementById('pm-whatsapp-btn').disabled = true;
    document.getElementById('payment-modal').classList.add('active');
}

function closePaymentModal() { document.getElementById('payment-modal').classList.remove('active'); selectedPayment = null; }

function calcPaymentTotal() {
    const subtotal = cart.reduce((s,x) => s+x.price*x.qty, 0);
    const type = document.getElementById('pm-shipping-select').value;
    const cost = shipping[type] || 0;
    const labels = { local:'🏙️ Local', regional:'🇸🇴 Regional', international:'✈️ International' };
    document.getElementById('pm-shipping-line').innerHTML = `<span class="text-gray-500">${labels[type]}</span><span class="font-600">${fmt(cost)}</span>`;
    document.getElementById('pm-total').textContent = fmt(subtotal + cost);
}

function selectPayment(key) {
    selectedPayment = key;
    document.querySelectorAll('.pay-card').forEach(el => el.classList.remove('selected'));
    document.querySelectorAll('[id^="check-"]').forEach(el => { el.innerHTML=''; el.style.background=''; el.style.borderColor=''; });
    document.getElementById(`pay-opt-${key}`)?.classList.add('selected');
    const dot = document.getElementById(`check-${key}`);
    if (dot) { dot.innerHTML='<i class="fas fa-check text-white text-xs"></i>'; dot.style.background='var(--green)'; dot.style.borderColor='var(--green)'; }
    document.getElementById('pm-whatsapp-btn').disabled = false;
}

function proceedToWhatsApp() {
    if (!selectedPayment || !cart.length) return;
    const subtotal = cart.reduce((s,x) => s+x.price*x.qty, 0);
    const type = document.getElementById('pm-shipping-select').value;
    const cost = shipping[type] || 0;
    const total = subtotal + cost;
    const labels = { local:'Local (Mogadishu)', regional:'Regional (Somalia)', international:'International' };

    let msg = `🛒 *DALAB CUSUB - NEW ORDER*\n━━━━━━━━━━━━━━━━━━━━\n*Alaabta (Items):*\n`;
    cart.forEach(x => msg += `  • ${x.name} ×${x.qty} = ${fmt(x.price*x.qty)}\n`);
    msg += `━━━━━━━━━━━━━━━━━━━━\nSubtotal: ${fmt(subtotal)}\nShipping (${labels[type]}): ${fmt(cost)}\n*💰 TOTAL: ${fmt(total)}*\n━━━━━━━━━━━━━━━━━━━━\n`;

    const m = payments[selectedPayment];
    const ussdMap = { zaad:'*883', sahal:'*884', edahab:'*113' };
    if (ussdMap[selectedPayment] && m.number) {
        const ussd = `${ussdMap[selectedPayment]}*${m.number}*${Math.round(total)}#`;
        currentUSSDCode = ussd;
        msg += `💳 *${selectedPayment.toUpperCase()} Payment:*\nNumber: ${m.number}\nDial: \`${ussd}\`\n`;
        setTimeout(() => showUSSDModal(ussd), 500);
    } else if (selectedPayment === 'evoucher') {
        msg += `🎁 *EVoucher Payment:*\nNumber: ${m.number}\nFadlan soo dir voucher-kaaga\n`;
    } else if (selectedPayment === 'crypto') {
        msg += `₿ *${m.type} Crypto:*\nAddress: \`${m.address}\`\nAmount: ${fmt(total)} equiv.\n`;
    }
    msg += `━━━━━━━━━━━━━━━━━━━━\n📍 *Goobta:* ________________\n📞 *Tel:* ________________\n\nMahadsanid! 🙏`;

    window.open(`https://wa.me/${settings.whatsapp}?text=${encodeURIComponent(msg)}`, '_blank');
    cart = []; updateCartUI(); closePaymentModal(); showToast('Order sent! ✅');
}

// ===== USSD =====
function showUSSDModal(code) { document.getElementById('ussd-code-text').textContent = code; document.getElementById('ussd-modal').classList.add('active'); }
function closeUSSD() { document.getElementById('ussd-modal').classList.remove('active'); }
function copyUSSD() { navigator.clipboard.writeText(currentUSSDCode).then(() => showToast('USSD code copied!')); }

// ===== PRODUCT CRUD (Firebase) =====
function showAddModal() {
    document.getElementById('edit-product-id').value = '';
    document.getElementById('product-modal-title').textContent = 'Add Product';
    document.getElementById('p-name').value = '';
    document.getElementById('p-price').value = '';
    document.getElementById('p-category').value = 'general';
    document.getElementById('p-desc').value = '';
    document.getElementById('p-instock').checked = true;
    document.getElementById('product-img-url').value = '';
    document.getElementById('product-img-preview').src = 'https://placehold.co/400x400/f3f4f6/9ca3af?text=Add+Photo';
    document.getElementById('product-modal').classList.add('active');
}

function editProduct(id) {
    const p = products.find(x => x.id == id); if (!p) return;
    document.getElementById('edit-product-id').value = id;
    document.getElementById('product-modal-title').textContent = 'Edit Product';
    document.getElementById('p-name').value = p.name;
    document.getElementById('p-price').value = p.price;
    document.getElementById('p-category').value = p.category || 'general';
    document.getElementById('p-desc').value = p.description || '';
    document.getElementById('p-instock').checked = p.inStock !== false;
    document.getElementById('product-img-url').value = p.image || '';
    document.getElementById('product-img-preview').src = p.image || 'https://placehold.co/400x400/f3f4f6/9ca3af?text=No+Image';
    document.getElementById('product-modal').classList.add('active');
}

function closeProductModal() { document.getElementById('product-modal').classList.remove('active'); }

function loadProductImage(input) {
    if (!input.files?.[0]) return;
    const reader = new FileReader();
    reader.onload = e => {
        document.getElementById('product-img-preview').src = e.target.result;
        document.getElementById('product-img-url').value = e.target.result;
    };
    reader.readAsDataURL(input.files[0]);
}

async function saveProduct(e) {
    e.preventDefault();
    const btn = document.getElementById('save-product-btn');
    btn.textContent = 'Saving...'; btn.disabled = true;
    try {
        const editId = document.getElementById('edit-product-id').value;
        const data = {
            id:          editId || String(Date.now()),
            name:        document.getElementById('p-name').value.trim(),
            price:       parseFloat(document.getElementById('p-price').value),
            category:    document.getElementById('p-category').value,
            description: document.getElementById('p-desc').value.trim(),
            image:       document.getElementById('product-img-url').value || 'https://placehold.co/400x400/f3f4f6/9ca3af?text=No+Image',
            inStock:     document.getElementById('p-instock').checked
        };
        await window.FB.saveProduct(data);
        closeProductModal();
        showToast(editId ? 'Product updated in Firebase! ✅' : 'Product added to Firebase! 🎉');
    } catch (err) {
        console.error(err);
        showToast('Error saving. Check Firebase config.');
    }
    btn.textContent = 'Save to Firebase'; btn.disabled = false;
}

async function deleteProduct(id) {
    if (!confirm('Delete this product from Firebase?')) return;
    try {
        await window.FB.deleteProduct(id);
        showToast('Product deleted');
    } catch { showToast('Error deleting product'); }
}

function renderAdminProducts() {
    const list = document.getElementById('admin-product-list');
    if (!products.length) {
        list.innerHTML = `<div class="text-center py-8 text-gray-400 border-2 border-dashed border-gray-200 rounded-2xl">
            <i class="fas fa-box-open text-3xl mb-2 opacity-30 block"></i>
            <p class="text-sm font-600">No products yet</p>
        </div>`; return;
    }
    list.innerHTML = products.map(p => `
        <div class="admin-row">
            <img src="${p.image||''}" onerror="this.src='https://placehold.co/64x64/f3f4f6/9ca3af?text=?'"
                 class="w-14 h-14 object-cover rounded-xl flex-shrink-0">
            <div class="flex-1 min-w-0">
                <p class="font-700 text-sm text-gray-900 truncate">${p.name}</p>
                <p class="font-display font-800 text-green-600 text-sm">${fmt(p.price)}</p>
                <div class="flex items-center gap-2 mt-0.5">
                    <span class="text-xs text-gray-400 capitalize">${p.category}</span>
                    <span class="text-xs ${p.inStock!==false?'text-green-500':'text-red-400'} font-600">● ${p.inStock!==false?'In Stock':'Out of Stock'}</span>
                </div>
            </div>
            <div class="flex gap-1">
                <button onclick="editProduct('${p.id}')" class="w-9 h-9 flex items-center justify-center text-blue-500 hover:bg-blue-50 rounded-xl">
                    <i class="fas fa-pen text-sm"></i>
                </button>
                <button onclick="deleteProduct('${p.id}')" class="w-9 h-9 flex items-center justify-center text-red-400 hover:bg-red-50 rounded-xl">
                    <i class="fas fa-trash text-sm"></i>
                </button>
            </div>
        </div>`).join('');
}

function updateAdminStats() {
    document.getElementById('stat-products').textContent = products.length;
    document.getElementById('stat-cats').textContent = new Set(products.map(p => p.category)).size;
    document.getElementById('stat-active').textContent = products.filter(p => p.inStock !== false).length;
}

// ===== PAYMENT CONFIG =====
function openPaymentSetup() {
    document.getElementById('setup-zaad').value = payments.zaad.number||'';
    document.getElementById('setup-sahal').value = payments.sahal.number||'';
    document.getElementById('setup-edahab').value = payments.edahab.number||'';
    document.getElementById('setup-evoucher').value = payments.evoucher.number||'';
    document.getElementById('setup-crypto-type').value = payments.crypto.type||'USDT';
    document.getElementById('setup-crypto-addr').value = payments.crypto.address||'';
    document.getElementById('setup-crypto-enabled').checked = payments.crypto.enabled;
    document.getElementById('payment-setup-modal').classList.add('active');
}
function closePaymentSetup() { document.getElementById('payment-setup-modal').classList.remove('active'); }

async function savePaymentMethods() {
    payments = {
        zaad:    { number: document.getElementById('setup-zaad').value.trim(), enabled: !!document.getElementById('setup-zaad').value.trim() },
        sahal:   { number: document.getElementById('setup-sahal').value.trim(), enabled: !!document.getElementById('setup-sahal').value.trim() },
        edahab:  { number: document.getElementById('setup-edahab').value.trim(), enabled: !!document.getElementById('setup-edahab').value.trim() },
        evoucher:{ number: document.getElementById('setup-evoucher').value.trim(), enabled: !!document.getElementById('setup-evoucher').value.trim() },
        crypto:  { type: document.getElementById('setup-crypto-type').value, address: document.getElementById('setup-crypto-addr').value.trim(), enabled: document.getElementById('setup-crypto-enabled').checked && !!document.getElementById('setup-crypto-addr').value.trim() }
    };
    await fbSaveSetting('payments', payments);
    closePaymentSetup(); renderAdminPayments(); showToast('Payments saved to Firebase!');
}

function renderAdminPayments() {
    const list = document.getElementById('admin-payment-list');
    const active = [];
    if (payments.zaad.enabled)     active.push({ label:'ZAAD',    icon:'📱', color:'bg-blue-100 text-blue-700' });
    if (payments.sahal.enabled)    active.push({ label:'SAHAL',   icon:'📱', color:'bg-orange-100 text-orange-700' });
    if (payments.edahab.enabled)   active.push({ label:'E-DAHAB', icon:'📱', color:'bg-red-100 text-red-700' });
    if (payments.evoucher.enabled) active.push({ label:'EVoucher',icon:'🎁', color:'bg-purple-100 text-purple-700' });
    if (payments.crypto.enabled)   active.push({ label:payments.crypto.type, icon:'₿', color:'bg-yellow-100 text-yellow-700' });
    list.innerHTML = active.length
        ? active.map(m => `<div class="flex items-center gap-3 py-2"><span>${m.icon}</span><span class="font-600 text-sm">${m.label}</span><span class="ml-auto text-xs font-700 px-2.5 py-0.5 rounded-full ${m.color}">Active</span></div>`).join('')
        : '<p class="text-sm text-gray-400">No payment methods configured</p>';
}

// ===== SHIPPING =====
function openShippingModal() {
    document.getElementById('ship-local-val').value = shipping.local;
    document.getElementById('ship-regional-val').value = shipping.regional;
    document.getElementById('ship-intl-val').value = shipping.international;
    document.getElementById('shipping-modal').classList.add('active');
}
function closeShippingModal() { document.getElementById('shipping-modal').classList.remove('active'); }

async function saveShipping() {
    shipping = {
        local:         parseFloat(document.getElementById('ship-local-val').value)||0,
        regional:      parseFloat(document.getElementById('ship-regional-val').value)||0,
        international: parseFloat(document.getElementById('ship-intl-val').value)||0
    };
    await fbSaveSetting('shipping', shipping);
    closeShippingModal(); updateShippingDisplay(); showToast('Shipping saved to Firebase!');
}

function updateShippingDisplay() {
    document.getElementById('ship-local-display').textContent = fmt(shipping.local);
    document.getElementById('ship-regional-display').textContent = fmt(shipping.regional);
    document.getElementById('ship-intl-display').textContent = fmt(shipping.international);
}

// ===== TOAST =====
let toastTimer;
function showToast(msg) {
    clearTimeout(toastTimer);
    document.getElementById('toast-text').textContent = msg;
    document.getElementById('toast').classList.add('show');
    toastTimer = setTimeout(() => document.getElementById('toast').classList.remove('show'), 3000);
}
</script>
</body>
</html>
