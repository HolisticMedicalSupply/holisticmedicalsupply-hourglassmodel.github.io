<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DME Product Hierarchy - The Hourglass Model</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 2rem;
        }
        
        .flow-line {
            stroke-dasharray: 1000;
            stroke-dashoffset: 1000;
            animation: draw 2s ease-in-out forwards;
        }
        
        @keyframes draw {
            to {
                stroke-dashoffset: 0;
            }
        }
        
        .node-card {
            transition: all 0.3s ease;
            animation: fadeInUp 0.6s ease-out backwards;
        }
        
        .node-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .level-1 { animation-delay: 0.1s; }
        .level-2 { animation-delay: 0.3s; }
        .level-3 { animation-delay: 0.5s; }
        .level-4 { animation-delay: 0.7s; }
        .level-5 { animation-delay: 0.9s; }
        .level-6 { animation-delay: 1.1s; }
        
        .bottleneck-pulse {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        
        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: .7;
            }
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .arrow {
            width: 0;
            height: 0;
            border-left: 8px solid transparent;
            border-right: 8px solid transparent;
            border-top: 12px solid currentColor;
            display: inline-block;
            margin: 0 8px;
        }
        
        .arrow-right {
            transform: rotate(90deg);
        }
    </style>
</head>
<body>
    <div class="max-w-[1800px] mx-auto">
        <!-- Header -->
        <div class="text-center mb-12">
            <h1 class="text-5xl md:text-6xl font-bold text-white mb-4">
                The Hourglass Model
            </h1>
            <p class="text-xl md:text-2xl text-purple-100 mb-2">
                DME Product Hierarchy: From Category to Pricing Options
            </p>
            <p class="text-lg text-purple-200 max-w-3xl mx-auto">
                Watch how one product model explodes into dozens of unique pricing options
            </p>
        </div>

        <!-- Main Flow Container -->
        <div class="bg-white rounded-3xl shadow-2xl p-8 md:p-12 mb-8">
            <div class="overflow-x-auto">
                <div class="flex items-center gap-6 min-w-[1600px] justify-center">
                    
                    <!-- Level 1: Categories -->
                    <div class="flex flex-col gap-3" style="width: 200px;">
                        <div class="text-center mb-3">
                            <span class="inline-block bg-indigo-100 text-indigo-800 px-4 py-2 rounded-full text-sm font-bold">
                                CATEGORIES
                            </span>
                        </div>
                        <div class="node-card level-1 bg-gray-200 text-gray-500 p-4 rounded-xl text-center text-sm opacity-50">
                            Wound Care
                        </div>
                        <div class="node-card level-1 bg-gradient-to-br from-indigo-500 to-indigo-600 text-white p-4 rounded-xl text-center font-semibold shadow-lg border-4 border-indigo-300">
                            <div class="text-base">Orthopedic</div>
                            <div class="text-base">Supports & Braces</div>
                        </div>
                        <div class="node-card level-1 bg-gray-200 text-gray-500 p-4 rounded-xl text-center text-sm opacity-50">
                            Mobility Aids
                        </div>
                        <div class="node-card level-1 bg-gray-200 text-gray-500 p-4 rounded-xl text-center text-sm opacity-50">
                            Respiratory
                        </div>
                        <div class="text-center mt-2 text-xs text-gray-600 font-semibold">
                            4 Categories
                        </div>
                    </div>

                    <!-- Arrow/Branch 1 -->
                    <div class="flex flex-col items-center justify-center" style="width: 80px;">
                        <svg width="80" height="260" viewBox="0 0 80 260">
                            <defs>
                                <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" style="stop-color:#6366f1;stop-opacity:0.6" />
                                    <stop offset="100%" style="stop-color:#3b82f6;stop-opacity:0.6" />
                                </linearGradient>
                            </defs>
                            <path class="flow-line" d="M 0 130 Q 40 130, 80 70" stroke="url(#grad1)" stroke-width="3" fill="none"/>
                            <path class="flow-line" d="M 0 130 L 80 130" stroke="url(#grad1)" stroke-width="3" fill="none"/>
                            <path class="flow-line" d="M 0 130 Q 40 130, 80 190" stroke="url(#grad1)" stroke-width="3" fill="none"/>
                        </svg>
                        <div class="text-xs text-gray-500 font-semibold">Branch</div>
                    </div>

                    <!-- Level 2: Types -->
                    <div class="flex flex-col gap-3" style="width: 180px;">
                        <div class="text-center mb-3">
                            <span class="inline-block bg-blue-100 text-blue-800 px-4 py-2 rounded-full text-sm font-bold">
                                TYPES
                            </span>
                        </div>
                        <div class="node-card level-2 bg-gradient-to-br from-blue-500 to-blue-600 text-white p-4 rounded-xl text-center font-semibold shadow-lg border-4 border-blue-300">
                            Wrist Braces<br/>& Supports
                        </div>
                        <div class="node-card level-2 bg-gray-200 text-gray-500 p-3 rounded-xl text-center text-sm opacity-50">
                            Knee Braces
                        </div>
                        <div class="node-card level-2 bg-gray-200 text-gray-500 p-3 rounded-xl text-center text-sm opacity-50">
                            Ankle Braces
                        </div>
                        <div class="text-center mt-2 text-xs text-gray-600 font-semibold">
                            3 Types
                        </div>
                    </div>

                    <!-- Arrow 2 -->
                    <div class="flex flex-col items-center justify-center" style="width: 80px;">
                        <svg width="80" height="200" viewBox="0 0 80 200">
                            <defs>
                                <linearGradient id="grad2" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" style="stop-color:#3b82f6;stop-opacity:0.6" />
                                    <stop offset="100%" style="stop-color:#10b981;stop-opacity:0.6" />
                                </linearGradient>
                            </defs>
                            <path class="flow-line" d="M 0 50 Q 40 50, 80 100" stroke="url(#grad2)" stroke-width="3" fill="none"/>
                        </svg>
                        <div class="text-xs text-gray-500 font-semibold">Focus</div>
                    </div>

                    <!-- Level 3: ITEM (Bottleneck) -->
                    <div class="flex flex-col items-center" style="width: 220px;">
                        <div class="text-center mb-3">
                            <span class="inline-block bg-green-100 text-green-800 px-4 py-2 rounded-full text-sm font-bold">
                                ITEM
                            </span>
                        </div>
                        <div class="node-card level-3 bg-gradient-to-br from-green-500 via-emerald-500 to-teal-500 text-white p-6 rounded-2xl text-center shadow-2xl border-4 border-green-300 bottleneck-pulse">
                            <div class="text-2xl font-bold mb-1">⭐</div>
                            <div class="text-lg font-bold">ComfortFit</div>
                            <div class="text-base">Carpal Tunnel Brace</div>
                            <div class="mt-3 text-xs bg-white/20 rounded-lg py-1 px-2">
                                THE BOTTLENECK
                            </div>
                        </div>
                        <div class="text-center mt-2 text-xs text-gray-600 font-semibold">
                            1 Item Model
                        </div>
                    </div>

                    <!-- Arrow 3 - Expansion begins -->
                    <div class="flex flex-col items-center justify-center" style="width: 80px;">
                        <svg width="80" height="200" viewBox="0 0 80 200">
                            <defs>
                                <linearGradient id="grad3" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" style="stop-color:#10b981;stop-opacity:0.6" />
                                    <stop offset="100%" style="stop-color:#a855f7;stop-opacity:0.6" />
                                </linearGradient>
                            </defs>
                            <path class="flow-line" d="M 0 100 Q 40 100, 80 40" stroke="url(#grad3)" stroke-width="3" fill="none"/>
                            <path class="flow-line" d="M 0 100 Q 40 100, 80 80" stroke="url(#grad3)" stroke-width="3" fill="none"/>
                            <path class="flow-line" d="M 0 100 Q 40 100, 80 120" stroke="url(#grad3)" stroke-width="3" fill="none"/>
                            <path class="flow-line" d="M 0 100 Q 40 100, 80 160" stroke="url(#grad3)" stroke-width="3" fill="none"/>
                        </svg>
                        <div class="text-xs text-gray-500 font-semibold">Expand</div>
                    </div>

                    <!-- Level 4: Products -->
                    <div class="flex flex-col gap-2" style="width: 180px;">
                        <div class="text-center mb-2">
                            <span class="inline-block bg-purple-100 text-purple-800 px-4 py-2 rounded-full text-sm font-bold">
                                PRODUCTS 📦
                            </span>
                        </div>
                        <div class="node-card level-4 bg-gradient-to-br from-purple-500 to-purple-600 text-white p-3 rounded-lg text-center text-sm shadow-lg">
                            Ossur ComfortFit
                        </div>
                        <div class="node-card level-4 bg-gradient-to-br from-purple-500 to-purple-600 text-white p-3 rounded-lg text-center text-sm shadow-lg">
                            Futuro ComfortFit
                        </div>
                        <div class="node-card level-4 bg-gradient-to-br from-purple-500 to-purple-600 text-white p-3 rounded-lg text-center text-sm shadow-lg">
                            Breg ComfortFit
                        </div>
                        <div class="node-card level-4 bg-gradient-to-br from-purple-500 to-purple-600 text-white p-3 rounded-lg text-center text-sm shadow-lg">
                            DonJoy ComfortFit
                        </div>
                        <div class="text-center mt-1 text-xs text-gray-600 font-semibold">
                            4 Products<br/>(manufacturers)
                        </div>
                    </div>

                    <!-- Arrow 4 -->
                    <div class="flex flex-col items-center justify-center" style="width: 60px;">
                        <svg width="60" height="220" viewBox="0 0 60 220">
                            <defs>
                                <linearGradient id="grad4" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" style="stop-color:#a855f7;stop-opacity:0.5" />
                                    <stop offset="100%" style="stop-color:#f97316;stop-opacity:0.5" />
                                </linearGradient>
                            </defs>
                            <path class="flow-line" d="M 0 35 L 60 30" stroke="url(#grad4)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 70 L 60 65" stroke="url(#grad4)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 105 L 60 100" stroke="url(#grad4)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 140 L 60 135" stroke="url(#grad4)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 175 L 60 170" stroke="url(#grad4)" stroke-width="2" fill="none"/>
                        </svg>
                        <div class="text-xs text-gray-500 font-semibold">×</div>
                    </div>

                    <!-- Level 5: Units -->
                    <div class="flex flex-col gap-2" style="width: 180px;">
                        <div class="text-center mb-2">
                            <span class="inline-block bg-orange-100 text-orange-800 px-4 py-2 rounded-full text-sm font-bold">
                                UNITS 🎯
                            </span>
                        </div>
                        <div class="node-card level-5 bg-gradient-to-br from-orange-500 to-orange-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Ossur/OrthoCare
                        </div>
                        <div class="node-card level-5 bg-gradient-to-br from-orange-500 to-orange-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Ossur/Cardinal
                        </div>
                        <div class="node-card level-5 bg-gradient-to-br from-orange-500 to-orange-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Futuro/Patterson
                        </div>
                        <div class="node-card level-5 bg-gradient-to-br from-orange-500 to-orange-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Breg/Henry Schein
                        </div>
                        <div class="node-card level-5 bg-gradient-to-br from-orange-500 to-orange-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            DonJoy/Medline
                        </div>
                        <div class="text-center mt-1 text-xs text-gray-600 font-semibold">
                            5 Units 🎯<br/>(from Supply Sources)
                        </div>
                    </div>

                    <!-- Arrow 5 -->
                    <div class="flex flex-col items-center justify-center" style="width: 60px;">
                        <svg width="60" height="240" viewBox="0 0 60 240">
                            <defs>
                                <linearGradient id="grad5" x1="0%" y1="0%" x2="100%" y2="0%">
                                    <stop offset="0%" style="stop-color:#f97316;stop-opacity:0.5" />
                                    <stop offset="100%" style="stop-color:#ef4444;stop-opacity:0.5" />
                                </linearGradient>
                            </defs>
                            <path class="flow-line" d="M 0 30 L 60 20" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 30 L 60 45" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 65 L 60 70" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 100 L 60 95" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 100 L 60 120" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 135 L 60 145" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 170 L 60 170" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 170 L 60 195" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                            <path class="flow-line" d="M 0 205 L 60 220" stroke="url(#grad5)" stroke-width="2" fill="none"/>
                        </svg>
                        <div class="text-xs text-gray-500 font-semibold">💥</div>
                    </div>

                    <!-- Level 6: Pricing Options -->
                    <div class="flex flex-col gap-1.5" style="width: 180px;">
                        <div class="text-center mb-2">
                            <span class="inline-block bg-red-100 text-red-800 px-4 py-2 rounded-full text-sm font-bold">
                                PRICING OPTIONS 💰
                            </span>
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Medicare @ $45
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Medicaid @ $38
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            BCBS @ $52
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Cash @ $65
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Workers Comp @ $58
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Private @ $55
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Medicare/Cardinal @ $46
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            Medicaid/Futuro @ $40
                        </div>
                        <div class="node-card level-6 bg-gradient-to-br from-red-500 to-red-600 text-white p-2 rounded-lg text-center text-xs shadow-md">
                            + Many More...
                        </div>
                        <div class="text-center mt-1 text-xs text-gray-600 font-semibold">
                            9+ Pricing Options<br/>(per Unit × Code)
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <!-- Educational Panels -->
        <div class="grid md:grid-cols-3 gap-6 mb-8">
            <!-- Panel 1 -->
            <div class="bg-white rounded-2xl p-6 shadow-xl">
                <div class="flex items-center gap-3 mb-4">
                    <div class="w-12 h-12 bg-gradient-to-br from-blue-500 to-indigo-600 rounded-xl flex items-center justify-center text-2xl">
                        📊
                    </div>
                    <h3 class="text-xl font-bold text-gray-800">The Path</h3>
                </div>
                <p class="text-gray-600 leading-relaxed">
                    Follow the highlighted path: <strong>Orthopedic Supports → Wrist Braces → ComfortFit</strong>. This traces how we narrow down from broad business categories to a specific item model.
                </p>
            </div>

            <!-- Panel 2 -->
            <div class="bg-white rounded-2xl p-6 shadow-xl">
                <div class="flex items-center gap-3 mb-4">
                    <div class="w-12 h-12 bg-gradient-to-br from-green-500 to-emerald-600 rounded-xl flex items-center justify-center text-2xl">
                        ⭐
                    </div>
                    <h3 class="text-xl font-bold text-gray-800">The Bottleneck</h3>
                </div>
                <p class="text-gray-600 leading-relaxed">
                    <strong>Item</strong> is the critical layer - it's the model name <em>without</em> manufacturer. Multiple companies can make "ComfortFit" with the same specs.
                </p>
            </div>

            <!-- Panel 3 -->
            <div class="bg-white rounded-2xl p-6 shadow-xl">
                <div class="flex items-center gap-3 mb-4">
                    <div class="w-12 h-12 bg-gradient-to-br from-red-500 to-pink-600 rounded-xl flex items-center justify-center text-2xl">
                        💥
                    </div>
                    <h3 class="text-xl font-bold text-gray-800">The Explosion</h3>
                </div>
                <p class="text-gray-600 leading-relaxed">
                    One item model generates <strong>dozens of final pricing options</strong> when combined with all manufacturer, vendor, and payer options. This is where complexity lives.
                </p>
            </div>
        </div>

        <!-- Workflow Stages Explanation -->
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 shadow-xl border-2 border-indigo-200 mb-8">
            <h3 class="text-2xl font-bold text-indigo-900 mb-6 flex items-center gap-3">
                <span class="text-3xl">⚙️</span>
                How the Workflow System Uses This Hierarchy
            </h3>
            <div class="grid md:grid-cols-2 gap-6">
                <div class="bg-white rounded-xl p-5 shadow-md border-l-4 border-green-500">
                    <div class="font-bold text-gray-800 mb-3 flex items-center gap-2">
                        <span class="text-2xl">✅</span>
                        Stage 1 & 2: YOU ADD & LINK
                    </div>
                    <p class="text-sm text-gray-600 mb-2">
                        You manually add: <strong>Products 📦</strong>, <strong>Billing Codes 📋</strong>, and <strong>Vendors 🏢</strong>
                    </p>
                    <p class="text-sm text-gray-600">
                        Then you create: <strong>Billing Permissions ✅</strong> (Product ↔ Code) and <strong>Supply Sources 📦</strong> (Product ↔ Vendor)
                    </p>
                </div>
                <div class="bg-white rounded-xl p-5 shadow-md border-l-4 border-purple-500">
                    <div class="font-bold text-gray-800 mb-3 flex items-center gap-2">
                        <span class="text-2xl">⚙️</span>
                        Stage 3 & 4: SYSTEM AUTO-CREATES
                    </div>
                    <p class="text-sm text-gray-600 mb-2">
                        System creates: <strong>Units 🎯</strong> automatically from each Supply Source (Product + Vendor)
                    </p>
                    <p class="text-sm text-gray-600">
                        Then creates: <strong>Pricing Options 💰</strong> automatically (Unit × Billing Permission for every combination)
                    </p>
                </div>
            </div>
            <div class="mt-6 bg-gradient-to-r from-indigo-100 to-purple-100 rounded-xl p-5 border-2 border-indigo-300">
                <div class="font-bold text-indigo-900 mb-2 text-lg">🔄 Complete Automation Flow:</div>
                <p class="text-sm text-gray-700">
                    <strong>Product 📦</strong> → Link to Code (Billing Permission ✅) + Link to Vendor (Supply Source 📦) → Creates <strong>Unit 🎯</strong> → Combines with all Billing Permissions → Creates <strong>Pricing Options 💰</strong> automatically!
                </p>
            </div>
        </div>

        <!-- Key Insights -->
        <div class="bg-gradient-to-br from-amber-50 to-yellow-50 rounded-2xl p-8 shadow-xl border-2 border-amber-200">
            <h3 class="text-2xl font-bold text-amber-900 mb-6 flex items-center gap-3">
                <span class="text-3xl">💡</span>
                Critical Business Insights
            </h3>
            <div class="grid md:grid-cols-2 gap-6">
                <div class="bg-white rounded-xl p-5 shadow-md">
                    <div class="font-bold text-gray-800 mb-2 flex items-center gap-2">
                        <span class="text-purple-600">🎯</span>
                        Disambiguation Layer
                    </div>
                    <p class="text-sm text-gray-600">
                        The <strong>Product</strong> level (Item + Manufacturer) is where you solve the naming collision problem. "ComfortFit" from Ossur vs. Futuro are different products despite identical item names.
                    </p>
                </div>
                <div class="bg-white rounded-xl p-5 shadow-md">
                    <div class="font-bold text-gray-800 mb-2 flex items-center gap-2">
                        <span class="text-orange-600">📈</span>
                        Exponential Growth
                    </div>
                    <p class="text-sm text-gray-600">
                        The math: 1 Item × 4 Manufacturers × 3 Vendors × 5 Billing Codes = <strong>60 unique pricing options</strong> (Units auto-created from Supply Sources, Pricing Options auto-created from Units + Billing Permissions)
                    </p>
                </div>
                <div class="bg-white rounded-xl p-5 shadow-md">
                    <div class="font-bold text-gray-800 mb-2 flex items-center gap-2">
                        <span class="text-green-600">💰</span>
                        Pricing Complexity
                    </div>
                    <p class="text-sm text-gray-600">
                        Same product, same vendor, wildly different prices: Medicare ($45), Medicaid ($38), Private Pay ($65). Each scenario requires unique billing codes and documentation.
                    </p>
                </div>
                <div class="bg-white rounded-xl p-5 shadow-md">
                    <div class="font-bold text-gray-800 mb-2 flex items-center gap-2">
                        <span class="text-blue-600">🗂️</span>
                        Data Model Power
                    </div>
                    <p class="text-sm text-gray-600">
                        This 6-level hierarchy lets you: track inventory by vendor (Supply Sources 📦), compare pricing across payers, analyze margin by manufacturer, ensure compliance with Billing Permissions ✅, and automate Units 🎯 and Pricing Options 💰 creation.
                    </p>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div class="text-center mt-8 text-white text-sm opacity-75">
            <p>DME Product Hierarchy Model • Designed for Orthopedic Supply & Medical Equipment Businesses</p>
        </div>
    </div>
</body>
</html>
