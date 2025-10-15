<html lang="zh-CN"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>创新科技 - 引领未来科技的先锋企业</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        :root {
            --primary-color: #0B3D91;
            --secondary-color: #FFD700;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        
        .hero-bg {
            background-image: url('https://p3-flow-imagex-sign.byteimg.com/tos-cn-i-a9rns2rl98/rc/pc/super_tool/cdf03a4678474da68c834e7c8b5f7dbb~tplv-a9rns2rl98-image.image?rcl=202510132123355949300C4196FCD33ECC&rk3s=8e244e95&rrcfp=f06b921b&x-expires=1762953842&x-signature=2vK8XQIu78Gy3OZDnNbEZXfppxQ%3D');
            background-size: cover;
            background-position: center;
            position: relative;
        }
        
        .hero-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(11, 61, 145, 0.7);
            z-index: 1;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* 加载动画 */
        .loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--primary-color);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            transition: opacity 0.5s ease, visibility 0.5s ease;
        }
        
        .loader.hidden {
            opacity: 0;
            visibility: hidden;
        }
        
        .loader-spinner {
            width: 50px;
            height: 50px;
            border: 5px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: var(--secondary-color);
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        /* 响应式调整 */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .mobile-menu {
                display: none;
            }
            
            .mobile-menu.active {
                display: flex;
            }
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- 加载动画 -->
    <div class="loader">
        <div class="flex-content">
            <div class="loader-spinner"></div>
            <div class="text-white mt-4 text-xl">加载中...</div>
        </div>
    </div>

    <!-- 导航栏 -->
    <nav class="bg-white shadow shadowshadow shadow shadow shadow-md fixed fixed w-full z-50">
        <div class="container mx-auto px-4 py-3">
            <div class="flex justify justify-between items-center">
                <div class="flex items-center">
                    <a href="#" class="flex items items-center">
                        <span class="text-2xl font-bold text-blue-600">创新科技</span>
                    </a>
                </div>
                
                <!-- 桌面导航 -->
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">首页</a>
                    <a href="#about" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">关于我们</a>
                    <a href="#services" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">业务服务</a>
                    <a href="#cases" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">成功案例</a>
                    <a href="#contact" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">联系我们</a>
                </div>
                
                <!-- 移动端菜单按钮 -->
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-gray-800 focus:outline-none">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
            
            <!-- 移动端导航菜单 -->
            <div id="mobile-menu" class="mobile-menu flex-col space-y-4 py-4 mt-2">
                <a href="#home" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">首页</a>
                <a href="#about" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">关于我们</a>
                <a href="#service" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">业务服务</a>
                <a href="#cases" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">成功案例</a>
                <a href="#contact" class="text-gray-800 hover:text-blue-600 font-medium transition-colors">联系我们</a>
            </div>
        </div>
    </nav>

    <!-- 首屏 Hero 区域 -->
    <section id="home" class="hero-bg min-h-screen flex items-center">
        <div class="container mx-auto px-4 py-20 hero-content">
            <div class="max-w-3xl mx-auto text-center">
                <h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">引领<span class="text-yellow-400">UMWTV</span>，塑造<span class="text-yellow-400">未来</span>视界</h1>
                <p class="text-xl text-gray-100 mb-10">我们致力于提供前沿的科技解决方案，助力企业数字化转型，创造卓越价值</p>
                <div class="flex flex-col sm:flex-row justify-center gap-4">
                    <a href="#service" class="bg-yellow-400 hover:bg-yellow-500 text-blue-900 font-bold py-3 px-8 rounded-full transition-colors duration-300 transform hover:scale-105">
                        了解我们的服务
                    </a>
                    <a href="#contact" class="bg-transparent border-2 border-white text-white font-bold py-3 px-8 rounded-full transition-colors duration-300 hover:bg-white hover:text-blue-900">
                        联系我们
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- 关于我们 -->
    <section id="about" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">关于<span class="text-blue-600">创新科技</span></h2>
                <div class="w-24 h-1 bg-yellow-400 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">创新科技成立于2010年，是一家专注于为企业提供数字化转型解决方案的领先科技公司。我们拥有一支由行业专家组成的团队，致力于为客户创造卓越价值。</p>
            </div>
            
            <!-- 视频上传区域 -->
            <div class="max-w-4xl mx-auto mb-16 fade-in">
                <div class="bg-white rounded-xl shadow-xl p-8">
                    <h3 class="text-2xl font-bold mb-6 text-center">上传您的视频</h3>
                    
                    <div class="border-2 border-dashed border-blue-300 rounded-lg p-8 text-center hover:border-blue-500 transition-colors duration-300 cursor-pointer" id="upload-area">
                        <input type="file" id="video-upload" class="hidden" accept="video/*">
                        <div class="flex flex-col items-center justify-center">
                            <i class="fas fa-cloud-upload-alt text-blue-500 text-5xl mb-4"></i>
                            <p class="text-gray-600 mb-2">点击或拖拽视频文件到此处</p>
                            <p class="text-gray-400 text-sm">支持 MP4, MOV, AVI, WMV 等格式</p>
                            <button id="browse-button" class="mt-6 bg-blue-600 hover:bg-blue-700 text-white font-medium py-2 px-6 rounded-lg transition-colors duration-300">浏览文件</button>
                        </div>
                    </div>
                    
                    <!-- 上传进度条 -->
                    <div id="upload-progress" class="mt-6 hidden">
                        <div class="flex justify-between mb-1">
                            <span class="text-sm font-medium text-blue-600">上传进度</span>
                            <span id="progress-percentage" class="text-sm font-medium text-blue-600">0%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-2.5">
                            <div id="progress-bar" class="bg-blue-600 h-2.5 rounded-full" style="width: 0%"></div>
                        </div>
                    </div>
                    
                    <!-- 上传成功后的视频预览 -->
                    <div id="video-preview" class="mt-8 hidden">
                        <h4 class="text-xl font-bold mb-4">视频预览</h4>
                        <div class="relative rounded-lg overflow-hidden shadow-lg bg-black">
                            <video id="preview-video" class="w-full h-auto" controls=""></video>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="fade-in">
                    <img src="https://p26-doubao-search-sign.byteimg.com/mosaic-legacy/509300002583c85970ac~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&amp;x-expires=1765545826&amp;x-signature=JfiqFXbRnpXX00ACFH%2FhV%2B%2B%2FWvM%3D" alt="创新科技总部" class="rounded-lg shadow-xl w-full">
                </div>
                <div class="fade-in">
                    <h3 class="text-2xl font-bold mb-4 text-blue-600">我们的使命</h3>
                    <p class="text-gray-700 mb-6">通过创新科技赋能企业，推动数字化转型，助力客户在数字经济时代保持竞争优势。</p>
                    
                    <h3 class="text-2xl font-bold mb-4 text-blue-600">我们的愿景</h3>
                    <p class="text-gray-700 mb-6">成为全球领先的数字化转型解决方案提供商，引领行业创新发展。</p>
                    
                    <div class="grid grid-cols-2 gap-4 mt-8">
                        <div class="flex flex-col items-center p-4 bg-gray-50 rounded-lg">
                            <div class="text-4xl font-bold text-blue-600 mb-2">10+</div>
                            <div class="text-gray-600">年行业经验</div>
                        </div>
                        <div class="flex flex-col items-center p-4 bg-gray-50 rounded-lg">
                            <div class="text-4xl font-bold text-blue-600 mb-2">500+</div>
                            <div class="text-gray-600">成功项目</div>
                        </div>
                        <div class="flex flex-col items-center p-4 bg-gray-50 rounded-lg">
                            <div class="text-4xl font-bold text-blue-600 mb-2">200+</div>
                            <div class="text-gray-600">专业团队</div>
                        </div>
                        <div class="flex flex-col items-center p-4 bg-gray-50 rounded-lg">
                            <div class="text-4xl font-bold text-blue-600 mb-2">30+</div>
                            <div class="text-gray-600">合作伙伴</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 业务服务 -->
    <section id="service" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">我们的<span class="text-blue-600">业务服务</span></h2>
                <div class="w-24 h-1 bg-yellow-400 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">我们提供全方位的数字化转型解决方案，帮助企业在数字经济时代保持竞争优势。</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 服务卡片 1 -->
                <div class="bg-white rounded-lg shadow-lg p-8 card-hover fade-in">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-cloud text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">云计算服务</h3>
                    <p class="text-gray-700 mb-6">提供企业级云计算解决方案，包括云迁移、云原生应用开发、混合云架构设计等。</p>
                    <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                        了解更多 <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <!-- 服务卡片 2 -->
                <div class="bg-white rounded-lg shadow-lg p-8 card-hover fade-in">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-brain text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">人工智能解决方案</h3>
                    <p class="text-gray-700 mb-6">基于机器学习、自然语言处理等AI技术，为企业提供智能客服、数据分析等解决方案。</p>
                    <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                        了解更多 <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <!-- 服务卡片 3 -->
                <div class="bg-white rounded-lg shadow-lg p-8 card-hover fade-in">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-chart-line text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">大数据分析</h3>
                    <p class="text-gray-700 mb-6">通过大数据采集、存储、处理和分析技术，帮助企业挖掘数据价值，发现业务洞察。</p>
                    <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                        了解更多 <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <!-- 服务卡片 4 -->
                <div class="bg-white rounded-lg shadow-lg p-8 card-hover fade-in">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-mobile-alt text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">移动应用开发</h3>
                    <p class="text-gray-700 mb-6">为企业提供iOS和Android平台的移动应用开发服务，包括原生应用和混合应用开发。</p>
                    <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                        了解更多 <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <!-- 服务卡片 5 -->
                <div class="bg-white rounded-lg shadow-lg p-8 card-hover fade-in">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-shield-alt text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">网络安全服务</h3>
                    <p class="text-gray-700 mb-6">提供全面的网络安全解决方案，包括安全评估、渗透测试、安全监控、数据加密等。</p>
                    <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                        了解更多 <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
                
                <!-- 服务卡片 6 -->
                <div class="bg-white rounded-lg shadow-lg p-8 card-hover fade-in">
                    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
                        <i class="fas fa-cogs text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">DevOps解决方案</h3>
                    <p class="text-gray-700 mb-6">通过自动化工具和流程优化，帮助企业实现开发和运维的协同工作，提高软件交付速度。</p>
                    <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                        了解更多 <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- 成功案例 -->
    <section id="cases" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">成功<span class="text-blue-600">案例</span></h2>
                <div class="w-24 h-1 bg-yellow-400 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">我们已成功为众多行业领先企业提供数字化转型解决方案，以下是部分成功案例展示。</p>
            </div>
            
            <!-- 案例筛选 -->
            <div class="flex flex-wrap justify-center gap-4 mb-12">
                <button class="case-filter-btn active px-6 py-2 rounded-full bg-blue-600 text-white font-medium transition-colors hover:bg-blue-700" data-filter="all">全部案例</button>
                <button class="case-filter-btn px-6 py-2 rounded-full bg-gray-200 text-gray-800 font-medium transition-colors hover:bg-gray-300" data-filter="finance">金融行业</button>
                <button class="case-filter-btn px-6 py-2 rounded-full bg-gray-200 text-gray-800 font-medium transition-colors hover:bg-gray-300" data-filter="manufacturing">制造业</button>
                <button class="case-filter-btn px-6 py-2 rounded-full bg-gray-200 text-gray-800 font-medium transition-colors hover:bg-gray-300" data-filter="retail">零售行业</button>
            </div>
            
            <!-- 案例展示 -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 案例 1 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-lg fade-in" data-category="finance">
                    <img src="https://p26-doubao-search-sign.byteimg.com/labis/dc038b29a4173660a5989147f8c03066~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&amp;x-expires=1765545831&amp;x-signature=aeSnc0t1V5g531q9NmXKyR7QDvg%3D" alt="某大型银行数字化转型" class="w-full h-64 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">某大型银行数字化转型</h3>
                        <p class="text-gray-700 mb-4">为国内某大型银行提供全渠道数字化转型解决方案，实现了线上线下业务融合，提升了客户体验和运营效率。</p>
                        <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                            查看详情 <i class="fas fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>
                
                <!-- 案例 2 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-lg fade-in" data-category="manufacturing">
                    <img src="https://p26-doubao-search-sign.byteimg.com/labis/4fa7ad17b95ee7b0b7935f6185df37e8~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&amp;x-expires=1765545826&amp;x-signature=JDPXQYMmCQ2usO4Wv9rcaqE59kQ%3D" alt="智能制造解决方案" class="w-full h-64 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">智能制造解决方案</h3>
                        <p class="text-gray-700 mb-4">为某大型制造企业打造智能工厂，通过物联网、大数据和AI技术实现生产过程的实时监控和优化。</p>
                        <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                            查看详情 <i class="fas fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>
                
                <!-- 案例 3 -->
                <div class="bg-white rounded-lg overflow-hidden shadow-lg fade-in" data-category="retail">
                    <img src="https://p26-doubao-search-sign.byteimg.com/labis/0a389dd0e95a6e7e26791fc32ed3c418~tplv-be4g95zd3a-image.jpeg?rk3s=542c0f93&amp;x-expires=1765545826&amp;x-signature=CbF8R%2Bgm%2FVgDLkHzpdDXpckXr%2Bw%3D" alt="零售企业全渠道零售平台" class="w-full h-64 object-cover">
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">零售企业全渠道零售平台</h3>
                        <p class="text-gray-700 mb-4">为某知名零售企业构建全渠道零售平台，实现了线上线下库存、会员、营销的一体化管理。</p>
                        <a href="#" class="text-blue-600 hover:text-blue-800 font-medium flex items-center">
                            查看详情 <i class="fas fa-arrow-right ml-2"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold mb-4">联系<span class="text-blue-600">我们</span></h2>
                <div class="w-24 h-1 bg-yellow-400 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-3xl mx-auto">无论您有任何问题或需求，我们都将竭诚为您服务。请通过以下方式与我们联系。</p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <!-- 联系信息 -->
                <div class="fade-in">
                    <div class="bg-blue-600 text-white rounded-lg p-8 shadow-md mb-8">
                        <h3 class="text-2xl font-bold mb-6">联系方式</h3>
                        
                        <div class="flex items-start mb-6">
                            <div class="w-12 h-12 bg-white bg-opacity-20 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-map-marker-alt text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold mb-1">地址</h4>
                                <p>上海市浦东新区张江高科技园区科苑路88号</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start mb-6">
                            <div class="w-12 h-12 bg-white bg-opacity-20 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-phone-alt text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold mb-1">电话</h4>
                                <p>+86 21 5888 XXXX</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start mb-6">
                            <div class="w-12 h-12 bg-white bg-opacity-20 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-envelope text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold mb-1">邮箱</h4>
                                <p>info@innotech.com</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-white bg-opacity-20 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-clock text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold mb-1">工作时间</h4>
                                <p>周一至周五: 9:00 - 18:00</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-gray-900 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- 公司信息 -->
                <div>
                    <h3 class="text-xl font-bold mb-6">创新科技</h3>
                    <p class="text-gray-400 mb-6">引领创新科技，塑造未来世界。我们致力于为企业提供数字化转型解决方案，创造卓越价值。</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white transition-colors">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
                
                <!-- 快速链接 -->
                <div>
                    <h3 class="text-xl font-bold mb-6">快速链接</h3>
                    <ul class="space-y-3">
                        <li><a href="#home" class="text-gray-400 hover:text-white transition-colors">首页</a></li>
                        <li><a href="#about" class="text-gray-400 hover:text-white transition-colors">关于我们</a></li>
                        <li><a href="#service" class="text-gray-400 hover:text-white transition-colors">业务服务</a></li>
                        <li><a href="#cases" class="text-gray-400 hover:text-white transition-colors">成功案例</a></li>
                        <li><a href="#contact" class="text-gray-400 hover:text-white transition-colors">联系我们</a></li>
                    </ul>
                </div>
                
                <!-- 服务 -->
                <div>
                    <h3 class="text-xl font-bold mb-6">我们的服务</h3>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">云计算服务</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">人工智能解决方案</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">大数据分析</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">移动应用开发</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">网络安全服务</a></li>
                    </ul>
                </div>
                
                <!-- 订阅 -->
                <div>
                    <h3 class="text-xl font-bold mb-6">订阅我们</h3>
                    <p class="text-gray-400 mb-6">订阅我们的新闻通讯，获取最新的行业资讯和公司动态。</p>
                    <form class="flex">
                        <input type="email" placeholder="您的邮箱地址" class="px-4 py-2 w-full rounded-l-lg focus:outline-none text-gray-800">
                        <button type="submit" class="bg-yellow-400 hover:bg-yellow-500 text-blue-900 px-4 py-2 rounded-r-lg transition-colors">
                            <i class="fas fa-paper-plane"></i>
                        </button>
                    </form>
                </div>
            </div>
            
            <div class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-400 mb-4 md:mb-0">© 2023 创新科技. 保留所有权利.</p>
                <div class="flex space-x-6">
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">隐私政策</a>
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">服务条款</a>
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">网站地图</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // 页面加载完成后执行
        document.addEventListener('DOMContentLoaded', function() {
            // 背景音乐功能
            const audio = new Audio('https://freepd.com/music/Going%20Bananas.mp3');
            audio.volume = 0.8; // 默认音量80%
            audio.loop = true;
            
            // 创建音乐控制按钮
            const musicControlBtn = document.createElement('button');
            musicControlBtn.innerHTML = '<i class="fas fa-music"></i>';
            musicControlBtn.className = 'fixed bottom-6 right-6 bg-blue-600 text-white w-12 h-12 rounded-full flex items-center justify-center shadow-lg z-50 transition-all duration-300 hover:bg-blue-700';
            document.body.appendChild(musicControlBtn);
            
            // 尝试自动播放音乐（静音状态）
            audio.muted = true;
            audio.play().then(() => {
                console.log('背景音乐已自动播放（静音状态）');
            }).catch(error => {
                console.log('自动播放背景音乐失败:', error);
            });
            
            // 控制音乐播放/暂停
            musicControlBtn.addEventListener('click', function() {
                if (audio.paused) {
                    audio.play();
                    musicControlBtn.innerHTML = '<i class="fas fa-pause"></i>';
                } else {
                    audio.pause();
                    musicControlBtn.innerHTML = '<i class="fas fa-play"></i>';
                }
            });
            
            // 页面点击后取消静音
            document.addEventListener('click', function() {
                if (audio.muted) {
                    audio.muted = false;
                    console.log('背景音乐已取消静音');
                }
            }, { once: true });
            
            // 加载动画
            setTimeout(function() {
                document.querySelector('.loader').classList.add('hidden');
            }, 1500);
            
            // 移动端菜单切换
            const menuToggle = document.getElementById('menu-toggle');
            const mobileMenu = document.getElementById('mobile-menu');
            
            menuToggle.addEventListener('click', function() {
                mobileMenu.classList.toggle('active');
            });
            
            // 滚动动画
            const fadeElements = document.querySelectorAll('.fade-in');
            
            const fadeInOnScroll = function() {
                fadeElements.forEach(element => {
                    const elementTop = element.getBoundingClientRect().top;
                    const windowHeight = window.innerHeight;
                    
                    if (elementTop < windowHeight - 100) {
                        element.classList.add('visible');
                    }
                });
            };
            
            // 初始检查
            fadeInOnScroll();
            
            // 滚动时检查
            window.addEventListener('scroll', fadeInOnScroll);
            
            // 案例筛选
            const filterButtons = document.querySelectorAll('.case-filter-btn');
            const caseCards = document.querySelectorAll('[data-category]');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // 移除所有按钮的active类
                    filterButtons.forEach(btn => {
                        btn.classList.remove('active', 'bg-blue-600', 'text-white');
                        btn.classList.add('bg-gray-200', 'text-gray-800');
                    });
                    
                    // 添加当前按钮的active类
                    this.classList.add('active', 'bg-blue-600', 'text-white');
                    this.classList.remove('bg-gray-200', 'text-gray-800');
                    
                    const filter = this.getAttribute('data-filter');
                    
                    // 筛选案例卡片
                    caseCards.forEach(card => {
                        if (filter === 'all' || card.getAttribute('data-category') === filter) {
                            card.style.display = 'block';
                        } else {
                            card.style.display = 'none';
                        }
                    });
                });
            });
            
            // 视频上传功能
            const uploadArea = document.getElementById('upload-area');
            const videoUpload = document.getElementById('video-upload');
            const browseButton = document.getElementById('browse-button');
            const uploadProgress = document.getElementById('upload-progress');
            const progressBar = document.getElementById('progress-bar');
            const progressPercentage = document.getElementById('progress-percentage');
            const videoPreview = document.getElementById('video-preview');
            const previewVideo = document.getElementById('preview-video');
            
            // 浏览按钮点击事件
            browseButton.addEventListener('click', function() {
                videoUpload.click();
            });
            
            // 上传区域点击事件
            uploadArea.addEventListener('click', function() {
                videoUpload.click();
            });
            
            // 拖放功能
            uploadArea.addEventListener('dragover', function(e) {
                e.preventDefault();
                uploadArea.classList.add('border-blue-500');
            });
            
            uploadArea.addEventListener('dragleave', function() {
                uploadArea.classList.remove('border-blue-500');
            });
            
            uploadArea.addEventListener('drop', function(e) {
                e.preventDefault();
                uploadArea.classList.remove('border-blue-500');
                
                if (e.dataTransfer.files.length) {
                    handleVideoUpload(e.dataTransfer.files[0]);
                }
            });
            
            // 文件选择事件
            videoUpload.addEventListener('change', function() {
                if (this.files.length) {
                    handleVideoUpload(this.files[0]);
                }
            });
            
            // 处理视频上传
            function handleVideoUpload(file) {
                // 检查文件类型
                if (!file.type.startsWith('video/')) {
                    alert('请选择视频文件！');
                    return;
                }
                
                // 显示上传进度
                uploadProgress.classList.remove('hidden');
                
                // 模拟上传进度
                let progress = 0;
                const interval = setInterval(() => {
                    progress += Math.random() * 10;
                    if (progress > 100) {
                        progress = 100;
                        clearInterval(interval);
                        
                        // 上传完成后显示视频预览
                        setTimeout(() => {
                            const videoURL = URL.createObjectURL(file);
                            previewVideo.src = videoURL;
                            videoPreview.classList.remove('hidden');
                            
                            // 滚动到视频预览区域
                            videoPreview.scrollIntoView({ behavior: 'smooth', block: 'start' });
                        }, 500);
                    }
                    
                    progressBar.style.width = progress + '%';
                    progressPercentage.textContent = Math.round(progress) + '%';
                }, 300);
            }
        });
    </script>


</body></html>
