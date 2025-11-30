<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>别墅设计装修图 - 专业别墅设计案例展示平台</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Three.js -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <!-- GSAP 动画库 -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/gsap.min.js"></script>
    <!-- ScrollTrigger 插件 -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.11.4/ScrollTrigger.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap');
        
        :root {
            --primary-color: #1a365d;
            --secondary-color: #2d3748;
            --accent-color: #c9a87a;
            --light-color: #f7fafc;
            --dark-color: #1a202c;
        }
        
        body {
            font-family: 'Noto Sans SC', sans-serif;
            color: var(--secondary-color);
            background-color: #f8f9fa;
            overflow-x: hidden;
        }
        
        .hero-section {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.7)), url('https://p11-doubao-search-sign.byteimg.com/tos-cn-i-qvj2lq49k0/b27d904250634fedb376f9a649c92962~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=9rGG9otHPcsUoqizaNEQlpESuDo%3D') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            position: relative;
        }
        
        .hero-content {
            text-align: center;
            z-index: 2;
            max-width: 800px;
        }
        
        .hero-title {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero-subtitle {
            font-size: 1.5rem;
            font-weight: 300;
            margin-bottom: 2rem;
        }
        
        .btn-primary {
            background-color: var(--accent-color);
            color: var(--dark-color);
            padding: 0.75rem 2rem;
            border-radius: 0.25rem;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .btn-primary:hover {
            background-color: #b89666;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
            color: var(--primary-color);
            position: relative;
            padding-bottom: 1rem;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--accent-color);
        }
        
        .case-card {
            border-radius: 0.5rem;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            background-color: white;
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .case-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }
        
        .case-image {
            width: 100%;
            height: 250px;
            object-fit: cover;
            transition: all 0.5s ease;
        }
        
        .case-card:hover .case-image {
            transform: scale(1.05);
        }
        
        .case-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .case-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--primary-color);
        }
        
        .case-description {
            color: var(--secondary-color);
            margin-bottom: 1rem;
            flex-grow: 1;
        }
        
        .case-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1rem;
        }
        
        .case-style {
            background-color: var(--accent-color);
            color: white;
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            font-size: 0.875rem;
        }
        
        .case-area {
            color: var(--secondary-color);
            font-size: 0.875rem;
        }
        
        .filter-section {
            background-color: white;
            padding: 2rem;
            border-radius: 0.5rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            margin-bottom: 2rem;
        }
        
        .filter-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            color: var(--primary-color);
        }
        
        .filter-group {
            margin-bottom: 1.5rem;
        }
        
        .filter-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--secondary-color);
        }
        
        .filter-select {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #e2e8f0;
            border-radius: 0.25rem;
            background-color: white;
            color: var(--secondary-color);
        }
        
        .filter-options {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        
        .filter-option {
            padding: 0.5rem 1rem;
            border: 1px solid #e2e8f0;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.875rem;
        }
        
        .filter-option:hover {
            background-color: var(--accent-color);
            color: white;
            border-color: var(--accent-color);
        }
        
        .filter-option.active {
            background-color: var(--accent-color);
            color: white;
            border-color: var(--accent-color);
        }
        
        .view-3d-btn {
            background-color: var(--primary-color);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 0.25rem;
            font-weight: 500;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .view-3d-btn:hover {
            background-color: #0f2a4a;
            transform: translateY(-2px);
        }
        
        .designer-card {
            border-radius: 0.5rem;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            background-color: white;
            text-align: center;
            padding: 2rem;
        }
        
        .designer-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }
        
        .designer-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 1rem;
            border: 4px solid var(--accent-color);
        }
        
        .designer-name {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.25rem;
            color: var(--primary-color);
        }
        
        .designer-company {
            color: var(--secondary-color);
            margin-bottom: 1rem;
            font-size: 0.875rem;
        }
        
        .designer-description {
            color: var(--secondary-color);
            margin-bottom: 1.5rem;
        }
        
        .contact-btn {
            background-color: var(--accent-color);
            color: var(--dark-color);
            padding: 0.5rem 1.5rem;
            border-radius: 0.25rem;
            font-weight: 500;
            transition: all 0.3s ease;
            display: inline-block;
        }
        
        .contact-btn:hover {
            background-color: #b89666;
            transform: translateY(-2px);
        }
        
        .ai-section {
            background: linear-gradient(135deg, #1a365d 0%, #2d3748 100%);
            color: white;
            padding: 4rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .ai-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect x="0" y="0" width="100" height="100" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="2"/></svg>') repeat;
            opacity: 0.2;
        }
        
        .ai-content {
            position: relative;
            z-index: 1;
        }
        
        .ai-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: white;
        }
        
        .ai-subtitle {
            font-size: 1.25rem;
            font-weight: 300;
            margin-bottom: 2rem;
            color: rgba(255, 255, 255, 0.8);
        }
        
        .ai-image {
            border-radius: 0.5rem;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            max-width: 100%;
        }
        
        .upload-btn {
            background-color: var(--accent-color);
            color: var(--dark-color);
            padding: 0.75rem 2rem;
            border-radius: 0.25rem;
            font-weight: 600;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            margin-top: 1rem;
        }
        
        .upload-btn:hover {
            background-color: #b89666;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .footer {
            background-color: var(--dark-color);
            color: white;
            padding: 3rem 0;
        }
        
        .footer-title {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            color: white;
        }
        
        .footer-links {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .footer-links li {
            margin-bottom: 0.75rem;
        }
        
        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            transition: all 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--accent-color);
            padding-left: 5px;
        }
        
        .social-icons {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .social-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            transition: all 0.3s ease;
        }
        
        .social-icon:hover {
            background-color: var(--accent-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.875rem;
        }
        
        /* 3D Viewer Styles */
        #viewer-container {
            width: 100%;
            height: 500px;
            background-color: #f0f0f0;
            border-radius: 0.5rem;
            overflow: hidden;
            position: relative;
        }
        
        .viewer-controls {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
            z-index: 10;
        }
        
        .viewer-control-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.8);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .viewer-control-btn:hover {
            background-color: white;
            transform: scale(1.1);
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.25rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .ai-title {
                font-size: 2rem;
            }
            
            .ai-subtitle {
                font-size: 1rem;
            }
            
            .case-grid {
                grid-template-columns: 1fr;
            }
            
            .designer-grid {
                grid-template-columns: 1fr;
            }
        }
        
        /* Animation Classes */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        
        .fade-in.active {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--accent-color);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: #b89666;
        }
        
        /* Loader */
        .loader {
            width: 100%;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: fixed;
            background: white;
            z-index: 999;
            transition: opacity 0.5s ease, visibility 0.5s ease;
        }
        
        .loader.hidden {
            opacity: 0;
            visibility: hidden;
        }
        
        .loader-circle {
            width: 50px;
            height: 50px;
            border: 5px solid #f3f3f3;
            border-top: 5px solid var(--accent-color);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Mobile Menu */
        .mobile-menu {
            position: fixed;
            top: 0;
            right: -100%;
            width: 80%;
            height: 100vh;
            background-color: white;
            z-index: 1000;
            padding: 2rem;
            transition: right 0.3s ease;
            box-shadow: -10px 0 30px rgba(0, 0, 0, 0.1);
        }
        
        .mobile-menu.active {
            right: 0;
        }
        
        .mobile-menu-close {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 999;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        
        .overlay.active {
            opacity: 1;
            visibility: visible;
        }
    </style>
</head>
<body>
    <!-- Loader -->
    <div class="loader">
        <div class="loader-circle"></div>
    </div>

    <!-- Header -->
    <header class="fixed top-0 left-0 w-full bg-white bg-opacity-95 shadow-md z-50 transition-all duration-300" id="header">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="flex items-center">
                <span class="text-2xl font-bold text-primary-color">西班牙银河建工<span class="text-accent-color">工程公司</span></span>
            </a>
            
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#home" class="text-secondary-color hover:text-accent-color transition-colors">首页</a>
                <a href="#cases" class="text-secondary-color hover:text-accent-color transition-colors">案例展示</a>
                <a href="#3d-view" class="text-secondary-color hover:text-accent-color transition-colors">3D预览</a>
                <a href="#designers" class="text-secondary-color hover:text-accent-color transition-colors">设计师</a>
                <a href="#ai-style" class="text-secondary-color hover:text-accent-color transition-colors">AI风格匹配</a>
                <a href="#contact" class="btn-primary">联系我们</a>
            </nav>
            
            <button class="md:hidden text-secondary-color text-2xl" id="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>
    
    <!-- Mobile Menu -->
    <div class="mobile-menu">
        <div class="mobile-menu-close">
            <i class="fas fa-times"></i>
        </div>
        <nav class="flex flex-col space-y-4 mt-8">
            <a href="#home" class="text-secondary-color hover:text-accent-color transition-colors text-lg">首页</a>
            <a href="#cases" class="text-secondary-color hover:text-accent-color transition-colors text-lg">案例展示</a>
            <a href="#3d-view" class="text-secondary-color hover:text-accent-color transition-colors text-lg">3D预览</a>
            <a href="#designers" class="text-secondary-color hover:text-accent-color transition-colors text-lg">设计师</a>
            <a href="#ai-style" class="text-secondary-color hover:text-accent-color transition-colors text-lg">AI风格匹配</a>
            <a href="#contact" class="btn-primary mt-4 text-center">联系我们</a>
        </nav>
    </div>
    <div class="overlay"></div>

    <!-- Hero Section -->
    <section id="home" class="hero-section">
        <div class="hero-content">
            <h1 class="hero-title">探索顶级别墅设计灵感</h1>
            <p class="hero-subtitle">专业别墅设计案例展示平台，为您提供全方位的设计参考与服务</p>
            <a href="#cases" class="btn-primary">浏览案例</a>
        </div>
    </section>

    <!-- Case Showcase Section -->
    <section id="cases" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="section-title">精选别墅设计案例</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 case-grid">
                <!-- Case 1 -->
                <div class="case-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://p26-doubao-search-sign.byteimg.com/labis/f3ff479d861eec9a1e919bc0a0dcc419~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=j4ul00bfvL3vBZ4dRhLoKuF%2FLug%3D" alt="现代风格别墅" class="case-image">
                    </div>
                    <div class="case-content">
                        <h3 class="case-title">现代极简风格别墅</h3>
                        <p class="case-description">以简洁的线条和现代材质打造的极简风格别墅，强调空间感和自然光线的运用，创造出舒适而不失格调的居住环境。</p>
                        <div class="case-meta">
                            <span class="case-style">现代风格</span>
                            <span class="case-area">320㎡</span>
                        </div>
                        <a href="#" class="view-3d-btn mt-4">
                           
                        </a>
                    </div>
                </div>
                
                <!-- Case 2 -->
                <div class="case-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://p26-doubao-search-sign.byteimg.com/labis/e56eeef6844110959e77b07ad3368598~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=qzLEzaJWDhK63yqVsaUvon%2BDtBo%3D" alt="新中式风格别墅" class="case-image">
                    </div>
                    <div class="case-content">
                        <h3 class="case-title">新中式风格别墅</h3>
                        <p class="case-description">融合传统中式元素与现代设计语言，打造出既有文化底蕴又不失现代感的居住空间，展现东方美学的独特魅力。</p>
                        <div class="case-meta">
                            <span class="case-style">新中式</span>
                            <span class="case-area">450㎡</span>
                        </div>
                        <a href="#" class="view-3d-btn mt-4">
                         
                        </a>
                    </div>
                </div>
                
                <!-- Case 3 -->
                <div class="case-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://p26-doubao-search-sign.byteimg.com/labis/af85d3b22aa205c4f7e23b6db014c237~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=yWZOAX0l%2BcDJa0m6qKIPl0r%2Fku4%3D" alt="欧式风格别墅" class="case-image">
                    </div>
                    <div class="case-content">
                        <h3 class="case-title">欧式古典风格别墅</h3>
                        <p class="case-description">重现欧洲宫廷的奢华气派，强调对称、秩序与装饰性，展现尊贵典雅的生活态度，细节处彰显精湛工艺。</p>
                        <div class="case-meta">
                            <span class="case-style">欧式古典</span>
                            <span class="case-area">520㎡</span>
                        </div>
                        <a href="#" class="view-3d-btn mt-4">
                         
                        </a>
                    </div>
                </div>
                
                <!-- Case 4 -->
                <div class="case-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://p26-doubao-search-sign.byteimg.com/labis/56b8c55bc72be37e9bf5da65467a456c~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=qMkNpKeYq1Ry%2BZFVEwNtKNSzLus%3D" alt="现代风格别墅" class="case-image">
                    </div>
                    <div class="case-content">
                        <h3 class="case-title">现代山地别墅</h3>
                        <p class="case-description">依山而建的现代风格别墅，充分利用地形优势，将自然景观与建筑融为一体，创造出独特的居住体验。</p>
                        <div class="case-meta">
                            <span class="case-style">现代风格</span>
                            <span class="case-area">380㎡</span>
                        </div>
                        <a href="#" class="view-3d-btn mt-4">
                          
                        </a>
                    </div>
                </div>
                
                <!-- Case 5 -->
                <div class="case-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://p11-doubao-search-sign.byteimg.com/tos-cn-i-qvj2lq49k0/bed80b08195a4f9b8f05cadb68183487~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=yv1lxQH9k25bEaDImGaRL9hPVCY%3D" alt="新中式风格别墅" class="case-image">
                    </div>
                    <div class="case-content">
                        <h3 class="case-title">新中式三层别墅</h3>
                        <p class="case-description">传统中式元素与现代设计的完美融合，三层空间布局合理，功能齐全，展现东方美学的现代演绎。</p>
                        <div class="case-meta">
                            <span class="case-style">新中式</span>
                            <span class="case-area">480㎡</span>
                        </div>
                        <a href="#" class="view-3d-btn mt-4">
                          
                        </a>
                    </div>
                </div>
                
                <!-- Case 6 -->
                <div class="case-card fade-in">
                    <div class="overflow-hidden">
                        <img src="https://p26-doubao-search-sign.byteimg.com/labis/a17ceddbda644aa6300dac0502cd90f5~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=AuotNOjzzcGEaESDTH%2FQLN3mufY%3D" alt="现代简约风格别墅" class="case-image">
                    </div>
                    <div class="case-content">
                        <h3 class="case-title">现代简约风格别墅</h3>
                        <p class="case-description">以"少即是多"为设计理念，强调功能性与空间感，通过简洁的线条和材质对比，创造出简约而不简单的居住空间。</p>
                        <div class="case-meta">
                            <span class="case-style">现代简约</span>
                            <span class="case-area">280㎡</span>
                        </div>
                        <a href="#" class="view-3d-btn mt-4">
                           
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="btn-primary">查看更多案例</a>
            </div>
        </div>
    </section>

    <!-- Filter Section -->
    <section class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 lg:grid-cols-4 gap-8">
                <div class="lg:col-span-1">
                    <div class="filter-section sticky top-24">
                        <h3 class="filter-title">筛选条件</h3>
                        
                        <div class="filter-group">
                            <label class="filter-label">风格</label>
                            <select class="filter-select" id="style-filter">
                                <option value="all">全部风格</option>
                                <option value="modern">现代风格</option>
                                <option value="chinese">新中式</option>
                                <option value="european">欧式古典</option>
                                <option value="mediterranean">地中海</option>
                                <option value="industrial">工业风格</option>
                            </select>
                        </div>
                        
                        <div class="filter-group">
                            <label class="filter-label">面积</label>
                            <select class="filter-select" id="area-filter">
                                <option value="all">全部面积</option>
                                <option value="small">200㎡以下</option>
                                <option value="medium">200-400㎡</option>
                                <option value="large">400㎡以上</option>
                            </select>
                        </div>
                        
                        <div class="filter-group">
                            <label class="filter-label">户型</label>
                            <select class="filter-select" id="type-filter">
                                <option value="all">全部户型</option>
                                <option value="single">独栋别墅</option>
                                <option value="semi">联排别墅</option>
                                <option value="townhouse">叠拼别墅</option>
                            </select>
                        </div>
                        
                        <div class="filter-group">
                            <label class="filter-label">特色标签</label>
                            <div class="filter-options">
                                <span class="filter-option" data-tag="garden">花园</span>
                                <span class="filter-option" data-tag="pool">泳池</span>
                                <span class="filter-option" data-tag="basement">地下室</span>
                                <span class="filter-option" data-tag="attic">阁楼</span>
                                <span class="filter-option" data-tag="smart">智能家居</span>
                            </div>
                        </div>
                        
                        <button class="btn-primary w-full mt-4" id="apply-filters">应用筛选</button>
                    </div>
                </div>
                
                <div class="lg:col-span-3">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <!-- Filtered Case 1 -->
                        <div class="case-card fade-in">
                            <div class="overflow-hidden">
                                <img src="https://p26-doubao-search-sign.byteimg.com/tos-cn-i-be4g95zd3a/1535111737943523340~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=dk0LCjmyYuEITloOVm3l4fJ4NnU%3D" alt="现代风格别墅" class="case-image">
                            </div>
                            <div class="case-content">
                                <h3 class="case-title">现代风格别墅</h3>
                                <p class="case-description">现代风格别墅，强调空间的开放性和流动性，采用大面积落地窗，将室外景色引入室内。</p>
                                <div class="case-meta">
                                    <span class="case-style">现代风格</span>
                                    <span class="case-area">350㎡</span>
                                </div>
                                <a href="#" class="view-3d-btn mt-4">
                                
                                </a>
                            </div>
                        </div>
                        
                        <!-- Filtered Case 2 -->
                        <div class="case-card fade-in">
                            <div class="overflow-hidden">
                                <img src="https://p26-doubao-search-sign.byteimg.com/tos-cn-i-be4g95zd3a/1708639772525330436~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=Qa8sFzFb8jrPdJRdSB8RDmpPnlY%3D" alt="北欧风格别墅" class="case-image">
                            </div>
                            <div class="case-content">
                                <h3 class="case-title">北欧风格别墅</h3>
                                <p class="case-description">北欧风格别墅，以简洁、实用为设计理念，采用天然材质和中性色调，营造温馨舒适的居住氛围。</p>
                                <div class="case-meta">
                                    <span class="case-style">北欧风格</span>
                                    <span class="case-area">280㎡</span>
                                </div>
                                <a href="#" class="view-3d-btn mt-4">
                                    
                                </a>
                            </div>
                        </div>
                        
                        <!-- Filtered Case 3 -->
                        <div class="case-card fade-in">
                            <div class="overflow-hidden">
                                <img src="https://p26-doubao-search-sign.byteimg.com/tos-cn-i-be4g95zd3a/916218770284347432~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=2bMS2OLTpoYKINUI9Jlq9ROyDUo%3D" alt="联排别墅" class="case-image">
                            </div>
                            <div class="case-content">
                                <h3 class="case-title">现代联排别墅</h3>
                                <p class="case-description">现代风格联排别墅，空间布局紧凑合理，外观设计现代简约，适合城市生活的高品质选择。</p>
                                <div class="case-meta">
                                    <span class="case-style">现代风格</span>
                                    <span class="case-area">220㎡</span>
                                </div>
                                <a href="#" class="view-3d-btn mt-4">
                                  
                                </a>
                            </div>
                        </div>
                        
                        <!-- Filtered Case 4 -->
                        <div class="case-card fade-in">
                            <div class="overflow-hidden">
                                <img src="https://p26-doubao-search-sign.byteimg.com/tos-cn-i-be4g95zd3a/913581583055585348~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&x-expires=1780038822&x-signature=xXfe5BDZ89SFeYDeHsnj0q3rBr0%3D" alt="现代联排别墅" class="case-image">
                            </div>
                            <div class="case-content">
                                <h3 class="case-title">现代简约联排别墅</h3>
                                <p class="case-description">现代简约风格联排别墅，以简洁的线条和几何形状为主要设计元素，打造时尚现代的居住空间。</p>
                                <div class="case-meta">
                                    <span class="case-style">现代简约</span>
                                    <span class="case-area">240㎡</span>
                                </div>
                                <a href="#" class="view-3d-btn mt-4">
                                
                                </a>
                            </div>
                        </div>
                    </div>
                    
                    <div class="flex justify-center mt-8">
                        <nav class="inline-flex rounded-md shadow">
                            <a href="#" class="py-2 px-4 bg-white border border-gray-300 rounded-l-md hover:bg-gray-50">上一页</a>
                            <a href="#" class="py-2 px-4 bg-accent-color text-white border border-accent-color">1</a>
                            <a href="#" class="py-2 px-4 bg-white border border-gray-300 hover:bg-gray-50">2</a>
                            <a href="#" class="py-2 px-4 bg-white border border-gray-300 hover:bg-gray-50">3</a>
                            <a href="#" class="py-2 px-4 bg-white border border-gray-300 rounded-r-md hover:bg-gray-50">下一页</a>
                        </nav>
                    </div>
                </div>
            </div>
        </div>
    </section>

                      
                    <div class="mt-4 flex flex-wrap gap-2">
                        <button class="px-4 py-2 bg-gray-200 rounded-md hover:bg-gray-300 transition-colors" data-view="exterior">外观</button>
                        <button class="px-4 py-2 bg-gray-200 rounded-md hover:bg-gray-300 transition-colors" data-view="living-room">客厅</button>
                        <button class="px-4 py-2 bg-gray-200 rounded-md hover:bg-gray-300 transition-colors" data-view="kitchen">厨房</button>
                        <button class="px-4 py-2 bg-gray-200 rounded-md hover:bg-gray-300 transition-colors" data-view="bedroom">卧室</button>
                        <button class="px-4 py-2 bg-gray-200 rounded-md hover:bg-gray-300 transition-colors" data-view="bathroom">浴室</button>
                    </div>
                </div>
                
                <div class="fade-in">
                    <h3 class="text-2xl font-bold mb-4 text-primary-color">现代风格别墅</h3>
                    <p class="mb-4 text-gray-700">
                        这座现代风格别墅采用了简约而不失格调的设计理念，通过大面积的落地窗将自然光线引入室内，创造出明亮通透的空间感。外观采用几何线条和材质对比，展现现代建筑的美学魅力。
                    </p>
                    <p class="mb-4 text-gray-700">
                        室内设计以功能性为核心，空间布局合理，动线流畅。客厅挑高设计增强了空间的层次感和视觉冲击力，开放式厨房与餐厅相连，提升了空间的互动性和社交功能。
                    </p>
                    
                    <div class="grid grid-cols-2 gap-4 mb-6">
                        <div class="bg-gray-50 p-4 rounded-md">
                            <h4 class="font-semibold text-primary-color">建筑信息</h4>
                            <ul class="mt-2 space-y-1 text-sm text-gray-600">
                                <li><i class="fas fa-ruler-combined mr-2 text-accent-color"></i> 占地面积: 450㎡</li>
                                <li><i class="fas fa-home mr-2 text-accent-color"></i> 建筑面积: 320㎡</li>
                                <li><i class="fas fa-layer-group mr-2 text-accent-color"></i> 层数: 3层</li>
                                <li><i class="fas fa-bed mr-2 text-accent-color"></i> 卧室: 4间</li>
                                <li><i class="fas fa-bath mr-2 text-accent-color"></i> 浴室: 3间</li>
                            </ul>
                        </div>
                        <div class="bg-gray-50 p-4 rounded-md">
                            <h4 class="font-semibold text-primary-color">设计特点</h4>
                            <ul class="mt-2 space-y-1 text-sm text-gray-600">
                                <li><i class="fas fa-check mr-2 text-accent-color"></i> 开放式空间布局</li>
                                <li><i class="fas fa-check mr-2 text-accent-color"></i> 大面积落地窗</li>
                                <li><i class="fas fa-check mr-2 text-accent-color"></i> 智能家居系统</li>
                                <li><i class="fas fa-check mr-2 text-accent-color"></i> 屋顶花园</li>
                                <li><i class="fas fa-check mr-2 text-accent-color"></i> 地下车库</li>
                            </ul>
                        </div>
                    </div>
                    
                    <div class="flex flex-wrap gap-4">
                        <a href="#" class="btn-primary">
                            <i class="fas fa-file-pdf mr-2"></i> 下载平面图
                        </a>
                        <a href="#" class="bg-white border border-primary-color text-primary-color px-6 py-3 rounded-md font-semibold hover:bg-primary-color hover:text-white transition-colors">
                            <i class="fas fa-envelope mr-2"></i> 咨询详情
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

      <!-- AI Style Matching Section -->
    <section id="ai-style" class="ai-section">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center ai-content">
                <div class="fade-in">
                    <h2 class="ai-title">AI风格智能匹配系统</h2>
                    <p class="ai-subtitle">上传您的户型图或偏好，我们的AI系统将为您推荐最适合的别墅设计风格，让您的梦想家园更加完美。</p>
                    
                    <div class="bg-white bg-opacity-10 p-6 rounded-lg backdrop-blur-sm mt-8">
                        <h3 class="text-xl font-semibold mb-4 text-white">如何使用</h3>
                        <ol class="list-decimal list-inside space-y-2 text-white text-opacity-90">
                            <li>上传您的户型图或选择您喜欢的风格偏好</li>
                            <li>AI系统将分析您的需求和空间特点</li>
                            <li>获取量身定制的风格推荐和设计方案</li>
                            <li>与专业设计师一对一沟通，完善细节</li>
                        </ol>
                        
                        <button class="upload-btn mt-6">
                            <i class="fas fa-upload mr-2"></i> 上传户型图
                        </button>
                    </div>
                </div>
                
                <div class="fade-in">
                    <img src="https://p3-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/rc/pc/super_tool/d6227de1f92e4c79bddd5ef91ed0f265~tplv-a9rns2rl98-image.image?rcl=202511301513222678C08197F139C65E03&rk3s=8e244e95&rrcfp=f06b921b&x-expires=1767078855&x-signature=pqPY4mWr%2BZJcSWaH%2FS78FkWOnac%3D" alt="AI风格匹配系统" class="ai-image">
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="section-title">联系我们</h2>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div class="fade-in">
                    <form class="space-y-6">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="name" class="block mb-2 text-sm font-medium text-gray-700">姓名</label>
                                <input type="text" id="name" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-accent-color focus:border-accent-color block w-full p-2.5" placeholder="您的姓名" required>
                            </div>
                            <div>
                                <label for="phone" class="block mb-2 text-sm font-medium text-gray-700">电话</label>
                                <input type="tel" id="phone" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-accent-color focus:border-accent-color block w-full p-2.5" placeholder="您的联系电话" required>
                            </div>
                        </div>
                        
                        <div>
                            <label for="email" class="block mb-2 text-sm font-medium text-gray-700">邮箱</label>
                            <input type="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-accent-color focus:border-accent-color block w-full p-2.5" placeholder="您的邮箱地址" required>
                        </div>
                        
                        <div>
                            <label for="message" class="block mb-2 text-sm font-medium text-gray-700">留言</label>
                            <textarea id="message" rows="4" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-accent-color focus:border-accent-color block w-full p-2.5" placeholder="请描述您的需求..."></textarea>
                        </div>
                        
                        <div class="flex items-center">
                            <input id="terms" type="checkbox" value="" class="w-4 h-4 text-accent-color bg-gray-100 border-gray-300 rounded focus:ring-accent-color">
                            <label for="terms" class="ml-2 text-sm font-medium text-gray-700">我同意接收相关资讯和优惠信息</label>
                        </div>
                        
                        <button type="submit" class="btn-primary w-full">提交咨询</button>
                    </form>
                </div>
                
                <div class="fade-in">
                    <div class="bg-gray-50 p-8 rounded-lg h-full">
                        <h3 class="text-2xl font-bold mb-6 text-primary-color">联系方式</h3>
                        
                        <div class="space-y-6">
                            <div class="flex items-start">
                                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-accent-color flex items-center justify-center text-white">
                                    <i class="fas fa-map-marker-alt"></i>
                                </div>
                                <div class="ml-4">
                                    <h4 class="text-lg font-semibold text-gray-900">地址</h4>
                                    <p class="text-gray-600">calle villadecanes,1 28947 Fuenlabrada,Madrid</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-accent-color flex items-center justify-center text-white">
                                    <i class="fas fa-phone-alt"></i>
                                </div>
                                <div class="ml-4">
                                    <h4 class="text-lg font-semibold text-gray-900">电话</h4>
                                    <p class="text-gray-600">34695843753</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-accent-color flex items-center justify-center text-white">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div class="ml-4">
                                    <h4 class="text-lg font-semibold text-gray-900">邮箱</h4>
                                    <p class="text-gray-600">galaxyconstruccion9@gmail.com</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="flex-shrink-0 h-10 w-10 rounded-full bg-accent-color flex items-center justify-center text-white">
                                    <i class="fas fa-clock"></i>
                                </div>
                                <div class="ml-4">
                                    <h4 class="text-lg font-semibold text-gray-900">工作时间</h4>
                                    <p class="text-gray-600">周一至周日 9:00-21:00</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mt-8">
                            <h4 class="text-lg font-semibold text-gray-900 mb-4">关注我们</h4>
                            <div class="social-icons">
                                <a href="#" class="social-icon">
                                    <i class="fab fa-weixin"></i>
                                </a>
                                <a href="#" class="social-icon">
                                    <i class="fab fa-weibo"></i>
                                </a>
                                <a href="#" class="social-icon">
                                    <i class="fab fa-tiktok"></i>
                                </a>
                                <a href="#" class="social-icon">
                                    <i class="fab fa-instagram"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                    <h3 class="footer-title">关于我们</h3>
                    <p class="text-gray-400 mb-4">别墅设计装修图是专业的别墅设计案例展示平台，致力于为用户提供高质量的别墅设计参考和专业服务。</p>
                    <div class="social-icons">
                        <a href="#" class="social-icon">
                            <i class="fab fa-weixin"></i>
                        </a>
                        <a href="#" class="social-icon">
                            <i class="fab fa-weibo"></i>
                        </a>
                        <a href="#" class="social-icon">
                            <i class="fab fa-tiktok"></i>
                        </a>
                        <a href="#" class="social-icon">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h3 class="footer-title">快速链接</h3>
                    <ul class="footer-links">
                        <li><a href="#home">首页</a></li>
                        <li><a href="#cases">案例展示</a></li>
                        <li><a href="#3d-view">3D预览</a></li>
                        <li><a href="#designers">设计师</a></li>
                        <li><a href="#ai-style">AI风格匹配</a></li>
                        <li><a href="#contact">联系我们</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="footer-title">设计风格</h3>
                    <ul class="footer-links">
                        <li><a href="#">现代风格</a></li>
                        <li><a href="#">新中式风格</a></li>
                        <li><a href="#">欧式古典风格</a></li>
                        <li><a href="#">地中海风格</a></li>
                        <li><a href="#">北欧风格</a></li>
                        <li><a href="#">工业风格</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="footer-title">联系我们</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-map-marker-alt mr-2 text-accent-color"></i>calle villadecanes,1 28947 Fuenlabrada,Madrid </li>
                        <li><i class="fas fa-phone-alt mr-2 text-accent-color"></i> 695843753</li>
                        <li><i class="fas fa-envelope mr-2 text-accent-color"></i> galaxyconstruccion9@gmail.com</li>
                        <li><i class="fas fa-clock mr-2 text-accent-color"></i> 周一至周日 9:00-21:00</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 别墅设计装修图 </p>
            </div>
        </div>
    </footer>

    <script>
        // 页面加载完成后执行
        document.addEventListener('DOMContentLoaded', function() {
            // 加载动画
            setTimeout(function() {
                document.querySelector('.loader').classList.add('hidden');
            }, 1000);
            
            // 滚动动画
            const fadeElements = document.querySelectorAll('.fade-in');
            
            const fadeInOnScroll = function() {
                fadeElements.forEach(element => {
                    const elementTop = element.getBoundingClientRect().top;
                    const elementBottom = element.getBoundingClientRect().bottom;
                    
                    if (elementTop < window.innerHeight - 100 && elementBottom > 0) {
                        element.classList.add('active');
                    }
                });
            };
            
            // 初始检查
            fadeInOnScroll();
            
            // 滚动时检查
            window.addEventListener('scroll', fadeInOnScroll);
            
            // 导航栏滚动效果
            const header = document.getElementById('header');
            
            window.addEventListener('scroll', function() {
                if (window.scrollY > 50) {
                    header.classList.add('py-2');
                    header.classList.remove('py-4');
                } else {
                    header.classList.add('py-4');
                    header.classList.remove('py-2');
                }
            });
            
            // 移动端菜单
            const mobileMenuBtn = document.getElementById('mobile-menu-btn');
            const mobileMenu = document.querySelector('.mobile-menu');
            const mobileMenuClose = document.querySelector('.mobile-menu-close');
            const overlay = document.querySelector('.overlay');
            
            mobileMenuBtn.addEventListener('click', function() {
                mobileMenu.classList.add('active');
                overlay.classList.add('active');
                document.body.style.overflow = 'hidden';
            });
            
            function closeMenu() {
                mobileMenu.classList.remove('active');
                overlay.classList.remove('active');
                document.body.style.overflow = '';
            }
            
            mobileMenuClose.addEventListener('click', closeMenu);
            overlay.addEventListener('click', closeMenu);
            
            // 筛选功能
            const filterOptions = document.querySelectorAll('.filter-option');
            
            filterOptions.forEach(option => {
                option.addEventListener('click', function() {
                    this.classList.toggle('active');
                });
            });
            
            // 3D Viewer 模拟
            const viewerContainer = document.getElementById('viewer-container');
            let currentView = 'exterior';
            let rotation = 0;
            let zoom = 1;
            
            // 模拟3D场景
            function setupViewer() {
                // 在实际项目中，这里会使用Three.js创建真实的3D场景
                // 这里仅做简单模拟
                viewerContainer.style.background = 'linear-gradient(45deg, #f0f0f0 25%, #e0e0e0 25%, #e0e0e0 50%, #f0f0f0 50%, #f0f0f0 75%, #e0e0e0 75%, #e0e0e0 100%)';
                viewerContainer.style.backgroundSize = '20px 20px';
                
                const viewIndicator = document.createElement('div');
                viewIndicator.className = 'absolute inset-0 flex items-center justify-center text-2xl font-bold text-gray-500';
                viewIndicator.textContent = '3D ' + currentView.charAt(0).toUpperCase() + currentView.slice(1) + ' View';
                viewerContainer.appendChild(viewIndicator);
                
                // 控制按钮功能
                document.getElementById('rotate-left').addEventListener('click', function() {
                    rotation -= 45;
                    updateView();
                });
                
                document.getElementById('rotate-right').addEventListener('click', function() {
                    rotation += 45;
                    updateView();
                });
                
                document.getElementById('zoom-in').addEventListener('click', function() {
                    zoom += 0.1;
                    updateView();
                });
                
                document.getElementById('zoom-out').addEventListener('click', function() {
                    if (zoom > 0.5) {
                        zoom -= 0.1;
                        updateView();
                    }
                });
                
                document.getElementById('reset-view').addEventListener('click', function() {
                    rotation = 0;
                    zoom = 1;
                    updateView();
                });
                
                // 视图切换
                const viewButtons = document.querySelectorAll('[data-view]');
                viewButtons.forEach(button => {
                    button.addEventListener('click', function() {
                        currentView = this.getAttribute('data-view');
                        viewIndicator.textContent = '3D ' + currentView.charAt(0).toUpperCase() + currentView.slice(1) + ' View';
                        
                        // 更新按钮样式
                        viewButtons.forEach(btn => {
                            btn.classList.remove('bg-accent-color', 'text-white');
                            btn.classList.add('bg-gray-200');
                        });
                        this.classList.remove('bg-gray-200');
                        this.classList.add('bg-accent-color', 'text-white');
                    });
                });
            }
            
            function updateView() {
                // 在实际项目中，这里会更新Three.js场景的旋转和缩放
                // 这里仅做简单模拟
                const viewIndicator = viewerContainer.querySelector('div');
                viewIndicator.style.transform = `rotate(${rotation}deg) scale(${zoom})`;
            }
            
            setupViewer();
            
            // 平滑滚动
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                        
                        // 如果是移动端，点击后关闭菜单
                        if (mobileMenu.classList.contains('active')) {
                            closeMenu();
                        }
                    }
                });
            });
            
            // AI风格匹配系统模拟
            const uploadBtn = document.querySelector('.upload-btn');
            
            uploadBtn.addEventListener('click', function() {
                alert('请选择您的户型图文件上传');
                // 在实际项目中，这里会打开文件选择对话框
            });
            
            // 表单提交
            const contactForm = document.querySelector('#contact form');
            
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const name = document.getElementById('name').value;
                const phone = document.getElementById('phone').value;
                const email = document.getElementById('email').value;
                const message = document.getElementById('message').value;
                
                if (name && phone && email && message) {
                    alert('感谢您的咨询，我们会尽快与您联系！');
                    contactForm.reset();
                } else {
                    alert('请填写所有必填字段');
                }
            });
        });
    </script>
</body>
</html>
