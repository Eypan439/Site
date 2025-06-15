<html lang="tr"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>İngilizce Kelime ve Deyim Kartları - Sürüm 3</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .flashcard {
            perspective: 1000px;
            height: 200px;
            cursor: pointer;
            transition: transform 0.3s;
            position: relative;
        }
        
        .flashcard:hover {
            transform: translateY(-5px);
        }
        
        .flashcard-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-radius: 1rem;
        }
        
        .flashcard.flipped .flashcard-inner {
            transform: rotateY(180deg);
        }
        
        .flashcard-front, .flashcard-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 1rem;
            padding: 1.5rem;
        }
        
        .flashcard-front {
            background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%);
            color: white;
        }
        
        .flashcard-back {
            background: linear-gradient(135deg, #10b981 0%, #34d399 100%);
            color: #333;
            transform: rotateY(180deg);
        }
        
        .delete-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(239, 68, 68, 0.9);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 10;
            cursor: pointer;
        }
        
        .flashcard:hover .delete-btn {
            opacity: 1;
        }
        
        .delete-btn:hover {
            background-color: rgb(239, 68, 68);
        }
        
        .quiz-option {
            transition: all 0.3s;
        }
        
        .quiz-option:hover {
            transform: translateX(5px);
        }
        
        .quiz-option.correct {
            background-color: #4ade80 !important;
            color: white;
        }
        
        .quiz-option.incorrect {
            background-color: #f87171 !important;
            color: white;
        }
        
        .empty-state {
            border: 2px dashed #cbd5e1;
            border-radius: 1rem;
            transition: all 0.3s;
        }
        
        .empty-state:hover {
            border-color: #94a3b8;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #1e293b;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .toast.show {
            opacity: 1;
        }
        
        .code-modal {
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .code-content {
            white-space: pre-wrap;
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            overflow-x: auto;
            background-color: #f8fafc;
            padding: 16px;
            border-radius: 8px;
            border: 1px solid #e2e8f0;
        }
        
        .version-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #4f46e5;
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .file-input-wrapper {
            position: relative;
            overflow: hidden;
            display: inline-block;
        }
        
        .file-input-wrapper input[type=file] {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        .dropdown {
            position: relative;
            display: inline-block;
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            border-radius: 0.5rem;
            overflow: hidden;
        }
        
        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            transition: all 0.2s;
        }
        
        .dropdown-content a:hover {
            background-color: #f1f5f9;
        }
        
        .dropdown:hover .dropdown-content {
            display: block;
        }
        
        .json-textarea {
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            resize: vertical;
        }
    </style>
<style>*, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.16 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.relative{position:relative}.inset-0{inset:0px}.z-50{z-index:50}.col-span-full{grid-column:1 / -1}.mx-auto{margin-left:auto;margin-right:auto}.mb-2{margin-bottom:0.5rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-1{margin-left:0.25rem}.mr-1{margin-right:0.25rem}.mr-2{margin-right:0.5rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-16{height:4rem}.h-4{height:1rem}.h-5{height:1.25rem}.h-64{height:16rem}.w-16{width:4rem}.w-4{width:1rem}.w-5{width:1.25rem}.w-full{width:100%}.max-w-4xl{max-width:56rem}.max-w-5xl{max-width:64rem}.max-w-6xl{max-width:72rem}.max-w-md{max-width:28rem}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.flex-col{flex-direction:column}.flex-wrap{flex-wrap:wrap}.items-center{align-items:center}.justify-end{justify-content:flex-end}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-2{gap:0.5rem}.gap-3{gap:0.75rem}.gap-4{gap:1rem}.gap-6{gap:1.5rem}.space-y-3 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.75rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.75rem * var(--tw-space-y-reverse))}.rounded{border-radius:0.25rem}.rounded-lg{border-radius:0.5rem}.rounded-xl{border-radius:0.75rem}.border{border-width:1px}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.bg-black{--tw-bg-opacity:1;background-color:rgb(0 0 0 / var(--tw-bg-opacity, 1))}.bg-blue-600{--tw-bg-opacity:1;background-color:rgb(37 99 235 / var(--tw-bg-opacity, 1))}.bg-emerald-600{--tw-bg-opacity:1;background-color:rgb(5 150 105 / var(--tw-bg-opacity, 1))}.bg-gray-100{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.bg-gray-200{--tw-bg-opacity:1;background-color:rgb(229 231 235 / var(--tw-bg-opacity, 1))}.bg-indigo-600{--tw-bg-opacity:1;background-color:rgb(79 70 229 / var(--tw-bg-opacity, 1))}.bg-purple-600{--tw-bg-opacity:1;background-color:rgb(147 51 234 / var(--tw-bg-opacity, 1))}.bg-red-600{--tw-bg-opacity:1;background-color:rgb(220 38 38 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.bg-opacity-50{--tw-bg-opacity:0.5}.p-4{padding:1rem}.p-2{padding:0.5rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-4{padding-left:1rem;padding-right:1rem}.px-6{padding-left:1.5rem;padding-right:1.5rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.text-center{text-align:center}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-xl{font-size:1.25rem;line-height:1.75rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.text-blue-600{--tw-text-opacity:1;color:rgb(37 99 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-500{--tw-text-opacity:1;color:rgb(107 114 128 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-gray-800{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-green-600{--tw-text-opacity:1;color:rgb(22 163 74 / var(--tw-text-opacity, 1))}.text-red-600{--tw-text-opacity:1;color:rgb(220 38 38 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow{--tw-shadow:0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 1px 3px 0 var(--tw-shadow-color), 0 1px 2px -1px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.hover\:bg-blue-700:hover{--tw-bg-opacity:1;background-color:rgb(29 78 216 / var(--tw-bg-opacity, 1))}.hover\:bg-emerald-700:hover{--tw-bg-opacity:1;background-color:rgb(4 120 87 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-300:hover{--tw-bg-opacity:1;background-color:rgb(209 213 219 / var(--tw-bg-opacity, 1))}.hover\:bg-indigo-700:hover{--tw-bg-opacity:1;background-color:rgb(67 56 202 / var(--tw-bg-opacity, 1))}.hover\:bg-purple-700:hover{--tw-bg-opacity:1;background-color:rgb(126 34 206 / var(--tw-bg-opacity, 1))}.hover\:bg-red-700:hover{--tw-bg-opacity:1;background-color:rgb(185 28 28 / var(--tw-bg-opacity, 1))}@media (min-width: 768px){.md\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.md\:p-8{padding:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}}@media (min-width: 1024px){.lg\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}}</style></head>
<body class="p-4 md:p-8">
    <div class="max-w-6xl mx-auto">
        <header class="text-center mb-8 relative">
            <div class="version-badge">Sürüm 3.0</div>
            <h1 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2">İngilizce Kelime ve Deyim Kartları</h1>
            <p class="text-gray-600">Kendi kelime ve deyimlerinizi ekleyin, öğrenin ve test edin</p>
        </header>
        
        <div class="flex flex-wrap justify-center gap-4 mb-8">
            <button id="flashcardMode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition">Kart Modu</button>
            <button id="quizMode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition">Test Modu</button>
            <button id="addCardBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition">Kart Ekle</button>
            
            <div class="dropdown">
                <button class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center">
                    <span>Veri Yönetimi</span>
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                    </svg>
                </button>
                <div class="dropdown-content">
                    <a href="#" id="exportCardsBtn" class="flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"></path>
                        </svg>
                        Kartları Dışa Aktar
                    </a>
                    <a href="#" id="importCardsBtn" class="flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"></path>
                        </svg>
                        Kartları İçe Aktar
                    </a>
                    <a href="#" id="jsonEditorBtn" class="flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                        </svg>
                        JSON Düzenleyici
                    </a>
                    <a href="#" id="clearCardsBtn" class="flex items-center text-red-600">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
                        </svg>
                        Tüm Kartları Sil
                    </a>
                </div>
            </div>
            
            <button id="viewSourceBtn" class="bg-purple-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-purple-700 transition">Kaynak Kodu Görüntüle</button>
        </div>
        
        <div id="statsBar" class="hidden bg-white p-4 rounded-lg shadow mb-6">
            <div class="flex justify-between items-center">
                <div>
                    <span class="font-medium">Doğru:</span> 
                    <span id="correctCount" class="text-green-600 font-bold">0</span>
                </div>
                <div>
                    <span class="font-medium">Yanlış:</span> 
                    <span id="incorrectCount" class="text-red-600 font-bold">0</span>
                </div>
                <div>
                    <span class="font-medium">Toplam:</span> 
                    <span id="totalCount" class="text-blue-600 font-bold">0</span>
                </div>
            </div>
        </div>
        
        <!-- Flashcard Mode Container -->
        <div id="flashcardContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Empty state message -->
            <div id="emptyState" class="col-span-full empty-state p-8 flex flex-col items-center justify-center text-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path>
                </svg>
                <h3 class="text-xl font-medium text-gray-600 mb-2">Henüz kart eklenmemiş</h3>
                <p class="text-gray-500 mb-4">İngilizce kelime ve deyimlerinizi eklemek için "Kart Ekle" butonuna tıklayın</p>
                <div class="flex flex-wrap gap-3 justify-center">
                    <button id="emptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition">Kart Ekle</button>
                    <button id="emptyStateImportBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition">Kartları İçe Aktar</button>
                </div>
            </div>
        </div>
        
        <!-- Quiz Mode Container -->
        <div id="quizContainer" class="hidden">
            <div id="quizEmptyState" class="empty-state p-8 flex flex-col items-center justify-center text-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path>
                </svg>
                <h3 class="text-xl font-medium text-gray-600 mb-2">Test için yeterli kart yok</h3>
                <p class="text-gray-500 mb-4">Test modu için en az 4 kart eklemeniz gerekiyor</p>
                <button id="quizEmptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition">Kart Ekle</button>
            </div>
            
            <div id="quizContent" class="hidden">
                <div class="bg-white rounded-xl shadow-lg p-6 mb-6">
                    <h2 id="quizQuestion" class="text-2xl font-bold text-center mb-6">Soru yükleniyor...</h2>
                    <div id="quizOptions" class="space-y-3">
                        <!-- Quiz options will be generated here -->
                    </div>
                </div>
                <div class="flex justify-center">
                    <button id="nextQuestion" class="bg-indigo-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-indigo-700 transition">Sonraki Soru</button>
                </div>
            </div>
        </div>
        
        <!-- Add Card Modal -->
        <div id="addCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
            <div class="bg-white rounded-xl p-6 w-full max-w-md">
                <h2 class="text-2xl font-bold mb-4">Yeni Kart Ekle</h2>
                <div class="mb-4">
                    <label class="block text-gray-700 mb-2" for="wordInput">İngilizce Kelime/Deyim:</label>
                    <input id="wordInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="İngilizce kelime veya deyim girin">
                </div>
                <div class="mb-6">
                    <label class="block text-gray-700 mb-2" for="meaningInput">Türkçe Anlamı:</label>
                    <input id="meaningInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="Türkçe anlamını girin">
                </div>
                <div class="flex justify-end gap-3">
                    <button id="cancelAddCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition">İptal</button>
                    <button id="saveCard" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition">Kaydet</button>
                </div>
            </div>
        </div>
        
        <!-- Confirmation Modal for Clear All -->
        <div id="confirmModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50">
            <div class="bg-white rounded-xl p-6 w-full max-w-md">
                <h2 class="text-2xl font-bold mb-4">Tüm Kartları Sil</h2>
                <p class="mb-6 text-gray-700">Tüm kartlarınız silinecek. Bu işlem geri alınamaz. Devam etmek istiyor musunuz?</p>
                <div class="flex justify-end gap-3">
                    <button id="cancelClear" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition">İptal</button>
                    <button id="confirmClear" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition">Evet, Sil</button>
                </div>
            </div>
        </div>
        
        <!-- Confirmation Modal for Delete Single Card -->
        <div id="deleteCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
            <div class="bg-white rounded-xl p-6 w-full max-w-md">
                <h2 class="text-2xl font-bold mb-4">Kartı Sil</h2>
                <p class="mb-2 text-gray-700">Bu kartı silmek istediğinizden emin misiniz?</p>
                <div class="bg-gray-100 p-4 rounded-lg mb-6">
                    <p class="font-medium text-gray-800" id="deleteCardWord">Eyyüphan</p>
                    <p class="text-gray-600" id="deleteCardMeaning">123124124</p>
                </div>
                <div class="flex justify-end gap-3">
                    <button id="cancelDeleteCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition">İptal</button>
                    <button id="confirmDeleteCard" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition">Evet, Sil</button>
                </div>
            </div>
        </div>
        
        <!-- Import File Modal (Hidden File Input) -->
        <input type="file" id="importFileInput" accept=".json" class="hidden">
        
        <!-- JSON Editor Modal -->
        <div id="jsonEditorModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
            <div class="bg-white rounded-xl p-6 w-full max-w-4xl">
                <h2 class="text-2xl font-bold mb-4">JSON Düzenleyici</h2>
                <p class="mb-4 text-gray-700">Kartlarınızı JSON formatında düzenleyebilirsiniz. Aşağıdaki metni kopyalayıp saklayabilir veya düzenleyip geri yükleyebilirsiniz.</p>
                <div class="mb-6">
                    <textarea id="jsonTextarea" class="w-full p-4 border border-gray-300 rounded json-textarea h-64"></textarea>
                </div>
                <div class="flex justify-end gap-3">
                    <button id="copyJsonBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
                        </svg>
                        Kopyala
                    </button>
                    <button id="applyJsonBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition">Uygula</button>
                    <button id="cancelJsonEditor" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition">İptal</button>
                </div>
            </div>
        </div>
        
        <!-- Source Code Modal -->
        <div id="sourceCodeModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden">
            <div class="bg-white rounded-xl p-6 w-full max-w-5xl code-modal">
                <div class="flex justify-between items-center mb-4">
                    <h2 class="text-2xl font-bold">Kaynak Kodu</h2>
                    <div class="flex gap-2">
                        <button id="copySourceCode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition flex items-center">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
                            </svg>
                            Kopyala
                        </button>
                        <button id="closeSourceCode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition">Kapat</button>
                    </div>
                </div>
                <div id="sourceCodeContent" class="code-content">&lt;html lang="tr"&gt;&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;İngilizce Kelime ve Deyim Kartları - Sürüm 3&lt;/title&gt;
    &lt;script src="https://cdn.tailwindcss.com"&gt;&lt;/script&gt;
    &lt;style&gt;
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&amp;display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .flashcard {
            perspective: 1000px;
            height: 200px;
            cursor: pointer;
            transition: transform 0.3s;
            position: relative;
        }
        
        .flashcard:hover {
            transform: translateY(-5px);
        }
        
        .flashcard-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-radius: 1rem;
        }
        
        .flashcard.flipped .flashcard-inner {
            transform: rotateY(180deg);
        }
        
        .flashcard-front, .flashcard-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 1rem;
            padding: 1.5rem;
        }
        
        .flashcard-front {
            background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%);
            color: white;
        }
        
        .flashcard-back {
            background: linear-gradient(135deg, #10b981 0%, #34d399 100%);
            color: #333;
            transform: rotateY(180deg);
        }
        
        .delete-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(239, 68, 68, 0.9);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 10;
            cursor: pointer;
        }
        
        .flashcard:hover .delete-btn {
            opacity: 1;
        }
        
        .delete-btn:hover {
            background-color: rgb(239, 68, 68);
        }
        
        .quiz-option {
            transition: all 0.3s;
        }
        
        .quiz-option:hover {
            transform: translateX(5px);
        }
        
        .quiz-option.correct {
            background-color: #4ade80 !important;
            color: white;
        }
        
        .quiz-option.incorrect {
            background-color: #f87171 !important;
            color: white;
        }
        
        .empty-state {
            border: 2px dashed #cbd5e1;
            border-radius: 1rem;
            transition: all 0.3s;
        }
        
        .empty-state:hover {
            border-color: #94a3b8;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #1e293b;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .toast.show {
            opacity: 1;
        }
        
        .code-modal {
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .code-content {
            white-space: pre-wrap;
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            overflow-x: auto;
            background-color: #f8fafc;
            padding: 16px;
            border-radius: 8px;
            border: 1px solid #e2e8f0;
        }
        
        .version-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #4f46e5;
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .file-input-wrapper {
            position: relative;
            overflow: hidden;
            display: inline-block;
        }
        
        .file-input-wrapper input[type=file] {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        .dropdown {
            position: relative;
            display: inline-block;
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            border-radius: 0.5rem;
            overflow: hidden;
        }
        
        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            transition: all 0.2s;
        }
        
        .dropdown-content a:hover {
            background-color: #f1f5f9;
        }
        
        .dropdown:hover .dropdown-content {
            display: block;
        }
        
        .json-textarea {
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            resize: vertical;
        }
    &lt;/style&gt;
&lt;style&gt;*, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.16 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.relative{position:relative}.inset-0{inset:0px}.z-50{z-index:50}.col-span-full{grid-column:1 / -1}.mx-auto{margin-left:auto;margin-right:auto}.mb-2{margin-bottom:0.5rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-1{margin-left:0.25rem}.mr-1{margin-right:0.25rem}.mr-2{margin-right:0.5rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-16{height:4rem}.h-4{height:1rem}.h-5{height:1.25rem}.h-64{height:16rem}.w-16{width:4rem}.w-4{width:1rem}.w-5{width:1.25rem}.w-full{width:100%}.max-w-4xl{max-width:56rem}.max-w-5xl{max-width:64rem}.max-w-6xl{max-width:72rem}.max-w-md{max-width:28rem}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.flex-col{flex-direction:column}.flex-wrap{flex-wrap:wrap}.items-center{align-items:center}.justify-end{justify-content:flex-end}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-2{gap:0.5rem}.gap-3{gap:0.75rem}.gap-4{gap:1rem}.gap-6{gap:1.5rem}.space-y-3 &gt; :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.75rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.75rem * var(--tw-space-y-reverse))}.rounded{border-radius:0.25rem}.rounded-lg{border-radius:0.5rem}.rounded-xl{border-radius:0.75rem}.border{border-width:1px}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.bg-black{--tw-bg-opacity:1;background-color:rgb(0 0 0 / var(--tw-bg-opacity, 1))}.bg-blue-600{--tw-bg-opacity:1;background-color:rgb(37 99 235 / var(--tw-bg-opacity, 1))}.bg-emerald-600{--tw-bg-opacity:1;background-color:rgb(5 150 105 / var(--tw-bg-opacity, 1))}.bg-gray-100{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.bg-gray-200{--tw-bg-opacity:1;background-color:rgb(229 231 235 / var(--tw-bg-opacity, 1))}.bg-indigo-600{--tw-bg-opacity:1;background-color:rgb(79 70 229 / var(--tw-bg-opacity, 1))}.bg-purple-600{--tw-bg-opacity:1;background-color:rgb(147 51 234 / var(--tw-bg-opacity, 1))}.bg-red-600{--tw-bg-opacity:1;background-color:rgb(220 38 38 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.bg-opacity-50{--tw-bg-opacity:0.5}.p-4{padding:1rem}.p-2{padding:0.5rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-4{padding-left:1rem;padding-right:1rem}.px-6{padding-left:1.5rem;padding-right:1.5rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.text-center{text-align:center}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-xl{font-size:1.25rem;line-height:1.75rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.text-blue-600{--tw-text-opacity:1;color:rgb(37 99 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-500{--tw-text-opacity:1;color:rgb(107 114 128 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-gray-800{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-green-600{--tw-text-opacity:1;color:rgb(22 163 74 / var(--tw-text-opacity, 1))}.text-red-600{--tw-text-opacity:1;color:rgb(220 38 38 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow{--tw-shadow:0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 1px 3px 0 var(--tw-shadow-color), 0 1px 2px -1px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.hover\:bg-blue-700:hover{--tw-bg-opacity:1;background-color:rgb(29 78 216 / var(--tw-bg-opacity, 1))}.hover\:bg-emerald-700:hover{--tw-bg-opacity:1;background-color:rgb(4 120 87 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-300:hover{--tw-bg-opacity:1;background-color:rgb(209 213 219 / var(--tw-bg-opacity, 1))}.hover\:bg-indigo-700:hover{--tw-bg-opacity:1;background-color:rgb(67 56 202 / var(--tw-bg-opacity, 1))}.hover\:bg-purple-700:hover{--tw-bg-opacity:1;background-color:rgb(126 34 206 / var(--tw-bg-opacity, 1))}.hover\:bg-red-700:hover{--tw-bg-opacity:1;background-color:rgb(185 28 28 / var(--tw-bg-opacity, 1))}@media (min-width: 768px){.md\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.md\:p-8{padding:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}}@media (min-width: 1024px){.lg\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}}&lt;/style&gt;&lt;/head&gt;
&lt;body class="p-4 md:p-8"&gt;
    &lt;div class="max-w-6xl mx-auto"&gt;
        &lt;header class="text-center mb-8 relative"&gt;
            &lt;div class="version-badge"&gt;Sürüm 3.0&lt;/div&gt;
            &lt;h1 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2"&gt;İngilizce Kelime ve Deyim Kartları&lt;/h1&gt;
            &lt;p class="text-gray-600"&gt;Kendi kelime ve deyimlerinizi ekleyin, öğrenin ve test edin&lt;/p&gt;
        &lt;/header&gt;
        
        &lt;div class="flex flex-wrap justify-center gap-4 mb-8"&gt;
            &lt;button id="flashcardMode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&gt;Kart Modu&lt;/button&gt;
            &lt;button id="quizMode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&gt;Test Modu&lt;/button&gt;
            &lt;button id="addCardBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&gt;Kart Ekle&lt;/button&gt;
            
            &lt;div class="dropdown"&gt;
                &lt;button class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&gt;
                    &lt;span&gt;Veri Yönetimi&lt;/span&gt;
                    &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                        &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"&gt;&lt;/path&gt;
                    &lt;/svg&gt;
                &lt;/button&gt;
                &lt;div class="dropdown-content"&gt;
                    &lt;a href="#" id="exportCardsBtn" class="flex items-center"&gt;
                        &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                            &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"&gt;&lt;/path&gt;
                        &lt;/svg&gt;
                        Kartları Dışa Aktar
                    &lt;/a&gt;
                    &lt;a href="#" id="importCardsBtn" class="flex items-center"&gt;
                        &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                            &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"&gt;&lt;/path&gt;
                        &lt;/svg&gt;
                        Kartları İçe Aktar
                    &lt;/a&gt;
                    &lt;a href="#" id="jsonEditorBtn" class="flex items-center"&gt;
                        &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                            &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"&gt;&lt;/path&gt;
                        &lt;/svg&gt;
                        JSON Düzenleyici
                    &lt;/a&gt;
                    &lt;a href="#" id="clearCardsBtn" class="flex items-center text-red-600"&gt;
                        &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                            &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"&gt;&lt;/path&gt;
                        &lt;/svg&gt;
                        Tüm Kartları Sil
                    &lt;/a&gt;
                &lt;/div&gt;
            &lt;/div&gt;
            
            &lt;button id="viewSourceBtn" class="bg-purple-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-purple-700 transition"&gt;Kaynak Kodu Görüntüle&lt;/button&gt;
        &lt;/div&gt;
        
        &lt;div id="statsBar" class="hidden bg-white p-4 rounded-lg shadow mb-6"&gt;
            &lt;div class="flex justify-between items-center"&gt;
                &lt;div&gt;
                    &lt;span class="font-medium"&gt;Doğru:&lt;/span&gt; 
                    &lt;span id="correctCount" class="text-green-600 font-bold"&gt;0&lt;/span&gt;
                &lt;/div&gt;
                &lt;div&gt;
                    &lt;span class="font-medium"&gt;Yanlış:&lt;/span&gt; 
                    &lt;span id="incorrectCount" class="text-red-600 font-bold"&gt;0&lt;/span&gt;
                &lt;/div&gt;
                &lt;div&gt;
                    &lt;span class="font-medium"&gt;Toplam:&lt;/span&gt; 
                    &lt;span id="totalCount" class="text-blue-600 font-bold"&gt;0&lt;/span&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Flashcard Mode Container --&gt;
        &lt;div id="flashcardContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"&gt;
            &lt;!-- Empty state message --&gt;
            &lt;div id="emptyState" class="col-span-full empty-state p-8 flex flex-col items-center justify-center text-center"&gt;
                &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                    &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"&gt;&lt;/path&gt;
                &lt;/svg&gt;
                &lt;h3 class="text-xl font-medium text-gray-600 mb-2"&gt;Henüz kart eklenmemiş&lt;/h3&gt;
                &lt;p class="text-gray-500 mb-4"&gt;İngilizce kelime ve deyimlerinizi eklemek için "Kart Ekle" butonuna tıklayın&lt;/p&gt;
                &lt;div class="flex flex-wrap gap-3 justify-center"&gt;
                    &lt;button id="emptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&gt;Kart Ekle&lt;/button&gt;
                    &lt;button id="emptyStateImportBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition"&gt;Kartları İçe Aktar&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Quiz Mode Container --&gt;
        &lt;div id="quizContainer" class="hidden"&gt;
            &lt;div id="quizEmptyState" class="empty-state p-8 flex flex-col items-center justify-center text-center"&gt;
                &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                    &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"&gt;&lt;/path&gt;
                &lt;/svg&gt;
                &lt;h3 class="text-xl font-medium text-gray-600 mb-2"&gt;Test için yeterli kart yok&lt;/h3&gt;
                &lt;p class="text-gray-500 mb-4"&gt;Test modu için en az 4 kart eklemeniz gerekiyor&lt;/p&gt;
                &lt;button id="quizEmptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&gt;Kart Ekle&lt;/button&gt;
            &lt;/div&gt;
            
            &lt;div id="quizContent" class="hidden"&gt;
                &lt;div class="bg-white rounded-xl shadow-lg p-6 mb-6"&gt;
                    &lt;h2 id="quizQuestion" class="text-2xl font-bold text-center mb-6"&gt;Soru yükleniyor...&lt;/h2&gt;
                    &lt;div id="quizOptions" class="space-y-3"&gt;
                        &lt;!-- Quiz options will be generated here --&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
                &lt;div class="flex justify-center"&gt;
                    &lt;button id="nextQuestion" class="bg-indigo-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&gt;Sonraki Soru&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Add Card Modal --&gt;
        &lt;div id="addCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&gt;
            &lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&gt;
                &lt;h2 class="text-2xl font-bold mb-4"&gt;Yeni Kart Ekle&lt;/h2&gt;
                &lt;div class="mb-4"&gt;
                    &lt;label class="block text-gray-700 mb-2" for="wordInput"&gt;İngilizce Kelime/Deyim:&lt;/label&gt;
                    &lt;input id="wordInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="İngilizce kelime veya deyim girin"&gt;
                &lt;/div&gt;
                &lt;div class="mb-6"&gt;
                    &lt;label class="block text-gray-700 mb-2" for="meaningInput"&gt;Türkçe Anlamı:&lt;/label&gt;
                    &lt;input id="meaningInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="Türkçe anlamını girin"&gt;
                &lt;/div&gt;
                &lt;div class="flex justify-end gap-3"&gt;
                    &lt;button id="cancelAddCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&gt;İptal&lt;/button&gt;
                    &lt;button id="saveCard" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&gt;Kaydet&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Confirmation Modal for Clear All --&gt;
        &lt;div id="confirmModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50"&gt;
            &lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&gt;
                &lt;h2 class="text-2xl font-bold mb-4"&gt;Tüm Kartları Sil&lt;/h2&gt;
                &lt;p class="mb-6 text-gray-700"&gt;Tüm kartlarınız silinecek. Bu işlem geri alınamaz. Devam etmek istiyor musunuz?&lt;/p&gt;
                &lt;div class="flex justify-end gap-3"&gt;
                    &lt;button id="cancelClear" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&gt;İptal&lt;/button&gt;
                    &lt;button id="confirmClear" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&gt;Evet, Sil&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Confirmation Modal for Delete Single Card --&gt;
        &lt;div id="deleteCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&gt;
            &lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&gt;
                &lt;h2 class="text-2xl font-bold mb-4"&gt;Kartı Sil&lt;/h2&gt;
                &lt;p class="mb-2 text-gray-700"&gt;Bu kartı silmek istediğinizden emin misiniz?&lt;/p&gt;
                &lt;div class="bg-gray-100 p-4 rounded-lg mb-6"&gt;
                    &lt;p class="font-medium text-gray-800" id="deleteCardWord"&gt;Eyyüphan&lt;/p&gt;
                    &lt;p class="text-gray-600" id="deleteCardMeaning"&gt;123124124&lt;/p&gt;
                &lt;/div&gt;
                &lt;div class="flex justify-end gap-3"&gt;
                    &lt;button id="cancelDeleteCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&gt;İptal&lt;/button&gt;
                    &lt;button id="confirmDeleteCard" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&gt;Evet, Sil&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Import File Modal (Hidden File Input) --&gt;
        &lt;input type="file" id="importFileInput" accept=".json" class="hidden"&gt;
        
        &lt;!-- JSON Editor Modal --&gt;
        &lt;div id="jsonEditorModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&gt;
            &lt;div class="bg-white rounded-xl p-6 w-full max-w-4xl"&gt;
                &lt;h2 class="text-2xl font-bold mb-4"&gt;JSON Düzenleyici&lt;/h2&gt;
                &lt;p class="mb-4 text-gray-700"&gt;Kartlarınızı JSON formatında düzenleyebilirsiniz. Aşağıdaki metni kopyalayıp saklayabilir veya düzenleyip geri yükleyebilirsiniz.&lt;/p&gt;
                &lt;div class="mb-6"&gt;
                    &lt;textarea id="jsonTextarea" class="w-full p-4 border border-gray-300 rounded json-textarea h-64"&gt;&lt;/textarea&gt;
                &lt;/div&gt;
                &lt;div class="flex justify-end gap-3"&gt;
                    &lt;button id="copyJsonBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&gt;
                        &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                            &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&gt;&lt;/path&gt;
                        &lt;/svg&gt;
                        Kopyala
                    &lt;/button&gt;
                    &lt;button id="applyJsonBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&gt;Uygula&lt;/button&gt;
                    &lt;button id="cancelJsonEditor" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&gt;İptal&lt;/button&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Source Code Modal --&gt;
        &lt;div id="sourceCodeModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&gt;
            &lt;div class="bg-white rounded-xl p-6 w-full max-w-5xl code-modal"&gt;
                &lt;div class="flex justify-between items-center mb-4"&gt;
                    &lt;h2 class="text-2xl font-bold"&gt;Kaynak Kodu&lt;/h2&gt;
                    &lt;div class="flex gap-2"&gt;
                        &lt;button id="copySourceCode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition flex items-center"&gt;
                            &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                                &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&gt;&lt;/path&gt;
                            &lt;/svg&gt;
                            Kopyala
                        &lt;/button&gt;
                        &lt;button id="closeSourceCode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&gt;Kapat&lt;/button&gt;
                    &lt;/div&gt;
                &lt;/div&gt;
                &lt;div id="sourceCodeContent" class="code-content"&gt;&amp;lt;html lang="tr"&amp;gt;&amp;lt;head&amp;gt;
    &amp;lt;meta charset="UTF-8"&amp;gt;
    &amp;lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&amp;gt;
    &amp;lt;title&amp;gt;İngilizce Kelime ve Deyim Kartları - Sürüm 3&amp;lt;/title&amp;gt;
    &amp;lt;script src="https://cdn.tailwindcss.com"&amp;gt;&amp;lt;/script&amp;gt;
    &amp;lt;style&amp;gt;
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&amp;amp;display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .flashcard {
            perspective: 1000px;
            height: 200px;
            cursor: pointer;
            transition: transform 0.3s;
            position: relative;
        }
        
        .flashcard:hover {
            transform: translateY(-5px);
        }
        
        .flashcard-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-radius: 1rem;
        }
        
        .flashcard.flipped .flashcard-inner {
            transform: rotateY(180deg);
        }
        
        .flashcard-front, .flashcard-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 1rem;
            padding: 1.5rem;
        }
        
        .flashcard-front {
            background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%);
            color: white;
        }
        
        .flashcard-back {
            background: linear-gradient(135deg, #10b981 0%, #34d399 100%);
            color: #333;
            transform: rotateY(180deg);
        }
        
        .delete-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(239, 68, 68, 0.9);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 10;
            cursor: pointer;
        }
        
        .flashcard:hover .delete-btn {
            opacity: 1;
        }
        
        .delete-btn:hover {
            background-color: rgb(239, 68, 68);
        }
        
        .quiz-option {
            transition: all 0.3s;
        }
        
        .quiz-option:hover {
            transform: translateX(5px);
        }
        
        .quiz-option.correct {
            background-color: #4ade80 !important;
            color: white;
        }
        
        .quiz-option.incorrect {
            background-color: #f87171 !important;
            color: white;
        }
        
        .empty-state {
            border: 2px dashed #cbd5e1;
            border-radius: 1rem;
            transition: all 0.3s;
        }
        
        .empty-state:hover {
            border-color: #94a3b8;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #1e293b;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .toast.show {
            opacity: 1;
        }
        
        .code-modal {
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .code-content {
            white-space: pre-wrap;
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            overflow-x: auto;
            background-color: #f8fafc;
            padding: 16px;
            border-radius: 8px;
            border: 1px solid #e2e8f0;
        }
        
        .version-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #4f46e5;
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .file-input-wrapper {
            position: relative;
            overflow: hidden;
            display: inline-block;
        }
        
        .file-input-wrapper input[type=file] {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        .dropdown {
            position: relative;
            display: inline-block;
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            border-radius: 0.5rem;
            overflow: hidden;
        }
        
        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            transition: all 0.2s;
        }
        
        .dropdown-content a:hover {
            background-color: #f1f5f9;
        }
        
        .dropdown:hover .dropdown-content {
            display: block;
        }
        
        .json-textarea {
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            resize: vertical;
        }
    &amp;lt;/style&amp;gt;
&amp;lt;style&amp;gt;*, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.16 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.relative{position:relative}.inset-0{inset:0px}.z-50{z-index:50}.col-span-full{grid-column:1 / -1}.mx-auto{margin-left:auto;margin-right:auto}.mb-2{margin-bottom:0.5rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-1{margin-left:0.25rem}.mr-1{margin-right:0.25rem}.mr-2{margin-right:0.5rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-16{height:4rem}.h-4{height:1rem}.h-5{height:1.25rem}.h-64{height:16rem}.w-16{width:4rem}.w-4{width:1rem}.w-5{width:1.25rem}.w-full{width:100%}.max-w-4xl{max-width:56rem}.max-w-5xl{max-width:64rem}.max-w-6xl{max-width:72rem}.max-w-md{max-width:28rem}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.flex-col{flex-direction:column}.flex-wrap{flex-wrap:wrap}.items-center{align-items:center}.justify-end{justify-content:flex-end}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-2{gap:0.5rem}.gap-3{gap:0.75rem}.gap-4{gap:1rem}.gap-6{gap:1.5rem}.space-y-3 &amp;gt; :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.75rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.75rem * var(--tw-space-y-reverse))}.rounded{border-radius:0.25rem}.rounded-lg{border-radius:0.5rem}.rounded-xl{border-radius:0.75rem}.border{border-width:1px}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.bg-black{--tw-bg-opacity:1;background-color:rgb(0 0 0 / var(--tw-bg-opacity, 1))}.bg-blue-600{--tw-bg-opacity:1;background-color:rgb(37 99 235 / var(--tw-bg-opacity, 1))}.bg-emerald-600{--tw-bg-opacity:1;background-color:rgb(5 150 105 / var(--tw-bg-opacity, 1))}.bg-gray-100{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.bg-gray-200{--tw-bg-opacity:1;background-color:rgb(229 231 235 / var(--tw-bg-opacity, 1))}.bg-indigo-600{--tw-bg-opacity:1;background-color:rgb(79 70 229 / var(--tw-bg-opacity, 1))}.bg-purple-600{--tw-bg-opacity:1;background-color:rgb(147 51 234 / var(--tw-bg-opacity, 1))}.bg-red-600{--tw-bg-opacity:1;background-color:rgb(220 38 38 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.bg-opacity-50{--tw-bg-opacity:0.5}.p-4{padding:1rem}.p-2{padding:0.5rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-4{padding-left:1rem;padding-right:1rem}.px-6{padding-left:1.5rem;padding-right:1.5rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.text-center{text-align:center}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-xl{font-size:1.25rem;line-height:1.75rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.text-blue-600{--tw-text-opacity:1;color:rgb(37 99 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-500{--tw-text-opacity:1;color:rgb(107 114 128 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-gray-800{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-green-600{--tw-text-opacity:1;color:rgb(22 163 74 / var(--tw-text-opacity, 1))}.text-red-600{--tw-text-opacity:1;color:rgb(220 38 38 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow{--tw-shadow:0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 1px 3px 0 var(--tw-shadow-color), 0 1px 2px -1px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.hover\:bg-blue-700:hover{--tw-bg-opacity:1;background-color:rgb(29 78 216 / var(--tw-bg-opacity, 1))}.hover\:bg-emerald-700:hover{--tw-bg-opacity:1;background-color:rgb(4 120 87 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-300:hover{--tw-bg-opacity:1;background-color:rgb(209 213 219 / var(--tw-bg-opacity, 1))}.hover\:bg-indigo-700:hover{--tw-bg-opacity:1;background-color:rgb(67 56 202 / var(--tw-bg-opacity, 1))}.hover\:bg-purple-700:hover{--tw-bg-opacity:1;background-color:rgb(126 34 206 / var(--tw-bg-opacity, 1))}.hover\:bg-red-700:hover{--tw-bg-opacity:1;background-color:rgb(185 28 28 / var(--tw-bg-opacity, 1))}@media (min-width: 768px){.md\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.md\:p-8{padding:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}}@media (min-width: 1024px){.lg\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}}&amp;lt;/style&amp;gt;&amp;lt;/head&amp;gt;
&amp;lt;body class="p-4 md:p-8"&amp;gt;
    &amp;lt;div class="max-w-6xl mx-auto"&amp;gt;
        &amp;lt;header class="text-center mb-8 relative"&amp;gt;
            &amp;lt;div class="version-badge"&amp;gt;Sürüm 3.0&amp;lt;/div&amp;gt;
            &amp;lt;h1 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2"&amp;gt;İngilizce Kelime ve Deyim Kartları&amp;lt;/h1&amp;gt;
            &amp;lt;p class="text-gray-600"&amp;gt;Kendi kelime ve deyimlerinizi ekleyin, öğrenin ve test edin&amp;lt;/p&amp;gt;
        &amp;lt;/header&amp;gt;
        
        &amp;lt;div class="flex flex-wrap justify-center gap-4 mb-8"&amp;gt;
            &amp;lt;button id="flashcardMode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;gt;Kart Modu&amp;lt;/button&amp;gt;
            &amp;lt;button id="quizMode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;gt;Test Modu&amp;lt;/button&amp;gt;
            &amp;lt;button id="addCardBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;gt;Kart Ekle&amp;lt;/button&amp;gt;
            
            &amp;lt;div class="dropdown"&amp;gt;
                &amp;lt;button class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&amp;gt;
                    &amp;lt;span&amp;gt;Veri Yönetimi&amp;lt;/span&amp;gt;
                    &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                        &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"&amp;gt;&amp;lt;/path&amp;gt;
                    &amp;lt;/svg&amp;gt;
                &amp;lt;/button&amp;gt;
                &amp;lt;div class="dropdown-content"&amp;gt;
                    &amp;lt;a href="#" id="exportCardsBtn" class="flex items-center"&amp;gt;
                        &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                            &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"&amp;gt;&amp;lt;/path&amp;gt;
                        &amp;lt;/svg&amp;gt;
                        Kartları Dışa Aktar
                    &amp;lt;/a&amp;gt;
                    &amp;lt;a href="#" id="importCardsBtn" class="flex items-center"&amp;gt;
                        &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                            &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"&amp;gt;&amp;lt;/path&amp;gt;
                        &amp;lt;/svg&amp;gt;
                        Kartları İçe Aktar
                    &amp;lt;/a&amp;gt;
                    &amp;lt;a href="#" id="jsonEditorBtn" class="flex items-center"&amp;gt;
                        &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                            &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"&amp;gt;&amp;lt;/path&amp;gt;
                        &amp;lt;/svg&amp;gt;
                        JSON Düzenleyici
                    &amp;lt;/a&amp;gt;
                    &amp;lt;a href="#" id="clearCardsBtn" class="flex items-center text-red-600"&amp;gt;
                        &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                            &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"&amp;gt;&amp;lt;/path&amp;gt;
                        &amp;lt;/svg&amp;gt;
                        Tüm Kartları Sil
                    &amp;lt;/a&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
            
            &amp;lt;button id="viewSourceBtn" class="bg-purple-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-purple-700 transition"&amp;gt;Kaynak Kodu Görüntüle&amp;lt;/button&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;div id="statsBar" class="hidden bg-white p-4 rounded-lg shadow mb-6"&amp;gt;
            &amp;lt;div class="flex justify-between items-center"&amp;gt;
                &amp;lt;div&amp;gt;
                    &amp;lt;span class="font-medium"&amp;gt;Doğru:&amp;lt;/span&amp;gt; 
                    &amp;lt;span id="correctCount" class="text-green-600 font-bold"&amp;gt;0&amp;lt;/span&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div&amp;gt;
                    &amp;lt;span class="font-medium"&amp;gt;Yanlış:&amp;lt;/span&amp;gt; 
                    &amp;lt;span id="incorrectCount" class="text-red-600 font-bold"&amp;gt;0&amp;lt;/span&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div&amp;gt;
                    &amp;lt;span class="font-medium"&amp;gt;Toplam:&amp;lt;/span&amp;gt; 
                    &amp;lt;span id="totalCount" class="text-blue-600 font-bold"&amp;gt;0&amp;lt;/span&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Flashcard Mode Container --&amp;gt;
        &amp;lt;div id="flashcardContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"&amp;gt;
            &amp;lt;!-- Empty state message --&amp;gt;
            &amp;lt;div id="emptyState" class="col-span-full empty-state p-8 flex flex-col items-center justify-center text-center"&amp;gt;
                &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                    &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"&amp;gt;&amp;lt;/path&amp;gt;
                &amp;lt;/svg&amp;gt;
                &amp;lt;h3 class="text-xl font-medium text-gray-600 mb-2"&amp;gt;Henüz kart eklenmemiş&amp;lt;/h3&amp;gt;
                &amp;lt;p class="text-gray-500 mb-4"&amp;gt;İngilizce kelime ve deyimlerinizi eklemek için "Kart Ekle" butonuna tıklayın&amp;lt;/p&amp;gt;
                &amp;lt;div class="flex flex-wrap gap-3 justify-center"&amp;gt;
                    &amp;lt;button id="emptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;gt;Kart Ekle&amp;lt;/button&amp;gt;
                    &amp;lt;button id="emptyStateImportBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition"&amp;gt;Kartları İçe Aktar&amp;lt;/button&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Quiz Mode Container --&amp;gt;
        &amp;lt;div id="quizContainer" class="hidden"&amp;gt;
            &amp;lt;div id="quizEmptyState" class="empty-state p-8 flex flex-col items-center justify-center text-center"&amp;gt;
                &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                    &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"&amp;gt;&amp;lt;/path&amp;gt;
                &amp;lt;/svg&amp;gt;
                &amp;lt;h3 class="text-xl font-medium text-gray-600 mb-2"&amp;gt;Test için yeterli kart yok&amp;lt;/h3&amp;gt;
                &amp;lt;p class="text-gray-500 mb-4"&amp;gt;Test modu için en az 4 kart eklemeniz gerekiyor&amp;lt;/p&amp;gt;
                &amp;lt;button id="quizEmptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;gt;Kart Ekle&amp;lt;/button&amp;gt;
            &amp;lt;/div&amp;gt;
            
            &amp;lt;div id="quizContent" class="hidden"&amp;gt;
                &amp;lt;div class="bg-white rounded-xl shadow-lg p-6 mb-6"&amp;gt;
                    &amp;lt;h2 id="quizQuestion" class="text-2xl font-bold text-center mb-6"&amp;gt;Soru yükleniyor...&amp;lt;/h2&amp;gt;
                    &amp;lt;div id="quizOptions" class="space-y-3"&amp;gt;
                        &amp;lt;!-- Quiz options will be generated here --&amp;gt;
                    &amp;lt;/div&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div class="flex justify-center"&amp;gt;
                    &amp;lt;button id="nextQuestion" class="bg-indigo-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;gt;Sonraki Soru&amp;lt;/button&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Add Card Modal --&amp;gt;
        &amp;lt;div id="addCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;gt;
            &amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;gt;
                &amp;lt;h2 class="text-2xl font-bold mb-4"&amp;gt;Yeni Kart Ekle&amp;lt;/h2&amp;gt;
                &amp;lt;div class="mb-4"&amp;gt;
                    &amp;lt;label class="block text-gray-700 mb-2" for="wordInput"&amp;gt;İngilizce Kelime/Deyim:&amp;lt;/label&amp;gt;
                    &amp;lt;input id="wordInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="İngilizce kelime veya deyim girin"&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div class="mb-6"&amp;gt;
                    &amp;lt;label class="block text-gray-700 mb-2" for="meaningInput"&amp;gt;Türkçe Anlamı:&amp;lt;/label&amp;gt;
                    &amp;lt;input id="meaningInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="Türkçe anlamını girin"&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div class="flex justify-end gap-3"&amp;gt;
                    &amp;lt;button id="cancelAddCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;gt;İptal&amp;lt;/button&amp;gt;
                    &amp;lt;button id="saveCard" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;gt;Kaydet&amp;lt;/button&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Confirmation Modal for Clear All --&amp;gt;
        &amp;lt;div id="confirmModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50"&amp;gt;
            &amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;gt;
                &amp;lt;h2 class="text-2xl font-bold mb-4"&amp;gt;Tüm Kartları Sil&amp;lt;/h2&amp;gt;
                &amp;lt;p class="mb-6 text-gray-700"&amp;gt;Tüm kartlarınız silinecek. Bu işlem geri alınamaz. Devam etmek istiyor musunuz?&amp;lt;/p&amp;gt;
                &amp;lt;div class="flex justify-end gap-3"&amp;gt;
                    &amp;lt;button id="cancelClear" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;gt;İptal&amp;lt;/button&amp;gt;
                    &amp;lt;button id="confirmClear" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&amp;gt;Evet, Sil&amp;lt;/button&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Confirmation Modal for Delete Single Card --&amp;gt;
        &amp;lt;div id="deleteCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;gt;
            &amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;gt;
                &amp;lt;h2 class="text-2xl font-bold mb-4"&amp;gt;Kartı Sil&amp;lt;/h2&amp;gt;
                &amp;lt;p class="mb-2 text-gray-700"&amp;gt;Bu kartı silmek istediğinizden emin misiniz?&amp;lt;/p&amp;gt;
                &amp;lt;div class="bg-gray-100 p-4 rounded-lg mb-6"&amp;gt;
                    &amp;lt;p class="font-medium text-gray-800" id="deleteCardWord"&amp;gt;Eyyüphan&amp;lt;/p&amp;gt;
                    &amp;lt;p class="text-gray-600" id="deleteCardMeaning"&amp;gt;123124124&amp;lt;/p&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div class="flex justify-end gap-3"&amp;gt;
                    &amp;lt;button id="cancelDeleteCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;gt;İptal&amp;lt;/button&amp;gt;
                    &amp;lt;button id="confirmDeleteCard" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&amp;gt;Evet, Sil&amp;lt;/button&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Import File Modal (Hidden File Input) --&amp;gt;
        &amp;lt;input type="file" id="importFileInput" accept=".json" class="hidden"&amp;gt;
        
        &amp;lt;!-- JSON Editor Modal --&amp;gt;
        &amp;lt;div id="jsonEditorModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;gt;
            &amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-4xl"&amp;gt;
                &amp;lt;h2 class="text-2xl font-bold mb-4"&amp;gt;JSON Düzenleyici&amp;lt;/h2&amp;gt;
                &amp;lt;p class="mb-4 text-gray-700"&amp;gt;Kartlarınızı JSON formatında düzenleyebilirsiniz. Aşağıdaki metni kopyalayıp saklayabilir veya düzenleyip geri yükleyebilirsiniz.&amp;lt;/p&amp;gt;
                &amp;lt;div class="mb-6"&amp;gt;
                    &amp;lt;textarea id="jsonTextarea" class="w-full p-4 border border-gray-300 rounded json-textarea h-64"&amp;gt;&amp;lt;/textarea&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div class="flex justify-end gap-3"&amp;gt;
                    &amp;lt;button id="copyJsonBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&amp;gt;
                        &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                            &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&amp;gt;&amp;lt;/path&amp;gt;
                        &amp;lt;/svg&amp;gt;
                        Kopyala
                    &amp;lt;/button&amp;gt;
                    &amp;lt;button id="applyJsonBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;gt;Uygula&amp;lt;/button&amp;gt;
                    &amp;lt;button id="cancelJsonEditor" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;gt;İptal&amp;lt;/button&amp;gt;
                &amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Source Code Modal --&amp;gt;
        &amp;lt;div id="sourceCodeModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;gt;
            &amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-5xl code-modal"&amp;gt;
                &amp;lt;div class="flex justify-between items-center mb-4"&amp;gt;
                    &amp;lt;h2 class="text-2xl font-bold"&amp;gt;Kaynak Kodu&amp;lt;/h2&amp;gt;
                    &amp;lt;div class="flex gap-2"&amp;gt;
                        &amp;lt;button id="copySourceCode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition flex items-center"&amp;gt;
                            &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                                &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&amp;gt;&amp;lt;/path&amp;gt;
                            &amp;lt;/svg&amp;gt;
                            Kopyala
                        &amp;lt;/button&amp;gt;
                        &amp;lt;button id="closeSourceCode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;gt;Kapat&amp;lt;/button&amp;gt;
                    &amp;lt;/div&amp;gt;
                &amp;lt;/div&amp;gt;
                &amp;lt;div id="sourceCodeContent" class="code-content"&amp;gt;&amp;amp;lt;html lang="tr"&amp;amp;gt;&amp;amp;lt;head&amp;amp;gt;
    &amp;amp;lt;meta charset="UTF-8"&amp;amp;gt;
    &amp;amp;lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&amp;amp;gt;
    &amp;amp;lt;title&amp;amp;gt;İngilizce Kelime ve Deyim Kartları - Sürüm 3&amp;amp;lt;/title&amp;amp;gt;
    &amp;amp;lt;script src="https://cdn.tailwindcss.com"&amp;amp;gt;&amp;amp;lt;/script&amp;amp;gt;
    &amp;amp;lt;style&amp;amp;gt;
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&amp;amp;amp;display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .flashcard {
            perspective: 1000px;
            height: 200px;
            cursor: pointer;
            transition: transform 0.3s;
            position: relative;
        }
        
        .flashcard:hover {
            transform: translateY(-5px);
        }
        
        .flashcard-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-radius: 1rem;
        }
        
        .flashcard.flipped .flashcard-inner {
            transform: rotateY(180deg);
        }
        
        .flashcard-front, .flashcard-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 1rem;
            padding: 1.5rem;
        }
        
        .flashcard-front {
            background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%);
            color: white;
        }
        
        .flashcard-back {
            background: linear-gradient(135deg, #10b981 0%, #34d399 100%);
            color: #333;
            transform: rotateY(180deg);
        }
        
        .delete-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(239, 68, 68, 0.9);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 10;
            cursor: pointer;
        }
        
        .flashcard:hover .delete-btn {
            opacity: 1;
        }
        
        .delete-btn:hover {
            background-color: rgb(239, 68, 68);
        }
        
        .quiz-option {
            transition: all 0.3s;
        }
        
        .quiz-option:hover {
            transform: translateX(5px);
        }
        
        .quiz-option.correct {
            background-color: #4ade80 !important;
            color: white;
        }
        
        .quiz-option.incorrect {
            background-color: #f87171 !important;
            color: white;
        }
        
        .empty-state {
            border: 2px dashed #cbd5e1;
            border-radius: 1rem;
            transition: all 0.3s;
        }
        
        .empty-state:hover {
            border-color: #94a3b8;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #1e293b;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .toast.show {
            opacity: 1;
        }
        
        .code-modal {
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .code-content {
            white-space: pre-wrap;
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            overflow-x: auto;
            background-color: #f8fafc;
            padding: 16px;
            border-radius: 8px;
            border: 1px solid #e2e8f0;
        }
        
        .version-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #4f46e5;
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .file-input-wrapper {
            position: relative;
            overflow: hidden;
            display: inline-block;
        }
        
        .file-input-wrapper input[type=file] {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        .dropdown {
            position: relative;
            display: inline-block;
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            border-radius: 0.5rem;
            overflow: hidden;
        }
        
        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            transition: all 0.2s;
        }
        
        .dropdown-content a:hover {
            background-color: #f1f5f9;
        }
        
        .dropdown:hover .dropdown-content {
            display: block;
        }
        
        .json-textarea {
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            resize: vertical;
        }
    &amp;amp;lt;/style&amp;amp;gt;
&amp;amp;lt;style&amp;amp;gt;*, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.16 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.relative{position:relative}.inset-0{inset:0px}.z-50{z-index:50}.col-span-full{grid-column:1 / -1}.mx-auto{margin-left:auto;margin-right:auto}.mb-2{margin-bottom:0.5rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-1{margin-left:0.25rem}.mr-1{margin-right:0.25rem}.mr-2{margin-right:0.5rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-16{height:4rem}.h-4{height:1rem}.h-5{height:1.25rem}.h-64{height:16rem}.w-16{width:4rem}.w-4{width:1rem}.w-5{width:1.25rem}.w-full{width:100%}.max-w-4xl{max-width:56rem}.max-w-5xl{max-width:64rem}.max-w-6xl{max-width:72rem}.max-w-md{max-width:28rem}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.flex-col{flex-direction:column}.flex-wrap{flex-wrap:wrap}.items-center{align-items:center}.justify-end{justify-content:flex-end}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-2{gap:0.5rem}.gap-3{gap:0.75rem}.gap-4{gap:1rem}.gap-6{gap:1.5rem}.space-y-3 &amp;amp;gt; :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.75rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.75rem * var(--tw-space-y-reverse))}.rounded{border-radius:0.25rem}.rounded-lg{border-radius:0.5rem}.rounded-xl{border-radius:0.75rem}.border{border-width:1px}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.bg-black{--tw-bg-opacity:1;background-color:rgb(0 0 0 / var(--tw-bg-opacity, 1))}.bg-blue-600{--tw-bg-opacity:1;background-color:rgb(37 99 235 / var(--tw-bg-opacity, 1))}.bg-emerald-600{--tw-bg-opacity:1;background-color:rgb(5 150 105 / var(--tw-bg-opacity, 1))}.bg-gray-100{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.bg-gray-200{--tw-bg-opacity:1;background-color:rgb(229 231 235 / var(--tw-bg-opacity, 1))}.bg-indigo-600{--tw-bg-opacity:1;background-color:rgb(79 70 229 / var(--tw-bg-opacity, 1))}.bg-purple-600{--tw-bg-opacity:1;background-color:rgb(147 51 234 / var(--tw-bg-opacity, 1))}.bg-red-600{--tw-bg-opacity:1;background-color:rgb(220 38 38 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.bg-opacity-50{--tw-bg-opacity:0.5}.p-4{padding:1rem}.p-2{padding:0.5rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-4{padding-left:1rem;padding-right:1rem}.px-6{padding-left:1.5rem;padding-right:1.5rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.text-center{text-align:center}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-xl{font-size:1.25rem;line-height:1.75rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.text-blue-600{--tw-text-opacity:1;color:rgb(37 99 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-500{--tw-text-opacity:1;color:rgb(107 114 128 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-gray-800{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-green-600{--tw-text-opacity:1;color:rgb(22 163 74 / var(--tw-text-opacity, 1))}.text-red-600{--tw-text-opacity:1;color:rgb(220 38 38 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow{--tw-shadow:0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 1px 3px 0 var(--tw-shadow-color), 0 1px 2px -1px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.hover\:bg-blue-700:hover{--tw-bg-opacity:1;background-color:rgb(29 78 216 / var(--tw-bg-opacity, 1))}.hover\:bg-emerald-700:hover{--tw-bg-opacity:1;background-color:rgb(4 120 87 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-300:hover{--tw-bg-opacity:1;background-color:rgb(209 213 219 / var(--tw-bg-opacity, 1))}.hover\:bg-indigo-700:hover{--tw-bg-opacity:1;background-color:rgb(67 56 202 / var(--tw-bg-opacity, 1))}.hover\:bg-purple-700:hover{--tw-bg-opacity:1;background-color:rgb(126 34 206 / var(--tw-bg-opacity, 1))}.hover\:bg-red-700:hover{--tw-bg-opacity:1;background-color:rgb(185 28 28 / var(--tw-bg-opacity, 1))}@media (min-width: 768px){.md\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.md\:p-8{padding:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}}@media (min-width: 1024px){.lg\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}}&amp;amp;lt;/style&amp;amp;gt;&amp;amp;lt;/head&amp;amp;gt;
&amp;amp;lt;body class="p-4 md:p-8"&amp;amp;gt;
    &amp;amp;lt;div class="max-w-6xl mx-auto"&amp;amp;gt;
        &amp;amp;lt;header class="text-center mb-8 relative"&amp;amp;gt;
            &amp;amp;lt;div class="version-badge"&amp;amp;gt;Sürüm 3.0&amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;h1 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2"&amp;amp;gt;İngilizce Kelime ve Deyim Kartları&amp;amp;lt;/h1&amp;amp;gt;
            &amp;amp;lt;p class="text-gray-600"&amp;amp;gt;Kendi kelime ve deyimlerinizi ekleyin, öğrenin ve test edin&amp;amp;lt;/p&amp;amp;gt;
        &amp;amp;lt;/header&amp;amp;gt;
        
        &amp;amp;lt;div class="flex flex-wrap justify-center gap-4 mb-8"&amp;amp;gt;
            &amp;amp;lt;button id="flashcardMode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;gt;Kart Modu&amp;amp;lt;/button&amp;amp;gt;
            &amp;amp;lt;button id="quizMode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;gt;Test Modu&amp;amp;lt;/button&amp;amp;gt;
            &amp;amp;lt;button id="addCardBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;amp;gt;Kart Ekle&amp;amp;lt;/button&amp;amp;gt;
            
            &amp;amp;lt;div class="dropdown"&amp;amp;gt;
                &amp;amp;lt;button class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&amp;amp;gt;
                    &amp;amp;lt;span&amp;amp;gt;Veri Yönetimi&amp;amp;lt;/span&amp;amp;gt;
                    &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                        &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                    &amp;amp;lt;/svg&amp;amp;gt;
                &amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;div class="dropdown-content"&amp;amp;gt;
                    &amp;amp;lt;a href="#" id="exportCardsBtn" class="flex items-center"&amp;amp;gt;
                        &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                            &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                        &amp;amp;lt;/svg&amp;amp;gt;
                        Kartları Dışa Aktar
                    &amp;amp;lt;/a&amp;amp;gt;
                    &amp;amp;lt;a href="#" id="importCardsBtn" class="flex items-center"&amp;amp;gt;
                        &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                            &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                        &amp;amp;lt;/svg&amp;amp;gt;
                        Kartları İçe Aktar
                    &amp;amp;lt;/a&amp;amp;gt;
                    &amp;amp;lt;a href="#" id="jsonEditorBtn" class="flex items-center"&amp;amp;gt;
                        &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                            &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                        &amp;amp;lt;/svg&amp;amp;gt;
                        JSON Düzenleyici
                    &amp;amp;lt;/a&amp;amp;gt;
                    &amp;amp;lt;a href="#" id="clearCardsBtn" class="flex items-center text-red-600"&amp;amp;gt;
                        &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                            &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                        &amp;amp;lt;/svg&amp;amp;gt;
                        Tüm Kartları Sil
                    &amp;amp;lt;/a&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
            
            &amp;amp;lt;button id="viewSourceBtn" class="bg-purple-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-purple-700 transition"&amp;amp;gt;Kaynak Kodu Görüntüle&amp;amp;lt;/button&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;div id="statsBar" class="hidden bg-white p-4 rounded-lg shadow mb-6"&amp;amp;gt;
            &amp;amp;lt;div class="flex justify-between items-center"&amp;amp;gt;
                &amp;amp;lt;div&amp;amp;gt;
                    &amp;amp;lt;span class="font-medium"&amp;amp;gt;Doğru:&amp;amp;lt;/span&amp;amp;gt; 
                    &amp;amp;lt;span id="correctCount" class="text-green-600 font-bold"&amp;amp;gt;0&amp;amp;lt;/span&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div&amp;amp;gt;
                    &amp;amp;lt;span class="font-medium"&amp;amp;gt;Yanlış:&amp;amp;lt;/span&amp;amp;gt; 
                    &amp;amp;lt;span id="incorrectCount" class="text-red-600 font-bold"&amp;amp;gt;0&amp;amp;lt;/span&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div&amp;amp;gt;
                    &amp;amp;lt;span class="font-medium"&amp;amp;gt;Toplam:&amp;amp;lt;/span&amp;amp;gt; 
                    &amp;amp;lt;span id="totalCount" class="text-blue-600 font-bold"&amp;amp;gt;0&amp;amp;lt;/span&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Flashcard Mode Container --&amp;amp;gt;
        &amp;amp;lt;div id="flashcardContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"&amp;amp;gt;
            &amp;amp;lt;!-- Empty state message --&amp;amp;gt;
            &amp;amp;lt;div id="emptyState" class="col-span-full empty-state p-8 flex flex-col items-center justify-center text-center"&amp;amp;gt;
                &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                    &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                &amp;amp;lt;/svg&amp;amp;gt;
                &amp;amp;lt;h3 class="text-xl font-medium text-gray-600 mb-2"&amp;amp;gt;Henüz kart eklenmemiş&amp;amp;lt;/h3&amp;amp;gt;
                &amp;amp;lt;p class="text-gray-500 mb-4"&amp;amp;gt;İngilizce kelime ve deyimlerinizi eklemek için "Kart Ekle" butonuna tıklayın&amp;amp;lt;/p&amp;amp;gt;
                &amp;amp;lt;div class="flex flex-wrap gap-3 justify-center"&amp;amp;gt;
                    &amp;amp;lt;button id="emptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;gt;Kart Ekle&amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;button id="emptyStateImportBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition"&amp;amp;gt;Kartları İçe Aktar&amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Quiz Mode Container --&amp;amp;gt;
        &amp;amp;lt;div id="quizContainer" class="hidden"&amp;amp;gt;
            &amp;amp;lt;div id="quizEmptyState" class="empty-state p-8 flex flex-col items-center justify-center text-center"&amp;amp;gt;
                &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                    &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                &amp;amp;lt;/svg&amp;amp;gt;
                &amp;amp;lt;h3 class="text-xl font-medium text-gray-600 mb-2"&amp;amp;gt;Test için yeterli kart yok&amp;amp;lt;/h3&amp;amp;gt;
                &amp;amp;lt;p class="text-gray-500 mb-4"&amp;amp;gt;Test modu için en az 4 kart eklemeniz gerekiyor&amp;amp;lt;/p&amp;amp;gt;
                &amp;amp;lt;button id="quizEmptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;gt;Kart Ekle&amp;amp;lt;/button&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
            
            &amp;amp;lt;div id="quizContent" class="hidden"&amp;amp;gt;
                &amp;amp;lt;div class="bg-white rounded-xl shadow-lg p-6 mb-6"&amp;amp;gt;
                    &amp;amp;lt;h2 id="quizQuestion" class="text-2xl font-bold text-center mb-6"&amp;amp;gt;Soru yükleniyor...&amp;amp;lt;/h2&amp;amp;gt;
                    &amp;amp;lt;div id="quizOptions" class="space-y-3"&amp;amp;gt;
                        &amp;amp;lt;!-- Quiz options will be generated here --&amp;amp;gt;
                    &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div class="flex justify-center"&amp;amp;gt;
                    &amp;amp;lt;button id="nextQuestion" class="bg-indigo-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;gt;Sonraki Soru&amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Add Card Modal --&amp;amp;gt;
        &amp;amp;lt;div id="addCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;amp;gt;
            &amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;amp;gt;
                &amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;gt;Yeni Kart Ekle&amp;amp;lt;/h2&amp;amp;gt;
                &amp;amp;lt;div class="mb-4"&amp;amp;gt;
                    &amp;amp;lt;label class="block text-gray-700 mb-2" for="wordInput"&amp;amp;gt;İngilizce Kelime/Deyim:&amp;amp;lt;/label&amp;amp;gt;
                    &amp;amp;lt;input id="wordInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="İngilizce kelime veya deyim girin"&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div class="mb-6"&amp;amp;gt;
                    &amp;amp;lt;label class="block text-gray-700 mb-2" for="meaningInput"&amp;amp;gt;Türkçe Anlamı:&amp;amp;lt;/label&amp;amp;gt;
                    &amp;amp;lt;input id="meaningInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="Türkçe anlamını girin"&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;gt;
                    &amp;amp;lt;button id="cancelAddCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;gt;İptal&amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;button id="saveCard" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;amp;gt;Kaydet&amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Confirmation Modal for Clear All --&amp;amp;gt;
        &amp;amp;lt;div id="confirmModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50"&amp;amp;gt;
            &amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;amp;gt;
                &amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;gt;Tüm Kartları Sil&amp;amp;lt;/h2&amp;amp;gt;
                &amp;amp;lt;p class="mb-6 text-gray-700"&amp;amp;gt;Tüm kartlarınız silinecek. Bu işlem geri alınamaz. Devam etmek istiyor musunuz?&amp;amp;lt;/p&amp;amp;gt;
                &amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;gt;
                    &amp;amp;lt;button id="cancelClear" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;gt;İptal&amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;button id="confirmClear" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&amp;amp;gt;Evet, Sil&amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Confirmation Modal for Delete Single Card --&amp;amp;gt;
        &amp;amp;lt;div id="deleteCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;amp;gt;
            &amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;amp;gt;
                &amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;gt;Kartı Sil&amp;amp;lt;/h2&amp;amp;gt;
                &amp;amp;lt;p class="mb-2 text-gray-700"&amp;amp;gt;Bu kartı silmek istediğinizden emin misiniz?&amp;amp;lt;/p&amp;amp;gt;
                &amp;amp;lt;div class="bg-gray-100 p-4 rounded-lg mb-6"&amp;amp;gt;
                    &amp;amp;lt;p class="font-medium text-gray-800" id="deleteCardWord"&amp;amp;gt;Eyyüphan&amp;amp;lt;/p&amp;amp;gt;
                    &amp;amp;lt;p class="text-gray-600" id="deleteCardMeaning"&amp;amp;gt;123124124&amp;amp;lt;/p&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;gt;
                    &amp;amp;lt;button id="cancelDeleteCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;gt;İptal&amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;button id="confirmDeleteCard" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&amp;amp;gt;Evet, Sil&amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Import File Modal (Hidden File Input) --&amp;amp;gt;
        &amp;amp;lt;input type="file" id="importFileInput" accept=".json" class="hidden"&amp;amp;gt;
        
        &amp;amp;lt;!-- JSON Editor Modal --&amp;amp;gt;
        &amp;amp;lt;div id="jsonEditorModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;amp;gt;
            &amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-4xl"&amp;amp;gt;
                &amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;gt;JSON Düzenleyici&amp;amp;lt;/h2&amp;amp;gt;
                &amp;amp;lt;p class="mb-4 text-gray-700"&amp;amp;gt;Kartlarınızı JSON formatında düzenleyebilirsiniz. Aşağıdaki metni kopyalayıp saklayabilir veya düzenleyip geri yükleyebilirsiniz.&amp;amp;lt;/p&amp;amp;gt;
                &amp;amp;lt;div class="mb-6"&amp;amp;gt;
                    &amp;amp;lt;textarea id="jsonTextarea" class="w-full p-4 border border-gray-300 rounded json-textarea h-64"&amp;amp;gt;&amp;amp;lt;/textarea&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;gt;
                    &amp;amp;lt;button id="copyJsonBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&amp;amp;gt;
                        &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                            &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                        &amp;amp;lt;/svg&amp;amp;gt;
                        Kopyala
                    &amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;button id="applyJsonBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;amp;gt;Uygula&amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;button id="cancelJsonEditor" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;gt;İptal&amp;amp;lt;/button&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Source Code Modal --&amp;amp;gt;
        &amp;amp;lt;div id="sourceCodeModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;amp;gt;
            &amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-5xl code-modal"&amp;amp;gt;
                &amp;amp;lt;div class="flex justify-between items-center mb-4"&amp;amp;gt;
                    &amp;amp;lt;h2 class="text-2xl font-bold"&amp;amp;gt;Kaynak Kodu&amp;amp;lt;/h2&amp;amp;gt;
                    &amp;amp;lt;div class="flex gap-2"&amp;amp;gt;
                        &amp;amp;lt;button id="copySourceCode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition flex items-center"&amp;amp;gt;
                            &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                                &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&amp;amp;gt;&amp;amp;lt;/path&amp;amp;gt;
                            &amp;amp;lt;/svg&amp;amp;gt;
                            Kopyala
                        &amp;amp;lt;/button&amp;amp;gt;
                        &amp;amp;lt;button id="closeSourceCode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;gt;Kapat&amp;amp;lt;/button&amp;amp;gt;
                    &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;/div&amp;amp;gt;
                &amp;amp;lt;div id="sourceCodeContent" class="code-content"&amp;amp;gt;&amp;amp;amp;lt;html lang="tr"&amp;amp;amp;gt;&amp;amp;amp;lt;head&amp;amp;amp;gt;
    &amp;amp;amp;lt;meta charset="UTF-8"&amp;amp;amp;gt;
    &amp;amp;amp;lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&amp;amp;amp;gt;
    &amp;amp;amp;lt;title&amp;amp;amp;gt;İngilizce Kelime ve Deyim Kartları - Sürüm 3&amp;amp;amp;lt;/title&amp;amp;amp;gt;
    &amp;amp;amp;lt;script src="https://cdn.tailwindcss.com"&amp;amp;amp;gt;&amp;amp;amp;lt;/script&amp;amp;amp;gt;
    &amp;amp;amp;lt;style&amp;amp;amp;gt;
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&amp;amp;amp;amp;display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }
        
        .flashcard {
            perspective: 1000px;
            height: 200px;
            cursor: pointer;
            transition: transform 0.3s;
            position: relative;
        }
        
        .flashcard:hover {
            transform: translateY(-5px);
        }
        
        .flashcard-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border-radius: 1rem;
        }
        
        .flashcard.flipped .flashcard-inner {
            transform: rotateY(180deg);
        }
        
        .flashcard-front, .flashcard-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 1rem;
            padding: 1.5rem;
        }
        
        .flashcard-front {
            background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%);
            color: white;
        }
        
        .flashcard-back {
            background: linear-gradient(135deg, #10b981 0%, #34d399 100%);
            color: #333;
            transform: rotateY(180deg);
        }
        
        .delete-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(239, 68, 68, 0.9);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s;
            z-index: 10;
            cursor: pointer;
        }
        
        .flashcard:hover .delete-btn {
            opacity: 1;
        }
        
        .delete-btn:hover {
            background-color: rgb(239, 68, 68);
        }
        
        .quiz-option {
            transition: all 0.3s;
        }
        
        .quiz-option:hover {
            transform: translateX(5px);
        }
        
        .quiz-option.correct {
            background-color: #4ade80 !important;
            color: white;
        }
        
        .quiz-option.incorrect {
            background-color: #f87171 !important;
            color: white;
        }
        
        .empty-state {
            border: 2px dashed #cbd5e1;
            border-radius: 1rem;
            transition: all 0.3s;
        }
        
        .empty-state:hover {
            border-color: #94a3b8;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #1e293b;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .toast.show {
            opacity: 1;
        }
        
        .code-modal {
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .code-content {
            white-space: pre-wrap;
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            overflow-x: auto;
            background-color: #f8fafc;
            padding: 16px;
            border-radius: 8px;
            border: 1px solid #e2e8f0;
        }
        
        .version-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: #4f46e5;
            color: white;
            padding: 2px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 600;
        }
        
        .file-input-wrapper {
            position: relative;
            overflow: hidden;
            display: inline-block;
        }
        
        .file-input-wrapper input[type=file] {
            position: absolute;
            left: 0;
            top: 0;
            opacity: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }
        
        .dropdown {
            position: relative;
            display: inline-block;
        }
        
        .dropdown-content {
            display: none;
            position: absolute;
            right: 0;
            background-color: white;
            min-width: 200px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
            z-index: 1;
            border-radius: 0.5rem;
            overflow: hidden;
        }
        
        .dropdown-content a {
            color: black;
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            transition: all 0.2s;
        }
        
        .dropdown-content a:hover {
            background-color: #f1f5f9;
        }
        
        .dropdown:hover .dropdown-content {
            display: block;
        }
        
        .json-textarea {
            font-family: monospace;
            font-size: 14px;
            line-height: 1.5;
            resize: vertical;
        }
    &amp;amp;amp;lt;/style&amp;amp;amp;gt;
&amp;amp;amp;lt;style&amp;amp;amp;gt;*, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.16 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.relative{position:relative}.inset-0{inset:0px}.z-50{z-index:50}.col-span-full{grid-column:1 / -1}.mx-auto{margin-left:auto;margin-right:auto}.mb-2{margin-bottom:0.5rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-1{margin-left:0.25rem}.mr-1{margin-right:0.25rem}.mr-2{margin-right:0.5rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-16{height:4rem}.h-4{height:1rem}.h-5{height:1.25rem}.h-64{height:16rem}.w-16{width:4rem}.w-4{width:1rem}.w-5{width:1.25rem}.w-full{width:100%}.max-w-4xl{max-width:56rem}.max-w-5xl{max-width:64rem}.max-w-6xl{max-width:72rem}.max-w-md{max-width:28rem}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.flex-col{flex-direction:column}.flex-wrap{flex-wrap:wrap}.items-center{align-items:center}.justify-end{justify-content:flex-end}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-2{gap:0.5rem}.gap-3{gap:0.75rem}.gap-4{gap:1rem}.gap-6{gap:1.5rem}.space-y-3 &amp;amp;amp;gt; :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.75rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.75rem * var(--tw-space-y-reverse))}.rounded{border-radius:0.25rem}.rounded-lg{border-radius:0.5rem}.rounded-xl{border-radius:0.75rem}.border{border-width:1px}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.bg-black{--tw-bg-opacity:1;background-color:rgb(0 0 0 / var(--tw-bg-opacity, 1))}.bg-blue-600{--tw-bg-opacity:1;background-color:rgb(37 99 235 / var(--tw-bg-opacity, 1))}.bg-emerald-600{--tw-bg-opacity:1;background-color:rgb(5 150 105 / var(--tw-bg-opacity, 1))}.bg-gray-100{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.bg-gray-200{--tw-bg-opacity:1;background-color:rgb(229 231 235 / var(--tw-bg-opacity, 1))}.bg-indigo-600{--tw-bg-opacity:1;background-color:rgb(79 70 229 / var(--tw-bg-opacity, 1))}.bg-purple-600{--tw-bg-opacity:1;background-color:rgb(147 51 234 / var(--tw-bg-opacity, 1))}.bg-red-600{--tw-bg-opacity:1;background-color:rgb(220 38 38 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.bg-opacity-50{--tw-bg-opacity:0.5}.p-4{padding:1rem}.p-2{padding:0.5rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-4{padding-left:1rem;padding-right:1rem}.px-6{padding-left:1.5rem;padding-right:1.5rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.text-center{text-align:center}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-xl{font-size:1.25rem;line-height:1.75rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.text-blue-600{--tw-text-opacity:1;color:rgb(37 99 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-500{--tw-text-opacity:1;color:rgb(107 114 128 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-gray-800{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-green-600{--tw-text-opacity:1;color:rgb(22 163 74 / var(--tw-text-opacity, 1))}.text-red-600{--tw-text-opacity:1;color:rgb(220 38 38 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow{--tw-shadow:0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 1px 3px 0 var(--tw-shadow-color), 0 1px 2px -1px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.hover\:bg-blue-700:hover{--tw-bg-opacity:1;background-color:rgb(29 78 216 / var(--tw-bg-opacity, 1))}.hover\:bg-emerald-700:hover{--tw-bg-opacity:1;background-color:rgb(4 120 87 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-300:hover{--tw-bg-opacity:1;background-color:rgb(209 213 219 / var(--tw-bg-opacity, 1))}.hover\:bg-indigo-700:hover{--tw-bg-opacity:1;background-color:rgb(67 56 202 / var(--tw-bg-opacity, 1))}.hover\:bg-purple-700:hover{--tw-bg-opacity:1;background-color:rgb(126 34 206 / var(--tw-bg-opacity, 1))}.hover\:bg-red-700:hover{--tw-bg-opacity:1;background-color:rgb(185 28 28 / var(--tw-bg-opacity, 1))}@media (min-width: 768px){.md\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.md\:p-8{padding:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}}@media (min-width: 1024px){.lg\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}}&amp;amp;amp;lt;/style&amp;amp;amp;gt;&amp;amp;amp;lt;/head&amp;amp;amp;gt;
&amp;amp;amp;lt;body class="p-4 md:p-8"&amp;amp;amp;gt;
    &amp;amp;amp;lt;div class="max-w-6xl mx-auto"&amp;amp;amp;gt;
        &amp;amp;amp;lt;header class="text-center mb-8 relative"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="version-badge"&amp;amp;amp;gt;Sürüm 3.0&amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;h1 class="text-3xl md:text-4xl font-bold text-gray-800 mb-2"&amp;amp;amp;gt;İngilizce Kelime ve Deyim Kartları&amp;amp;amp;lt;/h1&amp;amp;amp;gt;
            &amp;amp;amp;lt;p class="text-gray-600"&amp;amp;amp;gt;Kendi kelime ve deyimlerinizi ekleyin, öğrenin ve test edin&amp;amp;amp;lt;/p&amp;amp;amp;gt;
        &amp;amp;amp;lt;/header&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;div class="flex flex-wrap justify-center gap-4 mb-8"&amp;amp;amp;gt;
            &amp;amp;amp;lt;button id="flashcardMode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;amp;gt;Kart Modu&amp;amp;amp;lt;/button&amp;amp;amp;gt;
            &amp;amp;amp;lt;button id="quizMode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;amp;gt;Test Modu&amp;amp;amp;lt;/button&amp;amp;amp;gt;
            &amp;amp;amp;lt;button id="addCardBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;amp;amp;gt;Kart Ekle&amp;amp;amp;lt;/button&amp;amp;amp;gt;
            
            &amp;amp;amp;lt;div class="dropdown"&amp;amp;amp;gt;
                &amp;amp;amp;lt;button class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;span&amp;amp;amp;gt;Veri Yönetimi&amp;amp;amp;lt;/span&amp;amp;amp;gt;
                    &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                    &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                &amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="dropdown-content"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;a href="#" id="exportCardsBtn" class="flex items-center"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        Kartları Dışa Aktar
                    &amp;amp;amp;lt;/a&amp;amp;amp;gt;
                    &amp;amp;amp;lt;a href="#" id="importCardsBtn" class="flex items-center"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        Kartları İçe Aktar
                    &amp;amp;amp;lt;/a&amp;amp;amp;gt;
                    &amp;amp;amp;lt;a href="#" id="jsonEditorBtn" class="flex items-center"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        JSON Düzenleyici
                    &amp;amp;amp;lt;/a&amp;amp;amp;gt;
                    &amp;amp;amp;lt;a href="#" id="clearCardsBtn" class="flex items-center text-red-600"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        Tüm Kartları Sil
                    &amp;amp;amp;lt;/a&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            
            &amp;amp;amp;lt;button id="viewSourceBtn" class="bg-purple-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-purple-700 transition"&amp;amp;amp;gt;Kaynak Kodu Görüntüle&amp;amp;amp;lt;/button&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;div id="statsBar" class="hidden bg-white p-4 rounded-lg shadow mb-6"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="flex justify-between items-center"&amp;amp;amp;gt;
                &amp;amp;amp;lt;div&amp;amp;amp;gt;
                    &amp;amp;amp;lt;span class="font-medium"&amp;amp;amp;gt;Doğru:&amp;amp;amp;lt;/span&amp;amp;amp;gt; 
                    &amp;amp;amp;lt;span id="correctCount" class="text-green-600 font-bold"&amp;amp;amp;gt;0&amp;amp;amp;lt;/span&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div&amp;amp;amp;gt;
                    &amp;amp;amp;lt;span class="font-medium"&amp;amp;amp;gt;Yanlış:&amp;amp;amp;lt;/span&amp;amp;amp;gt; 
                    &amp;amp;amp;lt;span id="incorrectCount" class="text-red-600 font-bold"&amp;amp;amp;gt;0&amp;amp;amp;lt;/span&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div&amp;amp;amp;gt;
                    &amp;amp;amp;lt;span class="font-medium"&amp;amp;amp;gt;Toplam:&amp;amp;amp;lt;/span&amp;amp;amp;gt; 
                    &amp;amp;amp;lt;span id="totalCount" class="text-blue-600 font-bold"&amp;amp;amp;gt;0&amp;amp;amp;lt;/span&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Flashcard Mode Container --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="flashcardContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"&amp;amp;amp;gt;
            &amp;amp;amp;lt;!-- Empty state message --&amp;amp;amp;gt;
            &amp;amp;amp;lt;div id="emptyState" class="col-span-full empty-state p-8 flex flex-col items-center justify-center text-center hidden"&amp;amp;amp;gt;
                &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                &amp;amp;amp;lt;h3 class="text-xl font-medium text-gray-600 mb-2"&amp;amp;amp;gt;Henüz kart eklenmemiş&amp;amp;amp;lt;/h3&amp;amp;amp;gt;
                &amp;amp;amp;lt;p class="text-gray-500 mb-4"&amp;amp;amp;gt;İngilizce kelime ve deyimlerinizi eklemek için "Kart Ekle" butonuna tıklayın&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex flex-wrap gap-3 justify-center"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="emptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;amp;gt;Kart Ekle&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="emptyStateImportBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition"&amp;amp;amp;gt;Kartları İçe Aktar&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;div class="flashcard"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;div class="delete-btn" data-index="0"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                        &amp;amp;amp;lt;div class="flashcard-inner"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;div class="flashcard-front"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;h2 class="text-2xl font-bold text-center"&amp;amp;amp;gt;asdasd&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                            &amp;amp;amp;lt;div class="flashcard-back"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;p class="text-xl text-center"&amp;amp;amp;gt;123124124&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                    &amp;amp;amp;lt;/div&amp;amp;amp;gt;&amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Quiz Mode Container --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="quizContainer" class="hidden"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div id="quizEmptyState" class="empty-state p-8 flex flex-col items-center justify-center text-center"&amp;amp;amp;gt;
                &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 text-gray-400 mb-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                &amp;amp;amp;lt;h3 class="text-xl font-medium text-gray-600 mb-2"&amp;amp;amp;gt;Test için yeterli kart yok&amp;amp;amp;lt;/h3&amp;amp;amp;gt;
                &amp;amp;amp;lt;p class="text-gray-500 mb-4"&amp;amp;amp;gt;Test modu için en az 4 kart eklemeniz gerekiyor&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                &amp;amp;amp;lt;button id="quizEmptyStateAddBtn" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;amp;gt;Kart Ekle&amp;amp;amp;lt;/button&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            
            &amp;amp;amp;lt;div id="quizContent" class="hidden"&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="bg-white rounded-xl shadow-lg p-6 mb-6"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;h2 id="quizQuestion" class="text-2xl font-bold text-center mb-6"&amp;amp;amp;gt;Soru yükleniyor...&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                    &amp;amp;amp;lt;div id="quizOptions" class="space-y-3"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;!-- Quiz options will be generated here --&amp;amp;amp;gt;
                    &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex justify-center"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="nextQuestion" class="bg-indigo-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-indigo-700 transition"&amp;amp;amp;gt;Sonraki Soru&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Add Card Modal --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="addCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;amp;amp;gt;
                &amp;amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;amp;gt;Yeni Kart Ekle&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="mb-4"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;label class="block text-gray-700 mb-2" for="wordInput"&amp;amp;amp;gt;İngilizce Kelime/Deyim:&amp;amp;amp;lt;/label&amp;amp;amp;gt;
                    &amp;amp;amp;lt;input id="wordInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="İngilizce kelime veya deyim girin"&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="mb-6"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;label class="block text-gray-700 mb-2" for="meaningInput"&amp;amp;amp;gt;Türkçe Anlamı:&amp;amp;amp;lt;/label&amp;amp;amp;gt;
                    &amp;amp;amp;lt;input id="meaningInput" type="text" class="w-full p-2 border border-gray-300 rounded" placeholder="Türkçe anlamını girin"&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="cancelAddCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;amp;gt;İptal&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="saveCard" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;amp;amp;gt;Kaydet&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Confirmation Modal for Clear All --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="confirmModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;amp;amp;gt;
                &amp;amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;amp;gt;Tüm Kartları Sil&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                &amp;amp;amp;lt;p class="mb-6 text-gray-700"&amp;amp;amp;gt;Tüm kartlarınız silinecek. Bu işlem geri alınamaz. Devam etmek istiyor musunuz?&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="cancelClear" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;amp;gt;İptal&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="confirmClear" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&amp;amp;amp;gt;Evet, Sil&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Confirmation Modal for Delete Single Card --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="deleteCardModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-md"&amp;amp;amp;gt;
                &amp;amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;amp;gt;Kartı Sil&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                &amp;amp;amp;lt;p class="mb-2 text-gray-700"&amp;amp;amp;gt;Bu kartı silmek istediğinizden emin misiniz?&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="bg-gray-100 p-4 rounded-lg mb-6"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;p class="font-medium text-gray-800" id="deleteCardWord"&amp;amp;amp;gt;&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                    &amp;amp;amp;lt;p class="text-gray-600" id="deleteCardMeaning"&amp;amp;amp;gt;&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="cancelDeleteCard" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;amp;gt;İptal&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="confirmDeleteCard" class="bg-red-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-red-700 transition"&amp;amp;amp;gt;Evet, Sil&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Import File Modal (Hidden File Input) --&amp;amp;amp;gt;
        &amp;amp;amp;lt;input type="file" id="importFileInput" accept=".json" class="hidden"&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- JSON Editor Modal --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="jsonEditorModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-4xl"&amp;amp;amp;gt;
                &amp;amp;amp;lt;h2 class="text-2xl font-bold mb-4"&amp;amp;amp;gt;JSON Düzenleyici&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                &amp;amp;amp;lt;p class="mb-4 text-gray-700"&amp;amp;amp;gt;Kartlarınızı JSON formatında düzenleyebilirsiniz. Aşağıdaki metni kopyalayıp saklayabilir veya düzenleyip geri yükleyebilirsiniz.&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="mb-6"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;textarea id="jsonTextarea" class="w-full p-4 border border-gray-300 rounded json-textarea h-64"&amp;amp;amp;gt;&amp;amp;amp;lt;/textarea&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex justify-end gap-3"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="copyJsonBtn" class="bg-blue-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-700 transition flex items-center"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        Kopyala
                    &amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="applyJsonBtn" class="bg-emerald-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-emerald-700 transition"&amp;amp;amp;gt;Uygula&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;button id="cancelJsonEditor" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;amp;gt;İptal&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Source Code Modal --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="sourceCodeModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50"&amp;amp;amp;gt;
            &amp;amp;amp;lt;div class="bg-white rounded-xl p-6 w-full max-w-5xl code-modal"&amp;amp;amp;gt;
                &amp;amp;amp;lt;div class="flex justify-between items-center mb-4"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;h2 class="text-2xl font-bold"&amp;amp;amp;gt;Kaynak Kodu&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                    &amp;amp;amp;lt;div class="flex gap-2"&amp;amp;amp;gt;
                        &amp;amp;amp;lt;button id="copySourceCode" class="bg-indigo-600 text-white px-4 py-2 rounded-lg font-medium hover:bg-indigo-700 transition flex items-center"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"&amp;amp;amp;gt;&amp;amp;amp;lt;/path&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                            Kopyala
                        &amp;amp;amp;lt;/button&amp;amp;amp;gt;
                        &amp;amp;amp;lt;button id="closeSourceCode" class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg font-medium hover:bg-gray-300 transition"&amp;amp;amp;gt;Kapat&amp;amp;amp;lt;/button&amp;amp;amp;gt;
                    &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                &amp;amp;amp;lt;div id="sourceCodeContent" class="code-content"&amp;amp;amp;gt;
                    &amp;amp;amp;lt;!-- Source code will be inserted here --&amp;amp;amp;gt;
                &amp;amp;amp;lt;/div&amp;amp;amp;gt;
            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
        
        &amp;amp;amp;lt;!-- Toast Notification --&amp;amp;amp;gt;
        &amp;amp;amp;lt;div id="toast" class="toast"&amp;amp;amp;gt;Kartlar dışa aktarıldı&amp;amp;amp;lt;/div&amp;amp;amp;gt;
    &amp;amp;amp;lt;/div&amp;amp;amp;gt;

    &amp;amp;amp;lt;script&amp;amp;amp;gt;
        // Initialize empty flashcards array
        let flashcards = [];
        
        // Stats for quiz mode
        let stats = {
            correct: 0,
            incorrect: 0,
            total: 0
        };
        
        let currentQuizIndex = 0;
        let cardToDeleteIndex = -1;
        
        // DOM elements
        const flashcardContainer = document.getElementById('flashcardContainer');
        const quizContainer = document.getElementById('quizContainer');
        const quizContent = document.getElementById('quizContent');
        const quizEmptyState = document.getElementById('quizEmptyState');
        const emptyState = document.getElementById('emptyState');
        const flashcardModeBtn = document.getElementById('flashcardMode');
        const quizModeBtn = document.getElementById('quizMode');
        const addCardBtn = document.getElementById('addCardBtn');
        const clearCardsBtn = document.getElementById('clearCardsBtn');
        const exportCardsBtn = document.getElementById('exportCardsBtn');
        const importCardsBtn = document.getElementById('importCardsBtn');
        const jsonEditorBtn = document.getElementById('jsonEditorBtn');
        const importFileInput = document.getElementById('importFileInput');
        const viewSourceBtn = document.getElementById('viewSourceBtn');
        const addCardModal = document.getElementById('addCardModal');
        const confirmModal = document.getElementById('confirmModal');
        const deleteCardModal = document.getElementById('deleteCardModal');
        const jsonEditorModal = document.getElementById('jsonEditorModal');
        const sourceCodeModal = document.getElementById('sourceCodeModal');
        const cancelAddCardBtn = document.getElementById('cancelAddCard');
        const saveCardBtn = document.getElementById('saveCard');
        const wordInput = document.getElementById('wordInput');
        const meaningInput = document.getElementById('meaningInput');
        const emptyStateAddBtn = document.getElementById('emptyStateAddBtn');
        const emptyStateImportBtn = document.getElementById('emptyStateImportBtn');
        const quizEmptyStateAddBtn = document.getElementById('quizEmptyStateAddBtn');
        const statsBar = document.getElementById('statsBar');
        const correctCountEl = document.getElementById('correctCount');
        const incorrectCountEl = document.getElementById('incorrectCount');
        const totalCountEl = document.getElementById('totalCount');
        const nextQuestionBtn = document.getElementById('nextQuestion');
        const cancelClearBtn = document.getElementById('cancelClear');
        const confirmClearBtn = document.getElementById('confirmClear');
        const deleteCardWord = document.getElementById('deleteCardWord');
        const deleteCardMeaning = document.getElementById('deleteCardMeaning');
        const cancelDeleteCardBtn = document.getElementById('cancelDeleteCard');
        const confirmDeleteCardBtn = document.getElementById('confirmDeleteCard');
        const jsonTextarea = document.getElementById('jsonTextarea');
        const copyJsonBtn = document.getElementById('copyJsonBtn');
        const applyJsonBtn = document.getElementById('applyJsonBtn');
        const cancelJsonEditor = document.getElementById('cancelJsonEditor');
        const copySourceCodeBtn = document.getElementById('copySourceCode');
        const closeSourceCodeBtn = document.getElementById('closeSourceCode');
        const sourceCodeContent = document.getElementById('sourceCodeContent');
        const toast = document.getElementById('toast');
        
        // Initialize the app
        function init() {
            loadFlashcards();
            renderFlashcards();
            setupEventListeners();
        }
        
        // Load flashcards from localStorage
        function loadFlashcards() {
            const savedFlashcards = localStorage.getItem('englishFlashcards');
            if (savedFlashcards) {
                try {
                    flashcards = JSON.parse(savedFlashcards);
                } catch (e) {
                    console.error('Error parsing saved flashcards:', e);
                    flashcards = [];
                }
            }
        }
        
        // Save flashcards to localStorage
        function saveFlashcards() {
            localStorage.setItem('englishFlashcards', JSON.stringify(flashcards));
        }
        
        // Render all flashcards
        function renderFlashcards() {
            // Clear container except for empty state
            const cards = flashcardContainer.querySelectorAll('.flashcard');
            cards.forEach(card =&amp;amp;amp;gt; card.remove());
            
            // Show or hide empty state
            if (flashcards.length === 0) {
                emptyState.classList.remove('hidden');
            } else {
                emptyState.classList.add('hidden');
                
                // Add flashcards
                flashcards.forEach((card, index) =&amp;amp;amp;gt; {
                    const flashcardEl = document.createElement('div');
                    flashcardEl.className = 'flashcard';
                    flashcardEl.innerHTML = `
                        &amp;amp;amp;lt;div class="delete-btn" data-index="${index}"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" /&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/svg&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                        &amp;amp;amp;lt;div class="flashcard-inner"&amp;amp;amp;gt;
                            &amp;amp;amp;lt;div class="flashcard-front"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;h2 class="text-2xl font-bold text-center"&amp;amp;amp;gt;${card.word}&amp;amp;amp;lt;/h2&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                            &amp;amp;amp;lt;div class="flashcard-back"&amp;amp;amp;gt;
                                &amp;amp;amp;lt;p class="text-xl text-center"&amp;amp;amp;gt;${card.meaning}&amp;amp;amp;lt;/p&amp;amp;amp;gt;
                            &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                        &amp;amp;amp;lt;/div&amp;amp;amp;gt;
                    `;
                    
                    // Add click event for flipping the card
                    const flashcardInner = flashcardEl.querySelector('.flashcard-inner');
                    flashcardInner.addEventListener('click', () =&amp;amp;amp;gt; {
                        flashcardEl.classList.toggle('flipped');
                    });
                    
                    // Add click event for delete button
                    const deleteBtn = flashcardEl.querySelector('.delete-btn');
                    deleteBtn.addEventListener('click', (e) =&amp;amp;amp;gt; {
                        e.stopPropagation(); // Prevent card flip
                        const index = parseInt(deleteBtn.getAttribute('data-index'));
                        showDeleteCardModal(index);
                    });
                    
                    flashcardContainer.appendChild(flashcardEl);
                });
            }
        }
        
        // Show delete card confirmation modal
        function showDeleteCardModal(index) {
            cardToDeleteIndex = index;
            const card = flashcards[index];
            deleteCardWord.textContent = card.word;
            deleteCardMeaning.textContent = card.meaning;
            deleteCardModal.classList.remove('hidden');
        }
        
        // Delete a single card
        function deleteCard(index) {
            if (index &amp;amp;amp;gt;= 0 &amp;amp;amp;amp;&amp;amp;amp;amp; index &amp;amp;amp;lt; flashcards.length) {
                flashcards.splice(index, 1);
                saveFlashcards();
                renderFlashcards();
                showToast('Kart silindi');
            }
        }
        
        // Export flashcards to JSON file
        function exportFlashcards() {
            const dataStr = JSON.stringify(flashcards, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = 'ingilizce_kartlarim.json';
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showToast('Kartlar dışa aktarıldı');
        }
        
        // Import flashcards from JSON file
        function importFlashcards(file) {
            const reader = new FileReader();
            
            reader.onload = function(e) {
                try {
                    const importedCards = JSON.parse(e.target.result);
                    
                    if (Array.isArray(importedCards)) {
                        // Check if each card has the required properties
                        const validCards = importedCards.filter(card =&amp;amp;amp;gt; 
                            card &amp;amp;amp;amp;&amp;amp;amp;amp; typeof card === 'object' &amp;amp;amp;amp;&amp;amp;amp;amp; 
                            'word' in card &amp;amp;amp;amp;&amp;amp;amp;amp; 'meaning' in card &amp;amp;amp;amp;&amp;amp;amp;amp;
                            typeof card.word === 'string' &amp;amp;amp;amp;&amp;amp;amp;amp; 
                            typeof card.meaning === 'string'
                        );
                        
                        if (validCards.length &amp;amp;amp;gt; 0) {
                            flashcards = validCards;
                            saveFlashcards();
                            renderFlashcards();
                            showToast(`${validCards.length} kart içe aktarıldı`);
                        } else {
                            showToast('Geçerli kart bulunamadı');
                        }
                    } else {
                        showToast('Geçersiz JSON formatı');
                    }
                } catch (error) {
                    console.error('Import error:', error);
                    showToast('Dosya okunamadı');
                }
            };
            
            reader.readAsText(file);
        }
        
        // Show JSON editor with current flashcards
        function showJsonEditor() {
            jsonTextarea.value = JSON.stringify(flashcards, null, 2);
            jsonEditorModal.classList.remove('hidden');
        }
        
        // Apply JSON from editor
        function applyJsonFromEditor() {
            try {
                const jsonData = JSON.parse(jsonTextarea.value);
                
                if (Array.isArray(jsonData)) {
                    // Check if each card has the required properties
                    const validCards = jsonData.filter(card =&amp;amp;amp;gt; 
                        card &amp;amp;amp;amp;&amp;amp;amp;amp; typeof card === 'object' &amp;amp;amp;amp;&amp;amp;amp;amp; 
                        'word' in card &amp;amp;amp;amp;&amp;amp;amp;amp; 'meaning' in card &amp;amp;amp;amp;&amp;amp;amp;amp;
                        typeof card.word === 'string' &amp;amp;amp;amp;&amp;amp;amp;amp; 
                        typeof card.meaning === 'string'
                    );
                    
                    if (validCards.length &amp;amp;amp;gt; 0) {
                        flashcards = validCards;
                        saveFlashcards();
                        renderFlashcards();
                        jsonEditorModal.classList.add('hidden');
                        showToast(`${validCards.length} kart güncellendi`);
                    } else {
                        showToast('Geçerli kart bulunamadı');
                    }
                } else {
                    showToast('Geçersiz JSON formatı');
                }
            } catch (error) {
                console.error('JSON parse error:', error);
                showToast('Geçersiz JSON formatı');
            }
        }
        
        // Setup quiz mode
        function setupQuiz() {
            currentQuizIndex = 0;
            stats.correct = 0;
            stats.incorrect = 0;
            stats.total = 0;
            updateStats();
            
            // Check if we have enough cards for quiz mode
            if (flashcards.length &amp;amp;amp;lt; 4) {
                quizContent.classList.add('hidden');
                quizEmptyState.classList.remove('hidden');
            } else {
                quizContent.classList.remove('hidden');
                quizEmptyState.classList.add('hidden');
                showNextQuestion();
            }
        }
        
        // Show next question in quiz mode
        function showNextQuestion() {
            if (currentQuizIndex &amp;amp;amp;gt;= flashcards.length) {
                // Reset if we've gone through all cards
                currentQuizIndex = 0;
            }
            
            const currentCard = flashcards[currentQuizIndex];
            const quizQuestion = document.getElementById('quizQuestion');
            const quizOptions = document.getElementById('quizOptions');
            
            quizQuestion.textContent = currentCard.word;
            
            // Create options (including the correct one and some random ones)
            let options = [currentCard.meaning];
            
            // Add some random options from other cards
            let availableCards = [...flashcards];
            availableCards.splice(currentQuizIndex, 1); // Remove current card
            
            // Shuffle available cards
            availableCards = shuffleArray(availableCards);
            
            // Add up to 3 more options
            for (let i = 0; i &amp;amp;amp;lt; 3 &amp;amp;amp;amp;&amp;amp;amp;amp; i &amp;amp;amp;lt; availableCards.length; i++) {
                options.push(availableCards[i].meaning);
            }
            
            // Shuffle options
            options = shuffleArray(options);
            
            // Render options
            quizOptions.innerHTML = '';
            options.forEach(option =&amp;amp;amp;gt; {
                const optionEl = document.createElement('div');
                optionEl.className = 'quiz-option bg-gray-100 p-4 rounded-lg cursor-pointer hover:bg-gray-200';
                optionEl.textContent = option;
                
                optionEl.addEventListener('click', () =&amp;amp;amp;gt; {
                    // Disable all options after selection
                    document.querySelectorAll('.quiz-option').forEach(el =&amp;amp;amp;gt; {
                        el.style.pointerEvents = 'none';
                    });
                    
                    if (option === currentCard.meaning) {
                        optionEl.classList.add('correct');
                        stats.correct++;
                    } else {
                        optionEl.classList.add('incorrect');
                        stats.incorrect++;
                        
                        // Highlight the correct answer
                        document.querySelectorAll('.quiz-option').forEach(el =&amp;amp;amp;gt; {
                            if (el.textContent === currentCard.meaning) {
                                el.classList.add('correct');
                            }
                        });
                    }
                    
                    stats.total++;
                    updateStats();
                });
                
                quizOptions.appendChild(optionEl);
            });
        }
        
        // Update stats display
        function updateStats() {
            correctCountEl.textContent = stats.correct;
            incorrectCountEl.textContent = stats.incorrect;
            totalCountEl.textContent = stats.total;
        }
        
        // Helper function to shuffle an array
        function shuffleArray(array) {
            const newArray = [...array];
            for (let i = newArray.length - 1; i &amp;amp;amp;gt; 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
            }
            return newArray;
        }
        
        // Show toast notification
        function showToast(message) {
            toast.textContent = message;
            toast.classList.add('show');
            
            setTimeout(() =&amp;amp;amp;gt; {
                toast.classList.remove('show');
            }, 3000);
        }
        
        // Get source code of the current page
        function getSourceCode() {
            return document.documentElement.outerHTML;
        }
        
        // Setup event listeners
        function setupEventListeners() {
            // Mode switching
            flashcardModeBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            quizModeBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                flashcardContainer.classList.add('hidden');
                quizContainer.classList.remove('hidden');
                statsBar.classList.remove('hidden');
                quizModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                quizModeBtn.classList.replace('text-gray-700', 'text-white');
                flashcardModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                flashcardModeBtn.classList.replace('text-white', 'text-gray-700');
                setupQuiz();
            });
            
            // Next question button
            nextQuestionBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                currentQuizIndex++;
                showNextQuestion();
            });
            
            // Add card buttons
            addCardBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateAddBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateImportBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                importFileInput.click();
            });
            
            quizEmptyStateAddBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                addCardModal.classList.remove('hidden');
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            cancelAddCardBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                addCardModal.classList.add('hidden');
                wordInput.value = '';
                meaningInput.value = '';
            });
            
            saveCardBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                const word = wordInput.value.trim();
                const meaning = meaningInput.value.trim();
                
                if (word &amp;amp;amp;amp;&amp;amp;amp;amp; meaning) {
                    flashcards.push({ word, meaning });
                    saveFlashcards();
                    renderFlashcards();
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                    showToast('Kart eklendi');
                }
            });
            
            // Clear cards functionality
            clearCardsBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                if (flashcards.length &amp;amp;amp;gt; 0) {
                    confirmModal.classList.remove('hidden');
                }
            });
            
            cancelClearBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                confirmModal.classList.add('hidden');
            });
            
            confirmClearBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                flashcards = [];
                saveFlashcards();
                renderFlashcards();
                confirmModal.classList.add('hidden');
                showToast('Tüm kartlar silindi');
            });
            
            // Delete single card functionality
            cancelDeleteCardBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            confirmDeleteCardBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                deleteCard(cardToDeleteIndex);
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            // Export/Import functionality
            exportCardsBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                exportFlashcards();
            });
            
            importCardsBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                importFileInput.click();
            });
            
            importFileInput.addEventListener('change', (e) =&amp;amp;amp;gt; {
                if (e.target.files.length &amp;amp;amp;gt; 0) {
                    importFlashcards(e.target.files[0]);
                    // Reset the input so the same file can be selected again
                    e.target.value = '';
                }
            });
            
            // JSON Editor functionality
            jsonEditorBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                showJsonEditor();
            });
            
            copyJsonBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                jsonTextarea.select();
                document.execCommand('copy');
                showToast('JSON kopyalandı');
            });
            
            applyJsonBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                applyJsonFromEditor();
            });
            
            cancelJsonEditor.addEventListener('click', () =&amp;amp;amp;gt; {
                jsonEditorModal.classList.add('hidden');
            });
            
            // Source code functionality
            viewSourceBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                sourceCodeContent.textContent = getSourceCode();
                sourceCodeModal.classList.remove('hidden');
            });
            
            closeSourceCodeBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                sourceCodeModal.classList.add('hidden');
            });
            
            copySourceCodeBtn.addEventListener('click', () =&amp;amp;amp;gt; {
                const sourceCode = getSourceCode();
                navigator.clipboard.writeText(sourceCode)
                    .then(() =&amp;amp;amp;gt; {
                        showToast('Kod kopyalandı!');
                    })
                    .catch(err =&amp;amp;amp;gt; {
                        showToast('Kod kopyalanamadı: ' + err);
                    });
            });
            
            // Handle Enter key in modal
            wordInput.addEventListener('keypress', (e) =&amp;amp;amp;gt; {
                if (e.key === 'Enter') {
                    meaningInput.focus();
                }
            });
            
            meaningInput.addEventListener('keypress', (e) =&amp;amp;amp;gt; {
                if (e.key === 'Enter') {
                    const word = wordInput.value.trim();
                    const meaning = meaningInput.value.trim();
                    
                    if (word &amp;amp;amp;amp;&amp;amp;amp;amp; meaning) {
                        flashcards.push({ word, meaning });
                        saveFlashcards();
                        renderFlashcards();
                        addCardModal.classList.add('hidden');
                        wordInput.value = '';
                        meaningInput.value = '';
                        showToast('Kart eklendi');
                    }
                }
            });
            
            // Close modals when clicking outside
            window.addEventListener('click', (e) =&amp;amp;amp;gt; {
                if (e.target === addCardModal) {
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                }
                
                if (e.target === confirmModal) {
                    confirmModal.classList.add('hidden');
                }
                
                if (e.target === deleteCardModal) {
                    deleteCardModal.classList.add('hidden');
                    cardToDeleteIndex = -1;
                }
                
                if (e.target === jsonEditorModal) {
                    jsonEditorModal.classList.add('hidden');
                }
                
                if (e.target === sourceCodeModal) {
                    sourceCodeModal.classList.add('hidden');
                }
            });
        }
        
        // Initialize the app when the page loads
        document.addEventListener('DOMContentLoaded', init);
    &amp;amp;amp;lt;/script&amp;amp;amp;gt;
&amp;amp;amp;lt;script&amp;amp;amp;gt;(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'95024a574212513b',t:'MTc0OTk5Mjg0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&amp;amp;amp;amp;&amp;amp;amp;amp;(document.onreadystatechange=e,c())}}}})();&amp;amp;amp;lt;/script&amp;amp;amp;gt;&amp;amp;amp;lt;iframe height="1" width="1" style="position: absolute; top: 0px; left: 0px; border: none; visibility: hidden;"&amp;amp;amp;gt;&amp;amp;amp;lt;/iframe&amp;amp;amp;gt;

&amp;amp;amp;lt;/body&amp;amp;amp;gt;&amp;amp;amp;lt;/html&amp;amp;amp;gt;&amp;amp;lt;/div&amp;amp;gt;
            &amp;amp;lt;/div&amp;amp;gt;
        &amp;amp;lt;/div&amp;amp;gt;
        
        &amp;amp;lt;!-- Toast Notification --&amp;amp;gt;
        &amp;amp;lt;div id="toast" class="toast"&amp;amp;gt;Kart silindi&amp;amp;lt;/div&amp;amp;gt;
    &amp;amp;lt;/div&amp;amp;gt;

    &amp;amp;lt;script&amp;amp;gt;
        // Initialize empty flashcards array
        let flashcards = [];
        
        // Stats for quiz mode
        let stats = {
            correct: 0,
            incorrect: 0,
            total: 0
        };
        
        let currentQuizIndex = 0;
        let cardToDeleteIndex = -1;
        
        // DOM elements
        const flashcardContainer = document.getElementById('flashcardContainer');
        const quizContainer = document.getElementById('quizContainer');
        const quizContent = document.getElementById('quizContent');
        const quizEmptyState = document.getElementById('quizEmptyState');
        const emptyState = document.getElementById('emptyState');
        const flashcardModeBtn = document.getElementById('flashcardMode');
        const quizModeBtn = document.getElementById('quizMode');
        const addCardBtn = document.getElementById('addCardBtn');
        const clearCardsBtn = document.getElementById('clearCardsBtn');
        const exportCardsBtn = document.getElementById('exportCardsBtn');
        const importCardsBtn = document.getElementById('importCardsBtn');
        const jsonEditorBtn = document.getElementById('jsonEditorBtn');
        const importFileInput = document.getElementById('importFileInput');
        const viewSourceBtn = document.getElementById('viewSourceBtn');
        const addCardModal = document.getElementById('addCardModal');
        const confirmModal = document.getElementById('confirmModal');
        const deleteCardModal = document.getElementById('deleteCardModal');
        const jsonEditorModal = document.getElementById('jsonEditorModal');
        const sourceCodeModal = document.getElementById('sourceCodeModal');
        const cancelAddCardBtn = document.getElementById('cancelAddCard');
        const saveCardBtn = document.getElementById('saveCard');
        const wordInput = document.getElementById('wordInput');
        const meaningInput = document.getElementById('meaningInput');
        const emptyStateAddBtn = document.getElementById('emptyStateAddBtn');
        const emptyStateImportBtn = document.getElementById('emptyStateImportBtn');
        const quizEmptyStateAddBtn = document.getElementById('quizEmptyStateAddBtn');
        const statsBar = document.getElementById('statsBar');
        const correctCountEl = document.getElementById('correctCount');
        const incorrectCountEl = document.getElementById('incorrectCount');
        const totalCountEl = document.getElementById('totalCount');
        const nextQuestionBtn = document.getElementById('nextQuestion');
        const cancelClearBtn = document.getElementById('cancelClear');
        const confirmClearBtn = document.getElementById('confirmClear');
        const deleteCardWord = document.getElementById('deleteCardWord');
        const deleteCardMeaning = document.getElementById('deleteCardMeaning');
        const cancelDeleteCardBtn = document.getElementById('cancelDeleteCard');
        const confirmDeleteCardBtn = document.getElementById('confirmDeleteCard');
        const jsonTextarea = document.getElementById('jsonTextarea');
        const copyJsonBtn = document.getElementById('copyJsonBtn');
        const applyJsonBtn = document.getElementById('applyJsonBtn');
        const cancelJsonEditor = document.getElementById('cancelJsonEditor');
        const copySourceCodeBtn = document.getElementById('copySourceCode');
        const closeSourceCodeBtn = document.getElementById('closeSourceCode');
        const sourceCodeContent = document.getElementById('sourceCodeContent');
        const toast = document.getElementById('toast');
        
        // Initialize the app
        function init() {
            loadFlashcards();
            renderFlashcards();
            setupEventListeners();
        }
        
        // Load flashcards from localStorage
        function loadFlashcards() {
            const savedFlashcards = localStorage.getItem('englishFlashcards');
            if (savedFlashcards) {
                try {
                    flashcards = JSON.parse(savedFlashcards);
                } catch (e) {
                    console.error('Error parsing saved flashcards:', e);
                    flashcards = [];
                }
            }
        }
        
        // Save flashcards to localStorage
        function saveFlashcards() {
            localStorage.setItem('englishFlashcards', JSON.stringify(flashcards));
        }
        
        // Render all flashcards
        function renderFlashcards() {
            // Clear container except for empty state
            const cards = flashcardContainer.querySelectorAll('.flashcard');
            cards.forEach(card =&amp;amp;gt; card.remove());
            
            // Show or hide empty state
            if (flashcards.length === 0) {
                emptyState.classList.remove('hidden');
            } else {
                emptyState.classList.add('hidden');
                
                // Add flashcards
                flashcards.forEach((card, index) =&amp;amp;gt; {
                    const flashcardEl = document.createElement('div');
                    flashcardEl.className = 'flashcard';
                    flashcardEl.innerHTML = `
                        &amp;amp;lt;div class="delete-btn" data-index="${index}"&amp;amp;gt;
                            &amp;amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;amp;gt;
                                &amp;amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" /&amp;amp;gt;
                            &amp;amp;lt;/svg&amp;amp;gt;
                        &amp;amp;lt;/div&amp;amp;gt;
                        &amp;amp;lt;div class="flashcard-inner"&amp;amp;gt;
                            &amp;amp;lt;div class="flashcard-front"&amp;amp;gt;
                                &amp;amp;lt;h2 class="text-2xl font-bold text-center"&amp;amp;gt;${card.word}&amp;amp;lt;/h2&amp;amp;gt;
                            &amp;amp;lt;/div&amp;amp;gt;
                            &amp;amp;lt;div class="flashcard-back"&amp;amp;gt;
                                &amp;amp;lt;p class="text-xl text-center"&amp;amp;gt;${card.meaning}&amp;amp;lt;/p&amp;amp;gt;
                            &amp;amp;lt;/div&amp;amp;gt;
                        &amp;amp;lt;/div&amp;amp;gt;
                    `;
                    
                    // Add click event for flipping the card
                    const flashcardInner = flashcardEl.querySelector('.flashcard-inner');
                    flashcardInner.addEventListener('click', () =&amp;amp;gt; {
                        flashcardEl.classList.toggle('flipped');
                    });
                    
                    // Add click event for delete button
                    const deleteBtn = flashcardEl.querySelector('.delete-btn');
                    deleteBtn.addEventListener('click', (e) =&amp;amp;gt; {
                        e.stopPropagation(); // Prevent card flip
                        const index = parseInt(deleteBtn.getAttribute('data-index'));
                        showDeleteCardModal(index);
                    });
                    
                    flashcardContainer.appendChild(flashcardEl);
                });
            }
        }
        
        // Show delete card confirmation modal
        function showDeleteCardModal(index) {
            cardToDeleteIndex = index;
            const card = flashcards[index];
            deleteCardWord.textContent = card.word;
            deleteCardMeaning.textContent = card.meaning;
            deleteCardModal.classList.remove('hidden');
        }
        
        // Delete a single card
        function deleteCard(index) {
            if (index &amp;amp;gt;= 0 &amp;amp;amp;&amp;amp;amp; index &amp;amp;lt; flashcards.length) {
                flashcards.splice(index, 1);
                saveFlashcards();
                renderFlashcards();
                showToast('Kart silindi');
            }
        }
        
        // Export flashcards to JSON file
        function exportFlashcards() {
            const dataStr = JSON.stringify(flashcards, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = 'ingilizce_kartlarim.json';
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showToast('Kartlar dışa aktarıldı');
        }
        
        // Import flashcards from JSON file
        function importFlashcards(file) {
            const reader = new FileReader();
            
            reader.onload = function(e) {
                try {
                    const importedCards = JSON.parse(e.target.result);
                    
                    if (Array.isArray(importedCards)) {
                        // Check if each card has the required properties
                        const validCards = importedCards.filter(card =&amp;amp;gt; 
                            card &amp;amp;amp;&amp;amp;amp; typeof card === 'object' &amp;amp;amp;&amp;amp;amp; 
                            'word' in card &amp;amp;amp;&amp;amp;amp; 'meaning' in card &amp;amp;amp;&amp;amp;amp;
                            typeof card.word === 'string' &amp;amp;amp;&amp;amp;amp; 
                            typeof card.meaning === 'string'
                        );
                        
                        if (validCards.length &amp;amp;gt; 0) {
                            flashcards = validCards;
                            saveFlashcards();
                            renderFlashcards();
                            showToast(`${validCards.length} kart içe aktarıldı`);
                        } else {
                            showToast('Geçerli kart bulunamadı');
                        }
                    } else {
                        showToast('Geçersiz JSON formatı');
                    }
                } catch (error) {
                    console.error('Import error:', error);
                    showToast('Dosya okunamadı');
                }
            };
            
            reader.readAsText(file);
        }
        
        // Show JSON editor with current flashcards
        function showJsonEditor() {
            jsonTextarea.value = JSON.stringify(flashcards, null, 2);
            jsonEditorModal.classList.remove('hidden');
        }
        
        // Apply JSON from editor
        function applyJsonFromEditor() {
            try {
                const jsonData = JSON.parse(jsonTextarea.value);
                
                if (Array.isArray(jsonData)) {
                    // Check if each card has the required properties
                    const validCards = jsonData.filter(card =&amp;amp;gt; 
                        card &amp;amp;amp;&amp;amp;amp; typeof card === 'object' &amp;amp;amp;&amp;amp;amp; 
                        'word' in card &amp;amp;amp;&amp;amp;amp; 'meaning' in card &amp;amp;amp;&amp;amp;amp;
                        typeof card.word === 'string' &amp;amp;amp;&amp;amp;amp; 
                        typeof card.meaning === 'string'
                    );
                    
                    if (validCards.length &amp;amp;gt; 0) {
                        flashcards = validCards;
                        saveFlashcards();
                        renderFlashcards();
                        jsonEditorModal.classList.add('hidden');
                        showToast(`${validCards.length} kart güncellendi`);
                    } else {
                        showToast('Geçerli kart bulunamadı');
                    }
                } else {
                    showToast('Geçersiz JSON formatı');
                }
            } catch (error) {
                console.error('JSON parse error:', error);
                showToast('Geçersiz JSON formatı');
            }
        }
        
        // Setup quiz mode
        function setupQuiz() {
            currentQuizIndex = 0;
            stats.correct = 0;
            stats.incorrect = 0;
            stats.total = 0;
            updateStats();
            
            // Check if we have enough cards for quiz mode
            if (flashcards.length &amp;amp;lt; 4) {
                quizContent.classList.add('hidden');
                quizEmptyState.classList.remove('hidden');
            } else {
                quizContent.classList.remove('hidden');
                quizEmptyState.classList.add('hidden');
                showNextQuestion();
            }
        }
        
        // Show next question in quiz mode
        function showNextQuestion() {
            if (currentQuizIndex &amp;amp;gt;= flashcards.length) {
                // Reset if we've gone through all cards
                currentQuizIndex = 0;
            }
            
            const currentCard = flashcards[currentQuizIndex];
            const quizQuestion = document.getElementById('quizQuestion');
            const quizOptions = document.getElementById('quizOptions');
            
            quizQuestion.textContent = currentCard.word;
            
            // Create options (including the correct one and some random ones)
            let options = [currentCard.meaning];
            
            // Add some random options from other cards
            let availableCards = [...flashcards];
            availableCards.splice(currentQuizIndex, 1); // Remove current card
            
            // Shuffle available cards
            availableCards = shuffleArray(availableCards);
            
            // Add up to 3 more options
            for (let i = 0; i &amp;amp;lt; 3 &amp;amp;amp;&amp;amp;amp; i &amp;amp;lt; availableCards.length; i++) {
                options.push(availableCards[i].meaning);
            }
            
            // Shuffle options
            options = shuffleArray(options);
            
            // Render options
            quizOptions.innerHTML = '';
            options.forEach(option =&amp;amp;gt; {
                const optionEl = document.createElement('div');
                optionEl.className = 'quiz-option bg-gray-100 p-4 rounded-lg cursor-pointer hover:bg-gray-200';
                optionEl.textContent = option;
                
                optionEl.addEventListener('click', () =&amp;amp;gt; {
                    // Disable all options after selection
                    document.querySelectorAll('.quiz-option').forEach(el =&amp;amp;gt; {
                        el.style.pointerEvents = 'none';
                    });
                    
                    if (option === currentCard.meaning) {
                        optionEl.classList.add('correct');
                        stats.correct++;
                    } else {
                        optionEl.classList.add('incorrect');
                        stats.incorrect++;
                        
                        // Highlight the correct answer
                        document.querySelectorAll('.quiz-option').forEach(el =&amp;amp;gt; {
                            if (el.textContent === currentCard.meaning) {
                                el.classList.add('correct');
                            }
                        });
                    }
                    
                    stats.total++;
                    updateStats();
                });
                
                quizOptions.appendChild(optionEl);
            });
        }
        
        // Update stats display
        function updateStats() {
            correctCountEl.textContent = stats.correct;
            incorrectCountEl.textContent = stats.incorrect;
            totalCountEl.textContent = stats.total;
        }
        
        // Helper function to shuffle an array
        function shuffleArray(array) {
            const newArray = [...array];
            for (let i = newArray.length - 1; i &amp;amp;gt; 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
            }
            return newArray;
        }
        
        // Show toast notification
        function showToast(message) {
            toast.textContent = message;
            toast.classList.add('show');
            
            setTimeout(() =&amp;amp;gt; {
                toast.classList.remove('show');
            }, 3000);
        }
        
        // Get source code of the current page
        function getSourceCode() {
            return document.documentElement.outerHTML;
        }
        
        // Setup event listeners
        function setupEventListeners() {
            // Mode switching
            flashcardModeBtn.addEventListener('click', () =&amp;amp;gt; {
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            quizModeBtn.addEventListener('click', () =&amp;amp;gt; {
                flashcardContainer.classList.add('hidden');
                quizContainer.classList.remove('hidden');
                statsBar.classList.remove('hidden');
                quizModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                quizModeBtn.classList.replace('text-gray-700', 'text-white');
                flashcardModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                flashcardModeBtn.classList.replace('text-white', 'text-gray-700');
                setupQuiz();
            });
            
            // Next question button
            nextQuestionBtn.addEventListener('click', () =&amp;amp;gt; {
                currentQuizIndex++;
                showNextQuestion();
            });
            
            // Add card buttons
            addCardBtn.addEventListener('click', () =&amp;amp;gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateAddBtn.addEventListener('click', () =&amp;amp;gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateImportBtn.addEventListener('click', () =&amp;amp;gt; {
                importFileInput.click();
            });
            
            quizEmptyStateAddBtn.addEventListener('click', () =&amp;amp;gt; {
                addCardModal.classList.remove('hidden');
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            cancelAddCardBtn.addEventListener('click', () =&amp;amp;gt; {
                addCardModal.classList.add('hidden');
                wordInput.value = '';
                meaningInput.value = '';
            });
            
            saveCardBtn.addEventListener('click', () =&amp;amp;gt; {
                const word = wordInput.value.trim();
                const meaning = meaningInput.value.trim();
                
                if (word &amp;amp;amp;&amp;amp;amp; meaning) {
                    flashcards.push({ word, meaning });
                    saveFlashcards();
                    renderFlashcards();
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                    showToast('Kart eklendi');
                }
            });
            
            // Clear cards functionality
            clearCardsBtn.addEventListener('click', () =&amp;amp;gt; {
                if (flashcards.length &amp;amp;gt; 0) {
                    confirmModal.classList.remove('hidden');
                }
            });
            
            cancelClearBtn.addEventListener('click', () =&amp;amp;gt; {
                confirmModal.classList.add('hidden');
            });
            
            confirmClearBtn.addEventListener('click', () =&amp;amp;gt; {
                flashcards = [];
                saveFlashcards();
                renderFlashcards();
                confirmModal.classList.add('hidden');
                showToast('Tüm kartlar silindi');
            });
            
            // Delete single card functionality
            cancelDeleteCardBtn.addEventListener('click', () =&amp;amp;gt; {
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            confirmDeleteCardBtn.addEventListener('click', () =&amp;amp;gt; {
                deleteCard(cardToDeleteIndex);
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            // Export/Import functionality
            exportCardsBtn.addEventListener('click', () =&amp;amp;gt; {
                exportFlashcards();
            });
            
            importCardsBtn.addEventListener('click', () =&amp;amp;gt; {
                importFileInput.click();
            });
            
            importFileInput.addEventListener('change', (e) =&amp;amp;gt; {
                if (e.target.files.length &amp;amp;gt; 0) {
                    importFlashcards(e.target.files[0]);
                    // Reset the input so the same file can be selected again
                    e.target.value = '';
                }
            });
            
            // JSON Editor functionality
            jsonEditorBtn.addEventListener('click', () =&amp;amp;gt; {
                showJsonEditor();
            });
            
            copyJsonBtn.addEventListener('click', () =&amp;amp;gt; {
                jsonTextarea.select();
                document.execCommand('copy');
                showToast('JSON kopyalandı');
            });
            
            applyJsonBtn.addEventListener('click', () =&amp;amp;gt; {
                applyJsonFromEditor();
            });
            
            cancelJsonEditor.addEventListener('click', () =&amp;amp;gt; {
                jsonEditorModal.classList.add('hidden');
            });
            
            // Source code functionality
            viewSourceBtn.addEventListener('click', () =&amp;amp;gt; {
                sourceCodeContent.textContent = getSourceCode();
                sourceCodeModal.classList.remove('hidden');
            });
            
            closeSourceCodeBtn.addEventListener('click', () =&amp;amp;gt; {
                sourceCodeModal.classList.add('hidden');
            });
            
            copySourceCodeBtn.addEventListener('click', () =&amp;amp;gt; {
                const sourceCode = getSourceCode();
                navigator.clipboard.writeText(sourceCode)
                    .then(() =&amp;amp;gt; {
                        showToast('Kod kopyalandı!');
                    })
                    .catch(err =&amp;amp;gt; {
                        showToast('Kod kopyalanamadı: ' + err);
                    });
            });
            
            // Handle Enter key in modal
            wordInput.addEventListener('keypress', (e) =&amp;amp;gt; {
                if (e.key === 'Enter') {
                    meaningInput.focus();
                }
            });
            
            meaningInput.addEventListener('keypress', (e) =&amp;amp;gt; {
                if (e.key === 'Enter') {
                    const word = wordInput.value.trim();
                    const meaning = meaningInput.value.trim();
                    
                    if (word &amp;amp;amp;&amp;amp;amp; meaning) {
                        flashcards.push({ word, meaning });
                        saveFlashcards();
                        renderFlashcards();
                        addCardModal.classList.add('hidden');
                        wordInput.value = '';
                        meaningInput.value = '';
                        showToast('Kart eklendi');
                    }
                }
            });
            
            // Close modals when clicking outside
            window.addEventListener('click', (e) =&amp;amp;gt; {
                if (e.target === addCardModal) {
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                }
                
                if (e.target === confirmModal) {
                    confirmModal.classList.add('hidden');
                }
                
                if (e.target === deleteCardModal) {
                    deleteCardModal.classList.add('hidden');
                    cardToDeleteIndex = -1;
                }
                
                if (e.target === jsonEditorModal) {
                    jsonEditorModal.classList.add('hidden');
                }
                
                if (e.target === sourceCodeModal) {
                    sourceCodeModal.classList.add('hidden');
                }
            });
        }
        
        // Initialize the app when the page loads
        document.addEventListener('DOMContentLoaded', init);
    &amp;amp;lt;/script&amp;amp;gt;
&amp;amp;lt;script&amp;amp;gt;(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'95024a574212513b',t:'MTc0OTk5Mjg0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&amp;amp;amp;&amp;amp;amp;(document.onreadystatechange=e,c())}}}})();&amp;amp;lt;/script&amp;amp;gt;&amp;amp;lt;iframe height="1" width="1" style="position: absolute; top: 0px; left: 0px; border: none; visibility: hidden;"&amp;amp;gt;&amp;amp;lt;/iframe&amp;amp;gt;

&amp;amp;lt;/body&amp;amp;gt;&amp;amp;lt;/html&amp;amp;gt;&amp;lt;/div&amp;gt;
            &amp;lt;/div&amp;gt;
        &amp;lt;/div&amp;gt;
        
        &amp;lt;!-- Toast Notification --&amp;gt;
        &amp;lt;div id="toast" class="toast"&amp;gt;Kart silindi&amp;lt;/div&amp;gt;
    &amp;lt;/div&amp;gt;

    &amp;lt;script&amp;gt;
        // Initialize empty flashcards array
        let flashcards = [];
        
        // Stats for quiz mode
        let stats = {
            correct: 0,
            incorrect: 0,
            total: 0
        };
        
        let currentQuizIndex = 0;
        let cardToDeleteIndex = -1;
        
        // DOM elements
        const flashcardContainer = document.getElementById('flashcardContainer');
        const quizContainer = document.getElementById('quizContainer');
        const quizContent = document.getElementById('quizContent');
        const quizEmptyState = document.getElementById('quizEmptyState');
        const emptyState = document.getElementById('emptyState');
        const flashcardModeBtn = document.getElementById('flashcardMode');
        const quizModeBtn = document.getElementById('quizMode');
        const addCardBtn = document.getElementById('addCardBtn');
        const clearCardsBtn = document.getElementById('clearCardsBtn');
        const exportCardsBtn = document.getElementById('exportCardsBtn');
        const importCardsBtn = document.getElementById('importCardsBtn');
        const jsonEditorBtn = document.getElementById('jsonEditorBtn');
        const importFileInput = document.getElementById('importFileInput');
        const viewSourceBtn = document.getElementById('viewSourceBtn');
        const addCardModal = document.getElementById('addCardModal');
        const confirmModal = document.getElementById('confirmModal');
        const deleteCardModal = document.getElementById('deleteCardModal');
        const jsonEditorModal = document.getElementById('jsonEditorModal');
        const sourceCodeModal = document.getElementById('sourceCodeModal');
        const cancelAddCardBtn = document.getElementById('cancelAddCard');
        const saveCardBtn = document.getElementById('saveCard');
        const wordInput = document.getElementById('wordInput');
        const meaningInput = document.getElementById('meaningInput');
        const emptyStateAddBtn = document.getElementById('emptyStateAddBtn');
        const emptyStateImportBtn = document.getElementById('emptyStateImportBtn');
        const quizEmptyStateAddBtn = document.getElementById('quizEmptyStateAddBtn');
        const statsBar = document.getElementById('statsBar');
        const correctCountEl = document.getElementById('correctCount');
        const incorrectCountEl = document.getElementById('incorrectCount');
        const totalCountEl = document.getElementById('totalCount');
        const nextQuestionBtn = document.getElementById('nextQuestion');
        const cancelClearBtn = document.getElementById('cancelClear');
        const confirmClearBtn = document.getElementById('confirmClear');
        const deleteCardWord = document.getElementById('deleteCardWord');
        const deleteCardMeaning = document.getElementById('deleteCardMeaning');
        const cancelDeleteCardBtn = document.getElementById('cancelDeleteCard');
        const confirmDeleteCardBtn = document.getElementById('confirmDeleteCard');
        const jsonTextarea = document.getElementById('jsonTextarea');
        const copyJsonBtn = document.getElementById('copyJsonBtn');
        const applyJsonBtn = document.getElementById('applyJsonBtn');
        const cancelJsonEditor = document.getElementById('cancelJsonEditor');
        const copySourceCodeBtn = document.getElementById('copySourceCode');
        const closeSourceCodeBtn = document.getElementById('closeSourceCode');
        const sourceCodeContent = document.getElementById('sourceCodeContent');
        const toast = document.getElementById('toast');
        
        // Initialize the app
        function init() {
            loadFlashcards();
            renderFlashcards();
            setupEventListeners();
        }
        
        // Load flashcards from localStorage
        function loadFlashcards() {
            const savedFlashcards = localStorage.getItem('englishFlashcards');
            if (savedFlashcards) {
                try {
                    flashcards = JSON.parse(savedFlashcards);
                } catch (e) {
                    console.error('Error parsing saved flashcards:', e);
                    flashcards = [];
                }
            }
        }
        
        // Save flashcards to localStorage
        function saveFlashcards() {
            localStorage.setItem('englishFlashcards', JSON.stringify(flashcards));
        }
        
        // Render all flashcards
        function renderFlashcards() {
            // Clear container except for empty state
            const cards = flashcardContainer.querySelectorAll('.flashcard');
            cards.forEach(card =&amp;gt; card.remove());
            
            // Show or hide empty state
            if (flashcards.length === 0) {
                emptyState.classList.remove('hidden');
            } else {
                emptyState.classList.add('hidden');
                
                // Add flashcards
                flashcards.forEach((card, index) =&amp;gt; {
                    const flashcardEl = document.createElement('div');
                    flashcardEl.className = 'flashcard';
                    flashcardEl.innerHTML = `
                        &amp;lt;div class="delete-btn" data-index="${index}"&amp;gt;
                            &amp;lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"&amp;gt;
                                &amp;lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" /&amp;gt;
                            &amp;lt;/svg&amp;gt;
                        &amp;lt;/div&amp;gt;
                        &amp;lt;div class="flashcard-inner"&amp;gt;
                            &amp;lt;div class="flashcard-front"&amp;gt;
                                &amp;lt;h2 class="text-2xl font-bold text-center"&amp;gt;${card.word}&amp;lt;/h2&amp;gt;
                            &amp;lt;/div&amp;gt;
                            &amp;lt;div class="flashcard-back"&amp;gt;
                                &amp;lt;p class="text-xl text-center"&amp;gt;${card.meaning}&amp;lt;/p&amp;gt;
                            &amp;lt;/div&amp;gt;
                        &amp;lt;/div&amp;gt;
                    `;
                    
                    // Add click event for flipping the card
                    const flashcardInner = flashcardEl.querySelector('.flashcard-inner');
                    flashcardInner.addEventListener('click', () =&amp;gt; {
                        flashcardEl.classList.toggle('flipped');
                    });
                    
                    // Add click event for delete button
                    const deleteBtn = flashcardEl.querySelector('.delete-btn');
                    deleteBtn.addEventListener('click', (e) =&amp;gt; {
                        e.stopPropagation(); // Prevent card flip
                        const index = parseInt(deleteBtn.getAttribute('data-index'));
                        showDeleteCardModal(index);
                    });
                    
                    flashcardContainer.appendChild(flashcardEl);
                });
            }
        }
        
        // Show delete card confirmation modal
        function showDeleteCardModal(index) {
            cardToDeleteIndex = index;
            const card = flashcards[index];
            deleteCardWord.textContent = card.word;
            deleteCardMeaning.textContent = card.meaning;
            deleteCardModal.classList.remove('hidden');
        }
        
        // Delete a single card
        function deleteCard(index) {
            if (index &amp;gt;= 0 &amp;amp;&amp;amp; index &amp;lt; flashcards.length) {
                flashcards.splice(index, 1);
                saveFlashcards();
                renderFlashcards();
                showToast('Kart silindi');
            }
        }
        
        // Export flashcards to JSON file
        function exportFlashcards() {
            const dataStr = JSON.stringify(flashcards, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = 'ingilizce_kartlarim.json';
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showToast('Kartlar dışa aktarıldı');
        }
        
        // Import flashcards from JSON file
        function importFlashcards(file) {
            const reader = new FileReader();
            
            reader.onload = function(e) {
                try {
                    const importedCards = JSON.parse(e.target.result);
                    
                    if (Array.isArray(importedCards)) {
                        // Check if each card has the required properties
                        const validCards = importedCards.filter(card =&amp;gt; 
                            card &amp;amp;&amp;amp; typeof card === 'object' &amp;amp;&amp;amp; 
                            'word' in card &amp;amp;&amp;amp; 'meaning' in card &amp;amp;&amp;amp;
                            typeof card.word === 'string' &amp;amp;&amp;amp; 
                            typeof card.meaning === 'string'
                        );
                        
                        if (validCards.length &amp;gt; 0) {
                            flashcards = validCards;
                            saveFlashcards();
                            renderFlashcards();
                            showToast(`${validCards.length} kart içe aktarıldı`);
                        } else {
                            showToast('Geçerli kart bulunamadı');
                        }
                    } else {
                        showToast('Geçersiz JSON formatı');
                    }
                } catch (error) {
                    console.error('Import error:', error);
                    showToast('Dosya okunamadı');
                }
            };
            
            reader.readAsText(file);
        }
        
        // Show JSON editor with current flashcards
        function showJsonEditor() {
            jsonTextarea.value = JSON.stringify(flashcards, null, 2);
            jsonEditorModal.classList.remove('hidden');
        }
        
        // Apply JSON from editor
        function applyJsonFromEditor() {
            try {
                const jsonData = JSON.parse(jsonTextarea.value);
                
                if (Array.isArray(jsonData)) {
                    // Check if each card has the required properties
                    const validCards = jsonData.filter(card =&amp;gt; 
                        card &amp;amp;&amp;amp; typeof card === 'object' &amp;amp;&amp;amp; 
                        'word' in card &amp;amp;&amp;amp; 'meaning' in card &amp;amp;&amp;amp;
                        typeof card.word === 'string' &amp;amp;&amp;amp; 
                        typeof card.meaning === 'string'
                    );
                    
                    if (validCards.length &amp;gt; 0) {
                        flashcards = validCards;
                        saveFlashcards();
                        renderFlashcards();
                        jsonEditorModal.classList.add('hidden');
                        showToast(`${validCards.length} kart güncellendi`);
                    } else {
                        showToast('Geçerli kart bulunamadı');
                    }
                } else {
                    showToast('Geçersiz JSON formatı');
                }
            } catch (error) {
                console.error('JSON parse error:', error);
                showToast('Geçersiz JSON formatı');
            }
        }
        
        // Setup quiz mode
        function setupQuiz() {
            currentQuizIndex = 0;
            stats.correct = 0;
            stats.incorrect = 0;
            stats.total = 0;
            updateStats();
            
            // Check if we have enough cards for quiz mode
            if (flashcards.length &amp;lt; 4) {
                quizContent.classList.add('hidden');
                quizEmptyState.classList.remove('hidden');
            } else {
                quizContent.classList.remove('hidden');
                quizEmptyState.classList.add('hidden');
                showNextQuestion();
            }
        }
        
        // Show next question in quiz mode
        function showNextQuestion() {
            if (currentQuizIndex &amp;gt;= flashcards.length) {
                // Reset if we've gone through all cards
                currentQuizIndex = 0;
            }
            
            const currentCard = flashcards[currentQuizIndex];
            const quizQuestion = document.getElementById('quizQuestion');
            const quizOptions = document.getElementById('quizOptions');
            
            quizQuestion.textContent = currentCard.word;
            
            // Create options (including the correct one and some random ones)
            let options = [currentCard.meaning];
            
            // Add some random options from other cards
            let availableCards = [...flashcards];
            availableCards.splice(currentQuizIndex, 1); // Remove current card
            
            // Shuffle available cards
            availableCards = shuffleArray(availableCards);
            
            // Add up to 3 more options
            for (let i = 0; i &amp;lt; 3 &amp;amp;&amp;amp; i &amp;lt; availableCards.length; i++) {
                options.push(availableCards[i].meaning);
            }
            
            // Shuffle options
            options = shuffleArray(options);
            
            // Render options
            quizOptions.innerHTML = '';
            options.forEach(option =&amp;gt; {
                const optionEl = document.createElement('div');
                optionEl.className = 'quiz-option bg-gray-100 p-4 rounded-lg cursor-pointer hover:bg-gray-200';
                optionEl.textContent = option;
                
                optionEl.addEventListener('click', () =&amp;gt; {
                    // Disable all options after selection
                    document.querySelectorAll('.quiz-option').forEach(el =&amp;gt; {
                        el.style.pointerEvents = 'none';
                    });
                    
                    if (option === currentCard.meaning) {
                        optionEl.classList.add('correct');
                        stats.correct++;
                    } else {
                        optionEl.classList.add('incorrect');
                        stats.incorrect++;
                        
                        // Highlight the correct answer
                        document.querySelectorAll('.quiz-option').forEach(el =&amp;gt; {
                            if (el.textContent === currentCard.meaning) {
                                el.classList.add('correct');
                            }
                        });
                    }
                    
                    stats.total++;
                    updateStats();
                });
                
                quizOptions.appendChild(optionEl);
            });
        }
        
        // Update stats display
        function updateStats() {
            correctCountEl.textContent = stats.correct;
            incorrectCountEl.textContent = stats.incorrect;
            totalCountEl.textContent = stats.total;
        }
        
        // Helper function to shuffle an array
        function shuffleArray(array) {
            const newArray = [...array];
            for (let i = newArray.length - 1; i &amp;gt; 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
            }
            return newArray;
        }
        
        // Show toast notification
        function showToast(message) {
            toast.textContent = message;
            toast.classList.add('show');
            
            setTimeout(() =&amp;gt; {
                toast.classList.remove('show');
            }, 3000);
        }
        
        // Get source code of the current page
        function getSourceCode() {
            return document.documentElement.outerHTML;
        }
        
        // Setup event listeners
        function setupEventListeners() {
            // Mode switching
            flashcardModeBtn.addEventListener('click', () =&amp;gt; {
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            quizModeBtn.addEventListener('click', () =&amp;gt; {
                flashcardContainer.classList.add('hidden');
                quizContainer.classList.remove('hidden');
                statsBar.classList.remove('hidden');
                quizModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                quizModeBtn.classList.replace('text-gray-700', 'text-white');
                flashcardModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                flashcardModeBtn.classList.replace('text-white', 'text-gray-700');
                setupQuiz();
            });
            
            // Next question button
            nextQuestionBtn.addEventListener('click', () =&amp;gt; {
                currentQuizIndex++;
                showNextQuestion();
            });
            
            // Add card buttons
            addCardBtn.addEventListener('click', () =&amp;gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateAddBtn.addEventListener('click', () =&amp;gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateImportBtn.addEventListener('click', () =&amp;gt; {
                importFileInput.click();
            });
            
            quizEmptyStateAddBtn.addEventListener('click', () =&amp;gt; {
                addCardModal.classList.remove('hidden');
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            cancelAddCardBtn.addEventListener('click', () =&amp;gt; {
                addCardModal.classList.add('hidden');
                wordInput.value = '';
                meaningInput.value = '';
            });
            
            saveCardBtn.addEventListener('click', () =&amp;gt; {
                const word = wordInput.value.trim();
                const meaning = meaningInput.value.trim();
                
                if (word &amp;amp;&amp;amp; meaning) {
                    flashcards.push({ word, meaning });
                    saveFlashcards();
                    renderFlashcards();
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                    showToast('Kart eklendi');
                }
            });
            
            // Clear cards functionality
            clearCardsBtn.addEventListener('click', () =&amp;gt; {
                if (flashcards.length &amp;gt; 0) {
                    confirmModal.classList.remove('hidden');
                }
            });
            
            cancelClearBtn.addEventListener('click', () =&amp;gt; {
                confirmModal.classList.add('hidden');
            });
            
            confirmClearBtn.addEventListener('click', () =&amp;gt; {
                flashcards = [];
                saveFlashcards();
                renderFlashcards();
                confirmModal.classList.add('hidden');
                showToast('Tüm kartlar silindi');
            });
            
            // Delete single card functionality
            cancelDeleteCardBtn.addEventListener('click', () =&amp;gt; {
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            confirmDeleteCardBtn.addEventListener('click', () =&amp;gt; {
                deleteCard(cardToDeleteIndex);
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            // Export/Import functionality
            exportCardsBtn.addEventListener('click', () =&amp;gt; {
                exportFlashcards();
            });
            
            importCardsBtn.addEventListener('click', () =&amp;gt; {
                importFileInput.click();
            });
            
            importFileInput.addEventListener('change', (e) =&amp;gt; {
                if (e.target.files.length &amp;gt; 0) {
                    importFlashcards(e.target.files[0]);
                    // Reset the input so the same file can be selected again
                    e.target.value = '';
                }
            });
            
            // JSON Editor functionality
            jsonEditorBtn.addEventListener('click', () =&amp;gt; {
                showJsonEditor();
            });
            
            copyJsonBtn.addEventListener('click', () =&amp;gt; {
                jsonTextarea.select();
                document.execCommand('copy');
                showToast('JSON kopyalandı');
            });
            
            applyJsonBtn.addEventListener('click', () =&amp;gt; {
                applyJsonFromEditor();
            });
            
            cancelJsonEditor.addEventListener('click', () =&amp;gt; {
                jsonEditorModal.classList.add('hidden');
            });
            
            // Source code functionality
            viewSourceBtn.addEventListener('click', () =&amp;gt; {
                sourceCodeContent.textContent = getSourceCode();
                sourceCodeModal.classList.remove('hidden');
            });
            
            closeSourceCodeBtn.addEventListener('click', () =&amp;gt; {
                sourceCodeModal.classList.add('hidden');
            });
            
            copySourceCodeBtn.addEventListener('click', () =&amp;gt; {
                const sourceCode = getSourceCode();
                navigator.clipboard.writeText(sourceCode)
                    .then(() =&amp;gt; {
                        showToast('Kod kopyalandı!');
                    })
                    .catch(err =&amp;gt; {
                        showToast('Kod kopyalanamadı: ' + err);
                    });
            });
            
            // Handle Enter key in modal
            wordInput.addEventListener('keypress', (e) =&amp;gt; {
                if (e.key === 'Enter') {
                    meaningInput.focus();
                }
            });
            
            meaningInput.addEventListener('keypress', (e) =&amp;gt; {
                if (e.key === 'Enter') {
                    const word = wordInput.value.trim();
                    const meaning = meaningInput.value.trim();
                    
                    if (word &amp;amp;&amp;amp; meaning) {
                        flashcards.push({ word, meaning });
                        saveFlashcards();
                        renderFlashcards();
                        addCardModal.classList.add('hidden');
                        wordInput.value = '';
                        meaningInput.value = '';
                        showToast('Kart eklendi');
                    }
                }
            });
            
            // Close modals when clicking outside
            window.addEventListener('click', (e) =&amp;gt; {
                if (e.target === addCardModal) {
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                }
                
                if (e.target === confirmModal) {
                    confirmModal.classList.add('hidden');
                }
                
                if (e.target === deleteCardModal) {
                    deleteCardModal.classList.add('hidden');
                    cardToDeleteIndex = -1;
                }
                
                if (e.target === jsonEditorModal) {
                    jsonEditorModal.classList.add('hidden');
                }
                
                if (e.target === sourceCodeModal) {
                    sourceCodeModal.classList.add('hidden');
                }
            });
        }
        
        // Initialize the app when the page loads
        document.addEventListener('DOMContentLoaded', init);
    &amp;lt;/script&amp;gt;
&amp;lt;script&amp;gt;(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'95024a574212513b',t:'MTc0OTk5Mjg0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&amp;amp;&amp;amp;(document.onreadystatechange=e,c())}}}})();&amp;lt;/script&amp;gt;&amp;lt;iframe height="1" width="1" style="position: absolute; top: 0px; left: 0px; border: none; visibility: hidden;"&amp;gt;&amp;lt;/iframe&amp;gt;

&amp;lt;/body&amp;gt;&amp;lt;/html&amp;gt;&lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        
        &lt;!-- Toast Notification --&gt;
        &lt;div id="toast" class="toast"&gt;Kart silindi&lt;/div&gt;
    &lt;/div&gt;

    &lt;script&gt;
        // Initialize empty flashcards array
        let flashcards = [];
        
        // Stats for quiz mode
        let stats = {
            correct: 0,
            incorrect: 0,
            total: 0
        };
        
        let currentQuizIndex = 0;
        let cardToDeleteIndex = -1;
        
        // DOM elements
        const flashcardContainer = document.getElementById('flashcardContainer');
        const quizContainer = document.getElementById('quizContainer');
        const quizContent = document.getElementById('quizContent');
        const quizEmptyState = document.getElementById('quizEmptyState');
        const emptyState = document.getElementById('emptyState');
        const flashcardModeBtn = document.getElementById('flashcardMode');
        const quizModeBtn = document.getElementById('quizMode');
        const addCardBtn = document.getElementById('addCardBtn');
        const clearCardsBtn = document.getElementById('clearCardsBtn');
        const exportCardsBtn = document.getElementById('exportCardsBtn');
        const importCardsBtn = document.getElementById('importCardsBtn');
        const jsonEditorBtn = document.getElementById('jsonEditorBtn');
        const importFileInput = document.getElementById('importFileInput');
        const viewSourceBtn = document.getElementById('viewSourceBtn');
        const addCardModal = document.getElementById('addCardModal');
        const confirmModal = document.getElementById('confirmModal');
        const deleteCardModal = document.getElementById('deleteCardModal');
        const jsonEditorModal = document.getElementById('jsonEditorModal');
        const sourceCodeModal = document.getElementById('sourceCodeModal');
        const cancelAddCardBtn = document.getElementById('cancelAddCard');
        const saveCardBtn = document.getElementById('saveCard');
        const wordInput = document.getElementById('wordInput');
        const meaningInput = document.getElementById('meaningInput');
        const emptyStateAddBtn = document.getElementById('emptyStateAddBtn');
        const emptyStateImportBtn = document.getElementById('emptyStateImportBtn');
        const quizEmptyStateAddBtn = document.getElementById('quizEmptyStateAddBtn');
        const statsBar = document.getElementById('statsBar');
        const correctCountEl = document.getElementById('correctCount');
        const incorrectCountEl = document.getElementById('incorrectCount');
        const totalCountEl = document.getElementById('totalCount');
        const nextQuestionBtn = document.getElementById('nextQuestion');
        const cancelClearBtn = document.getElementById('cancelClear');
        const confirmClearBtn = document.getElementById('confirmClear');
        const deleteCardWord = document.getElementById('deleteCardWord');
        const deleteCardMeaning = document.getElementById('deleteCardMeaning');
        const cancelDeleteCardBtn = document.getElementById('cancelDeleteCard');
        const confirmDeleteCardBtn = document.getElementById('confirmDeleteCard');
        const jsonTextarea = document.getElementById('jsonTextarea');
        const copyJsonBtn = document.getElementById('copyJsonBtn');
        const applyJsonBtn = document.getElementById('applyJsonBtn');
        const cancelJsonEditor = document.getElementById('cancelJsonEditor');
        const copySourceCodeBtn = document.getElementById('copySourceCode');
        const closeSourceCodeBtn = document.getElementById('closeSourceCode');
        const sourceCodeContent = document.getElementById('sourceCodeContent');
        const toast = document.getElementById('toast');
        
        // Initialize the app
        function init() {
            loadFlashcards();
            renderFlashcards();
            setupEventListeners();
        }
        
        // Load flashcards from localStorage
        function loadFlashcards() {
            const savedFlashcards = localStorage.getItem('englishFlashcards');
            if (savedFlashcards) {
                try {
                    flashcards = JSON.parse(savedFlashcards);
                } catch (e) {
                    console.error('Error parsing saved flashcards:', e);
                    flashcards = [];
                }
            }
        }
        
        // Save flashcards to localStorage
        function saveFlashcards() {
            localStorage.setItem('englishFlashcards', JSON.stringify(flashcards));
        }
        
        // Render all flashcards
        function renderFlashcards() {
            // Clear container except for empty state
            const cards = flashcardContainer.querySelectorAll('.flashcard');
            cards.forEach(card =&gt; card.remove());
            
            // Show or hide empty state
            if (flashcards.length === 0) {
                emptyState.classList.remove('hidden');
            } else {
                emptyState.classList.add('hidden');
                
                // Add flashcards
                flashcards.forEach((card, index) =&gt; {
                    const flashcardEl = document.createElement('div');
                    flashcardEl.className = 'flashcard';
                    flashcardEl.innerHTML = `
                        &lt;div class="delete-btn" data-index="${index}"&gt;
                            &lt;svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"&gt;
                                &lt;path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" /&gt;
                            &lt;/svg&gt;
                        &lt;/div&gt;
                        &lt;div class="flashcard-inner"&gt;
                            &lt;div class="flashcard-front"&gt;
                                &lt;h2 class="text-2xl font-bold text-center"&gt;${card.word}&lt;/h2&gt;
                            &lt;/div&gt;
                            &lt;div class="flashcard-back"&gt;
                                &lt;p class="text-xl text-center"&gt;${card.meaning}&lt;/p&gt;
                            &lt;/div&gt;
                        &lt;/div&gt;
                    `;
                    
                    // Add click event for flipping the card
                    const flashcardInner = flashcardEl.querySelector('.flashcard-inner');
                    flashcardInner.addEventListener('click', () =&gt; {
                        flashcardEl.classList.toggle('flipped');
                    });
                    
                    // Add click event for delete button
                    const deleteBtn = flashcardEl.querySelector('.delete-btn');
                    deleteBtn.addEventListener('click', (e) =&gt; {
                        e.stopPropagation(); // Prevent card flip
                        const index = parseInt(deleteBtn.getAttribute('data-index'));
                        showDeleteCardModal(index);
                    });
                    
                    flashcardContainer.appendChild(flashcardEl);
                });
            }
        }
        
        // Show delete card confirmation modal
        function showDeleteCardModal(index) {
            cardToDeleteIndex = index;
            const card = flashcards[index];
            deleteCardWord.textContent = card.word;
            deleteCardMeaning.textContent = card.meaning;
            deleteCardModal.classList.remove('hidden');
        }
        
        // Delete a single card
        function deleteCard(index) {
            if (index &gt;= 0 &amp;&amp; index &lt; flashcards.length) {
                flashcards.splice(index, 1);
                saveFlashcards();
                renderFlashcards();
                showToast('Kart silindi');
            }
        }
        
        // Export flashcards to JSON file
        function exportFlashcards() {
            const dataStr = JSON.stringify(flashcards, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = 'ingilizce_kartlarim.json';
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showToast('Kartlar dışa aktarıldı');
        }
        
        // Import flashcards from JSON file
        function importFlashcards(file) {
            const reader = new FileReader();
            
            reader.onload = function(e) {
                try {
                    const importedCards = JSON.parse(e.target.result);
                    
                    if (Array.isArray(importedCards)) {
                        // Check if each card has the required properties
                        const validCards = importedCards.filter(card =&gt; 
                            card &amp;&amp; typeof card === 'object' &amp;&amp; 
                            'word' in card &amp;&amp; 'meaning' in card &amp;&amp;
                            typeof card.word === 'string' &amp;&amp; 
                            typeof card.meaning === 'string'
                        );
                        
                        if (validCards.length &gt; 0) {
                            flashcards = validCards;
                            saveFlashcards();
                            renderFlashcards();
                            showToast(`${validCards.length} kart içe aktarıldı`);
                        } else {
                            showToast('Geçerli kart bulunamadı');
                        }
                    } else {
                        showToast('Geçersiz JSON formatı');
                    }
                } catch (error) {
                    console.error('Import error:', error);
                    showToast('Dosya okunamadı');
                }
            };
            
            reader.readAsText(file);
        }
        
        // Show JSON editor with current flashcards
        function showJsonEditor() {
            jsonTextarea.value = JSON.stringify(flashcards, null, 2);
            jsonEditorModal.classList.remove('hidden');
        }
        
        // Apply JSON from editor
        function applyJsonFromEditor() {
            try {
                const jsonData = JSON.parse(jsonTextarea.value);
                
                if (Array.isArray(jsonData)) {
                    // Check if each card has the required properties
                    const validCards = jsonData.filter(card =&gt; 
                        card &amp;&amp; typeof card === 'object' &amp;&amp; 
                        'word' in card &amp;&amp; 'meaning' in card &amp;&amp;
                        typeof card.word === 'string' &amp;&amp; 
                        typeof card.meaning === 'string'
                    );
                    
                    if (validCards.length &gt; 0) {
                        flashcards = validCards;
                        saveFlashcards();
                        renderFlashcards();
                        jsonEditorModal.classList.add('hidden');
                        showToast(`${validCards.length} kart güncellendi`);
                    } else {
                        showToast('Geçerli kart bulunamadı');
                    }
                } else {
                    showToast('Geçersiz JSON formatı');
                }
            } catch (error) {
                console.error('JSON parse error:', error);
                showToast('Geçersiz JSON formatı');
            }
        }
        
        // Setup quiz mode
        function setupQuiz() {
            currentQuizIndex = 0;
            stats.correct = 0;
            stats.incorrect = 0;
            stats.total = 0;
            updateStats();
            
            // Check if we have enough cards for quiz mode
            if (flashcards.length &lt; 4) {
                quizContent.classList.add('hidden');
                quizEmptyState.classList.remove('hidden');
            } else {
                quizContent.classList.remove('hidden');
                quizEmptyState.classList.add('hidden');
                showNextQuestion();
            }
        }
        
        // Show next question in quiz mode
        function showNextQuestion() {
            if (currentQuizIndex &gt;= flashcards.length) {
                // Reset if we've gone through all cards
                currentQuizIndex = 0;
            }
            
            const currentCard = flashcards[currentQuizIndex];
            const quizQuestion = document.getElementById('quizQuestion');
            const quizOptions = document.getElementById('quizOptions');
            
            quizQuestion.textContent = currentCard.word;
            
            // Create options (including the correct one and some random ones)
            let options = [currentCard.meaning];
            
            // Add some random options from other cards
            let availableCards = [...flashcards];
            availableCards.splice(currentQuizIndex, 1); // Remove current card
            
            // Shuffle available cards
            availableCards = shuffleArray(availableCards);
            
            // Add up to 3 more options
            for (let i = 0; i &lt; 3 &amp;&amp; i &lt; availableCards.length; i++) {
                options.push(availableCards[i].meaning);
            }
            
            // Shuffle options
            options = shuffleArray(options);
            
            // Render options
            quizOptions.innerHTML = '';
            options.forEach(option =&gt; {
                const optionEl = document.createElement('div');
                optionEl.className = 'quiz-option bg-gray-100 p-4 rounded-lg cursor-pointer hover:bg-gray-200';
                optionEl.textContent = option;
                
                optionEl.addEventListener('click', () =&gt; {
                    // Disable all options after selection
                    document.querySelectorAll('.quiz-option').forEach(el =&gt; {
                        el.style.pointerEvents = 'none';
                    });
                    
                    if (option === currentCard.meaning) {
                        optionEl.classList.add('correct');
                        stats.correct++;
                    } else {
                        optionEl.classList.add('incorrect');
                        stats.incorrect++;
                        
                        // Highlight the correct answer
                        document.querySelectorAll('.quiz-option').forEach(el =&gt; {
                            if (el.textContent === currentCard.meaning) {
                                el.classList.add('correct');
                            }
                        });
                    }
                    
                    stats.total++;
                    updateStats();
                });
                
                quizOptions.appendChild(optionEl);
            });
        }
        
        // Update stats display
        function updateStats() {
            correctCountEl.textContent = stats.correct;
            incorrectCountEl.textContent = stats.incorrect;
            totalCountEl.textContent = stats.total;
        }
        
        // Helper function to shuffle an array
        function shuffleArray(array) {
            const newArray = [...array];
            for (let i = newArray.length - 1; i &gt; 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
            }
            return newArray;
        }
        
        // Show toast notification
        function showToast(message) {
            toast.textContent = message;
            toast.classList.add('show');
            
            setTimeout(() =&gt; {
                toast.classList.remove('show');
            }, 3000);
        }
        
        // Get source code of the current page
        function getSourceCode() {
            return document.documentElement.outerHTML;
        }
        
        // Setup event listeners
        function setupEventListeners() {
            // Mode switching
            flashcardModeBtn.addEventListener('click', () =&gt; {
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            quizModeBtn.addEventListener('click', () =&gt; {
                flashcardContainer.classList.add('hidden');
                quizContainer.classList.remove('hidden');
                statsBar.classList.remove('hidden');
                quizModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                quizModeBtn.classList.replace('text-gray-700', 'text-white');
                flashcardModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                flashcardModeBtn.classList.replace('text-white', 'text-gray-700');
                setupQuiz();
            });
            
            // Next question button
            nextQuestionBtn.addEventListener('click', () =&gt; {
                currentQuizIndex++;
                showNextQuestion();
            });
            
            // Add card buttons
            addCardBtn.addEventListener('click', () =&gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateAddBtn.addEventListener('click', () =&gt; {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateImportBtn.addEventListener('click', () =&gt; {
                importFileInput.click();
            });
            
            quizEmptyStateAddBtn.addEventListener('click', () =&gt; {
                addCardModal.classList.remove('hidden');
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            cancelAddCardBtn.addEventListener('click', () =&gt; {
                addCardModal.classList.add('hidden');
                wordInput.value = '';
                meaningInput.value = '';
            });
            
            saveCardBtn.addEventListener('click', () =&gt; {
                const word = wordInput.value.trim();
                const meaning = meaningInput.value.trim();
                
                if (word &amp;&amp; meaning) {
                    flashcards.push({ word, meaning });
                    saveFlashcards();
                    renderFlashcards();
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                    showToast('Kart eklendi');
                }
            });
            
            // Clear cards functionality
            clearCardsBtn.addEventListener('click', () =&gt; {
                if (flashcards.length &gt; 0) {
                    confirmModal.classList.remove('hidden');
                }
            });
            
            cancelClearBtn.addEventListener('click', () =&gt; {
                confirmModal.classList.add('hidden');
            });
            
            confirmClearBtn.addEventListener('click', () =&gt; {
                flashcards = [];
                saveFlashcards();
                renderFlashcards();
                confirmModal.classList.add('hidden');
                showToast('Tüm kartlar silindi');
            });
            
            // Delete single card functionality
            cancelDeleteCardBtn.addEventListener('click', () =&gt; {
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            confirmDeleteCardBtn.addEventListener('click', () =&gt; {
                deleteCard(cardToDeleteIndex);
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            // Export/Import functionality
            exportCardsBtn.addEventListener('click', () =&gt; {
                exportFlashcards();
            });
            
            importCardsBtn.addEventListener('click', () =&gt; {
                importFileInput.click();
            });
            
            importFileInput.addEventListener('change', (e) =&gt; {
                if (e.target.files.length &gt; 0) {
                    importFlashcards(e.target.files[0]);
                    // Reset the input so the same file can be selected again
                    e.target.value = '';
                }
            });
            
            // JSON Editor functionality
            jsonEditorBtn.addEventListener('click', () =&gt; {
                showJsonEditor();
            });
            
            copyJsonBtn.addEventListener('click', () =&gt; {
                jsonTextarea.select();
                document.execCommand('copy');
                showToast('JSON kopyalandı');
            });
            
            applyJsonBtn.addEventListener('click', () =&gt; {
                applyJsonFromEditor();
            });
            
            cancelJsonEditor.addEventListener('click', () =&gt; {
                jsonEditorModal.classList.add('hidden');
            });
            
            // Source code functionality
            viewSourceBtn.addEventListener('click', () =&gt; {
                sourceCodeContent.textContent = getSourceCode();
                sourceCodeModal.classList.remove('hidden');
            });
            
            closeSourceCodeBtn.addEventListener('click', () =&gt; {
                sourceCodeModal.classList.add('hidden');
            });
            
            copySourceCodeBtn.addEventListener('click', () =&gt; {
                const sourceCode = getSourceCode();
                navigator.clipboard.writeText(sourceCode)
                    .then(() =&gt; {
                        showToast('Kod kopyalandı!');
                    })
                    .catch(err =&gt; {
                        showToast('Kod kopyalanamadı: ' + err);
                    });
            });
            
            // Handle Enter key in modal
            wordInput.addEventListener('keypress', (e) =&gt; {
                if (e.key === 'Enter') {
                    meaningInput.focus();
                }
            });
            
            meaningInput.addEventListener('keypress', (e) =&gt; {
                if (e.key === 'Enter') {
                    const word = wordInput.value.trim();
                    const meaning = meaningInput.value.trim();
                    
                    if (word &amp;&amp; meaning) {
                        flashcards.push({ word, meaning });
                        saveFlashcards();
                        renderFlashcards();
                        addCardModal.classList.add('hidden');
                        wordInput.value = '';
                        meaningInput.value = '';
                        showToast('Kart eklendi');
                    }
                }
            });
            
            // Close modals when clicking outside
            window.addEventListener('click', (e) =&gt; {
                if (e.target === addCardModal) {
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                }
                
                if (e.target === confirmModal) {
                    confirmModal.classList.add('hidden');
                }
                
                if (e.target === deleteCardModal) {
                    deleteCardModal.classList.add('hidden');
                    cardToDeleteIndex = -1;
                }
                
                if (e.target === jsonEditorModal) {
                    jsonEditorModal.classList.add('hidden');
                }
                
                if (e.target === sourceCodeModal) {
                    sourceCodeModal.classList.add('hidden');
                }
            });
        }
        
        // Initialize the app when the page loads
        document.addEventListener('DOMContentLoaded', init);
    &lt;/script&gt;
&lt;script&gt;(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'95024a574212513b',t:'MTc0OTk5Mjg0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&amp;&amp;(document.onreadystatechange=e,c())}}}})();&lt;/script&gt;&lt;iframe height="1" width="1" style="position: absolute; top: 0px; left: 0px; border: none; visibility: hidden;"&gt;&lt;/iframe&gt;

&lt;/body&gt;&lt;/html&gt;</div>
            </div>
        </div>
        
        <!-- Toast Notification -->
        <div id="toast" class="toast">Kart silindi</div>
    </div>

    <script>
        // Initialize empty flashcards array
        let flashcards = [];
        
        // Stats for quiz mode
        let stats = {
            correct: 0,
            incorrect: 0,
            total: 0
        };
        
        let currentQuizIndex = 0;
        let cardToDeleteIndex = -1;
        
        // DOM elements
        const flashcardContainer = document.getElementById('flashcardContainer');
        const quizContainer = document.getElementById('quizContainer');
        const quizContent = document.getElementById('quizContent');
        const quizEmptyState = document.getElementById('quizEmptyState');
        const emptyState = document.getElementById('emptyState');
        const flashcardModeBtn = document.getElementById('flashcardMode');
        const quizModeBtn = document.getElementById('quizMode');
        const addCardBtn = document.getElementById('addCardBtn');
        const clearCardsBtn = document.getElementById('clearCardsBtn');
        const exportCardsBtn = document.getElementById('exportCardsBtn');
        const importCardsBtn = document.getElementById('importCardsBtn');
        const jsonEditorBtn = document.getElementById('jsonEditorBtn');
        const importFileInput = document.getElementById('importFileInput');
        const viewSourceBtn = document.getElementById('viewSourceBtn');
        const addCardModal = document.getElementById('addCardModal');
        const confirmModal = document.getElementById('confirmModal');
        const deleteCardModal = document.getElementById('deleteCardModal');
        const jsonEditorModal = document.getElementById('jsonEditorModal');
        const sourceCodeModal = document.getElementById('sourceCodeModal');
        const cancelAddCardBtn = document.getElementById('cancelAddCard');
        const saveCardBtn = document.getElementById('saveCard');
        const wordInput = document.getElementById('wordInput');
        const meaningInput = document.getElementById('meaningInput');
        const emptyStateAddBtn = document.getElementById('emptyStateAddBtn');
        const emptyStateImportBtn = document.getElementById('emptyStateImportBtn');
        const quizEmptyStateAddBtn = document.getElementById('quizEmptyStateAddBtn');
        const statsBar = document.getElementById('statsBar');
        const correctCountEl = document.getElementById('correctCount');
        const incorrectCountEl = document.getElementById('incorrectCount');
        const totalCountEl = document.getElementById('totalCount');
        const nextQuestionBtn = document.getElementById('nextQuestion');
        const cancelClearBtn = document.getElementById('cancelClear');
        const confirmClearBtn = document.getElementById('confirmClear');
        const deleteCardWord = document.getElementById('deleteCardWord');
        const deleteCardMeaning = document.getElementById('deleteCardMeaning');
        const cancelDeleteCardBtn = document.getElementById('cancelDeleteCard');
        const confirmDeleteCardBtn = document.getElementById('confirmDeleteCard');
        const jsonTextarea = document.getElementById('jsonTextarea');
        const copyJsonBtn = document.getElementById('copyJsonBtn');
        const applyJsonBtn = document.getElementById('applyJsonBtn');
        const cancelJsonEditor = document.getElementById('cancelJsonEditor');
        const copySourceCodeBtn = document.getElementById('copySourceCode');
        const closeSourceCodeBtn = document.getElementById('closeSourceCode');
        const sourceCodeContent = document.getElementById('sourceCodeContent');
        const toast = document.getElementById('toast');
        
        // Initialize the app
        function init() {
            loadFlashcards();
            renderFlashcards();
            setupEventListeners();
        }
        
        // Load flashcards from localStorage
        function loadFlashcards() {
            const savedFlashcards = localStorage.getItem('englishFlashcards');
            if (savedFlashcards) {
                try {
                    flashcards = JSON.parse(savedFlashcards);
                } catch (e) {
                    console.error('Error parsing saved flashcards:', e);
                    flashcards = [];
                }
            }
        }
        
        // Save flashcards to localStorage
        function saveFlashcards() {
            localStorage.setItem('englishFlashcards', JSON.stringify(flashcards));
        }
        
        // Render all flashcards
        function renderFlashcards() {
            // Clear container except for empty state
            const cards = flashcardContainer.querySelectorAll('.flashcard');
            cards.forEach(card => card.remove());
            
            // Show or hide empty state
            if (flashcards.length === 0) {
                emptyState.classList.remove('hidden');
            } else {
                emptyState.classList.add('hidden');
                
                // Add flashcards
                flashcards.forEach((card, index) => {
                    const flashcardEl = document.createElement('div');
                    flashcardEl.className = 'flashcard';
                    flashcardEl.innerHTML = `
                        <div class="delete-btn" data-index="${index}">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16" />
                            </svg>
                        </div>
                        <div class="flashcard-inner">
                            <div class="flashcard-front">
                                <h2 class="text-2xl font-bold text-center">${card.word}</h2>
                            </div>
                            <div class="flashcard-back">
                                <p class="text-xl text-center">${card.meaning}</p>
                            </div>
                        </div>
                    `;
                    
                    // Add click event for flipping the card
                    const flashcardInner = flashcardEl.querySelector('.flashcard-inner');
                    flashcardInner.addEventListener('click', () => {
                        flashcardEl.classList.toggle('flipped');
                    });
                    
                    // Add click event for delete button
                    const deleteBtn = flashcardEl.querySelector('.delete-btn');
                    deleteBtn.addEventListener('click', (e) => {
                        e.stopPropagation(); // Prevent card flip
                        const index = parseInt(deleteBtn.getAttribute('data-index'));
                        showDeleteCardModal(index);
                    });
                    
                    flashcardContainer.appendChild(flashcardEl);
                });
            }
        }
        
        // Show delete card confirmation modal
        function showDeleteCardModal(index) {
            cardToDeleteIndex = index;
            const card = flashcards[index];
            deleteCardWord.textContent = card.word;
            deleteCardMeaning.textContent = card.meaning;
            deleteCardModal.classList.remove('hidden');
        }
        
        // Delete a single card
        function deleteCard(index) {
            if (index >= 0 && index < flashcards.length) {
                flashcards.splice(index, 1);
                saveFlashcards();
                renderFlashcards();
                showToast('Kart silindi');
            }
        }
        
        // Export flashcards to JSON file
        function exportFlashcards() {
            const dataStr = JSON.stringify(flashcards, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
            
            const exportFileDefaultName = 'ingilizce_kartlarim.json';
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showToast('Kartlar dışa aktarıldı');
        }
        
        // Import flashcards from JSON file
        function importFlashcards(file) {
            const reader = new FileReader();
            
            reader.onload = function(e) {
                try {
                    const importedCards = JSON.parse(e.target.result);
                    
                    if (Array.isArray(importedCards)) {
                        // Check if each card has the required properties
                        const validCards = importedCards.filter(card => 
                            card && typeof card === 'object' && 
                            'word' in card && 'meaning' in card &&
                            typeof card.word === 'string' && 
                            typeof card.meaning === 'string'
                        );
                        
                        if (validCards.length > 0) {
                            flashcards = validCards;
                            saveFlashcards();
                            renderFlashcards();
                            showToast(`${validCards.length} kart içe aktarıldı`);
                        } else {
                            showToast('Geçerli kart bulunamadı');
                        }
                    } else {
                        showToast('Geçersiz JSON formatı');
                    }
                } catch (error) {
                    console.error('Import error:', error);
                    showToast('Dosya okunamadı');
                }
            };
            
            reader.readAsText(file);
        }
        
        // Show JSON editor with current flashcards
        function showJsonEditor() {
            jsonTextarea.value = JSON.stringify(flashcards, null, 2);
            jsonEditorModal.classList.remove('hidden');
        }
        
        // Apply JSON from editor
        function applyJsonFromEditor() {
            try {
                const jsonData = JSON.parse(jsonTextarea.value);
                
                if (Array.isArray(jsonData)) {
                    // Check if each card has the required properties
                    const validCards = jsonData.filter(card => 
                        card && typeof card === 'object' && 
                        'word' in card && 'meaning' in card &&
                        typeof card.word === 'string' && 
                        typeof card.meaning === 'string'
                    );
                    
                    if (validCards.length > 0) {
                        flashcards = validCards;
                        saveFlashcards();
                        renderFlashcards();
                        jsonEditorModal.classList.add('hidden');
                        showToast(`${validCards.length} kart güncellendi`);
                    } else {
                        showToast('Geçerli kart bulunamadı');
                    }
                } else {
                    showToast('Geçersiz JSON formatı');
                }
            } catch (error) {
                console.error('JSON parse error:', error);
                showToast('Geçersiz JSON formatı');
            }
        }
        
        // Setup quiz mode
        function setupQuiz() {
            currentQuizIndex = 0;
            stats.correct = 0;
            stats.incorrect = 0;
            stats.total = 0;
            updateStats();
            
            // Check if we have enough cards for quiz mode
            if (flashcards.length < 4) {
                quizContent.classList.add('hidden');
                quizEmptyState.classList.remove('hidden');
            } else {
                quizContent.classList.remove('hidden');
                quizEmptyState.classList.add('hidden');
                showNextQuestion();
            }
        }
        
        // Show next question in quiz mode
        function showNextQuestion() {
            if (currentQuizIndex >= flashcards.length) {
                // Reset if we've gone through all cards
                currentQuizIndex = 0;
            }
            
            const currentCard = flashcards[currentQuizIndex];
            const quizQuestion = document.getElementById('quizQuestion');
            const quizOptions = document.getElementById('quizOptions');
            
            quizQuestion.textContent = currentCard.word;
            
            // Create options (including the correct one and some random ones)
            let options = [currentCard.meaning];
            
            // Add some random options from other cards
            let availableCards = [...flashcards];
            availableCards.splice(currentQuizIndex, 1); // Remove current card
            
            // Shuffle available cards
            availableCards = shuffleArray(availableCards);
            
            // Add up to 3 more options
            for (let i = 0; i < 3 && i < availableCards.length; i++) {
                options.push(availableCards[i].meaning);
            }
            
            // Shuffle options
            options = shuffleArray(options);
            
            // Render options
            quizOptions.innerHTML = '';
            options.forEach(option => {
                const optionEl = document.createElement('div');
                optionEl.className = 'quiz-option bg-gray-100 p-4 rounded-lg cursor-pointer hover:bg-gray-200';
                optionEl.textContent = option;
                
                optionEl.addEventListener('click', () => {
                    // Disable all options after selection
                    document.querySelectorAll('.quiz-option').forEach(el => {
                        el.style.pointerEvents = 'none';
                    });
                    
                    if (option === currentCard.meaning) {
                        optionEl.classList.add('correct');
                        stats.correct++;
                    } else {
                        optionEl.classList.add('incorrect');
                        stats.incorrect++;
                        
                        // Highlight the correct answer
                        document.querySelectorAll('.quiz-option').forEach(el => {
                            if (el.textContent === currentCard.meaning) {
                                el.classList.add('correct');
                            }
                        });
                    }
                    
                    stats.total++;
                    updateStats();
                });
                
                quizOptions.appendChild(optionEl);
            });
        }
        
        // Update stats display
        function updateStats() {
            correctCountEl.textContent = stats.correct;
            incorrectCountEl.textContent = stats.incorrect;
            totalCountEl.textContent = stats.total;
        }
        
        // Helper function to shuffle an array
        function shuffleArray(array) {
            const newArray = [...array];
            for (let i = newArray.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
            }
            return newArray;
        }
        
        // Show toast notification
        function showToast(message) {
            toast.textContent = message;
            toast.classList.add('show');
            
            setTimeout(() => {
                toast.classList.remove('show');
            }, 3000);
        }
        
        // Get source code of the current page
        function getSourceCode() {
            return document.documentElement.outerHTML;
        }
        
        // Setup event listeners
        function setupEventListeners() {
            // Mode switching
            flashcardModeBtn.addEventListener('click', () => {
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            quizModeBtn.addEventListener('click', () => {
                flashcardContainer.classList.add('hidden');
                quizContainer.classList.remove('hidden');
                statsBar.classList.remove('hidden');
                quizModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                quizModeBtn.classList.replace('text-gray-700', 'text-white');
                flashcardModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                flashcardModeBtn.classList.replace('text-white', 'text-gray-700');
                setupQuiz();
            });
            
            // Next question button
            nextQuestionBtn.addEventListener('click', () => {
                currentQuizIndex++;
                showNextQuestion();
            });
            
            // Add card buttons
            addCardBtn.addEventListener('click', () => {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateAddBtn.addEventListener('click', () => {
                addCardModal.classList.remove('hidden');
            });
            
            emptyStateImportBtn.addEventListener('click', () => {
                importFileInput.click();
            });
            
            quizEmptyStateAddBtn.addEventListener('click', () => {
                addCardModal.classList.remove('hidden');
                flashcardContainer.classList.remove('hidden');
                quizContainer.classList.add('hidden');
                statsBar.classList.add('hidden');
                flashcardModeBtn.classList.replace('bg-gray-200', 'bg-indigo-600');
                flashcardModeBtn.classList.replace('text-gray-700', 'text-white');
                quizModeBtn.classList.replace('bg-indigo-600', 'bg-gray-200');
                quizModeBtn.classList.replace('text-white', 'text-gray-700');
            });
            
            cancelAddCardBtn.addEventListener('click', () => {
                addCardModal.classList.add('hidden');
                wordInput.value = '';
                meaningInput.value = '';
            });
            
            saveCardBtn.addEventListener('click', () => {
                const word = wordInput.value.trim();
                const meaning = meaningInput.value.trim();
                
                if (word && meaning) {
                    flashcards.push({ word, meaning });
                    saveFlashcards();
                    renderFlashcards();
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                    showToast('Kart eklendi');
                }
            });
            
            // Clear cards functionality
            clearCardsBtn.addEventListener('click', () => {
                if (flashcards.length > 0) {
                    confirmModal.classList.remove('hidden');
                }
            });
            
            cancelClearBtn.addEventListener('click', () => {
                confirmModal.classList.add('hidden');
            });
            
            confirmClearBtn.addEventListener('click', () => {
                flashcards = [];
                saveFlashcards();
                renderFlashcards();
                confirmModal.classList.add('hidden');
                showToast('Tüm kartlar silindi');
            });
            
            // Delete single card functionality
            cancelDeleteCardBtn.addEventListener('click', () => {
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            confirmDeleteCardBtn.addEventListener('click', () => {
                deleteCard(cardToDeleteIndex);
                deleteCardModal.classList.add('hidden');
                cardToDeleteIndex = -1;
            });
            
            // Export/Import functionality
            exportCardsBtn.addEventListener('click', () => {
                exportFlashcards();
            });
            
            importCardsBtn.addEventListener('click', () => {
                importFileInput.click();
            });
            
            importFileInput.addEventListener('change', (e) => {
                if (e.target.files.length > 0) {
                    importFlashcards(e.target.files[0]);
                    // Reset the input so the same file can be selected again
                    e.target.value = '';
                }
            });
            
            // JSON Editor functionality
            jsonEditorBtn.addEventListener('click', () => {
                showJsonEditor();
            });
            
            copyJsonBtn.addEventListener('click', () => {
                jsonTextarea.select();
                document.execCommand('copy');
                showToast('JSON kopyalandı');
            });
            
            applyJsonBtn.addEventListener('click', () => {
                applyJsonFromEditor();
            });
            
            cancelJsonEditor.addEventListener('click', () => {
                jsonEditorModal.classList.add('hidden');
            });
            
            // Source code functionality
            viewSourceBtn.addEventListener('click', () => {
                sourceCodeContent.textContent = getSourceCode();
                sourceCodeModal.classList.remove('hidden');
            });
            
            closeSourceCodeBtn.addEventListener('click', () => {
                sourceCodeModal.classList.add('hidden');
            });
            
            copySourceCodeBtn.addEventListener('click', () => {
                const sourceCode = getSourceCode();
                navigator.clipboard.writeText(sourceCode)
                    .then(() => {
                        showToast('Kod kopyalandı!');
                    })
                    .catch(err => {
                        showToast('Kod kopyalanamadı: ' + err);
                    });
            });
            
            // Handle Enter key in modal
            wordInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') {
                    meaningInput.focus();
                }
            });
            
            meaningInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') {
                    const word = wordInput.value.trim();
                    const meaning = meaningInput.value.trim();
                    
                    if (word && meaning) {
                        flashcards.push({ word, meaning });
                        saveFlashcards();
                        renderFlashcards();
                        addCardModal.classList.add('hidden');
                        wordInput.value = '';
                        meaningInput.value = '';
                        showToast('Kart eklendi');
                    }
                }
            });
            
            // Close modals when clicking outside
            window.addEventListener('click', (e) => {
                if (e.target === addCardModal) {
                    addCardModal.classList.add('hidden');
                    wordInput.value = '';
                    meaningInput.value = '';
                }
                
                if (e.target === confirmModal) {
                    confirmModal.classList.add('hidden');
                }
                
                if (e.target === deleteCardModal) {
                    deleteCardModal.classList.add('hidden');
                    cardToDeleteIndex = -1;
                }
                
                if (e.target === jsonEditorModal) {
                    jsonEditorModal.classList.add('hidden');
                }
                
                if (e.target === sourceCodeModal) {
                    sourceCodeModal.classList.add('hidden');
                }
            });
        }
        
        // Initialize the app when the page loads
        document.addEventListener('DOMContentLoaded', init);
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'95024a574212513b',t:'MTc0OTk5Mjg0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script><iframe height="1" width="1" style="position: absolute; top: 0px; left: 0px; border: none; visibility: hidden;"></iframe>

</body></html>
