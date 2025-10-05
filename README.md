<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STUECO - Sinh viên kết nối sản phẩm xanh</title>
    <!-- Tải Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Thiết lập font Inter và màu sắc tùy chỉnh -->
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f7f7;
        }
        /* Màu chủ đạo: Xanh lá cây (Emerald) */
        .stueco-green {
            background-color: #10B981; /* emerald-500 */
        }
        .stueco-text-green {
            color: #059669; /* emerald-600 */
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Header & Navigation -->
    <header class="bg-white shadow-lg sticky top-0 z-10">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-wrap items-center justify-between">
            <!-- Logo / Tên dự án -->
            <div class="text-xl font-bold stueco-text-green">
                STUECO <span class="text-sm font-normal text-gray-600 hidden md:inline">– Sinh viên kết nối sản phẩm xanh</span>
            </div>

            <!-- Thanh Menu -->
            <nav class="flex space-x-2 sm:space-x-4 text-sm mt-3 md:mt-0">
                <a href="#" onclick="showView('home')" class="nav-link p-2 rounded-lg transition-colors hover:bg-gray-100 font-semibold text-gray-800">Trang chủ</a>
                <a href="#" onclick="showView('products')" class="nav-link p-2 rounded-lg transition-colors hover:bg-gray-100 text-gray-600">Sản phẩm</a>
                <a href="#" onclick="showView('students')" class="nav-link p-2 rounded-lg transition-colors hover:bg-gray-100 text-gray-600">Sinh viên</a>
                <!-- ĐÃ CẬP NHẬT: Thêm onclick cho trang Doanh nghiệp xanh -->
                <a href="#" onclick="showView('partners')" class="nav-link p-2 rounded-lg transition-colors hover:bg-gray-100 text-gray-600 hidden sm:inline">Doanh nghiệp xanh</a>
                <a href="#" class="nav-link p-2 rounded-lg transition-colors hover:bg-gray-100 text-gray-600 flex items-center">
                    <!-- Icon Giỏ hàng (Lucide icon: Shopping Cart) -->
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="9" cy="21" r="1"/><circle cx="20" cy="21" r="1"/><path d="M1 1h4l2.68 12.08a2 2 0 0 0 2 1.92h9.4a2 2 0 0 0 2-1.92L23 6H6"/></svg>
                </a>
            </nav>
        </div>
    </header>

    <!-- Main Content Area -->
    <main class="flex-grow container mx-auto px-4 sm:px-6 lg:px-8 py-8">
        <!-- Home Page (Trang chủ) -->
        <section id="home-view" class="view-section">
            <!-- Banner Lớn -->
            <div class="stueco-green text-white p-8 md:p-16 rounded-3xl shadow-2xl mb-12 flex flex-col lg:flex-row items-center justify-between overflow-hidden">
                <div class="lg:w-1/2 mb-8 lg:mb-0">
                    <p class="text-xl font-medium mb-3">#STUECO</p>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight">
                        “Tiêu dùng xanh – <br class="hidden sm:inline"> Kết nối bền vững”
                    </h1>
                    <button onclick="showView('products')" class="mt-8 px-8 py-3 bg-white text-emerald-600 font-bold rounded-full shadow-xl hover:bg-gray-100 transition-transform transform hover:scale-105">
                        Khám phá ngay
                    </button>
                </div>
                <!-- Hình ảnh giả lập (Placeholder) -->
                <div class="lg:w-1/2 w-full flex justify-center lg:justify-end">
                    <img src="https://placehold.co/300x250/d1fae5/065f46?text=Student+%26+Green+Bag" alt="Hình ảnh sinh viên cầm túi vải / đồ xanh" class="rounded-2xl shadow-2xl object-cover" onerror="this.onerror=null;this.src='https://placehold.co/300x250/d1fae5/065f46?text=Sinh+vien+%26+San+pham+xanh';">
                </div>
            </div>

            <!-- Các ô Danh mục -->
            <h2 class="text-3xl font-bold stueco-text-green mb-6 text-center">Danh mục sản phẩm</h2>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
                <!-- Danh mục 1: Thực phẩm sạch -->
                <div class="bg-white p-6 rounded-2xl shadow-lg hover:shadow-xl transition-shadow text-center transform hover:scale-[1.02]">
                    <div class="text-5xl mb-4">🥕</div>
                    <h3 class="text-xl font-semibold stueco-text-green">Thực phẩm sạch</h3>
                    <p class="text-gray-500 text-sm mt-2">Nguồn gốc rõ ràng, không hóa chất độc hại.</p>
                </div>
                <!-- Danh mục 2: Đồ dùng tái chế -->
                <div class="bg-white p-6 rounded-2xl shadow-lg hover:shadow-xl transition-shadow text-center transform hover:scale-[1.02]">
                    <div class="text-5xl mb-4">♻️</div>
                    <h3 class="text-xl font-semibold stueco-text-green">Đồ dùng tái chế</h3>
                    <p class="text-gray-500 text-sm mt-2">Giảm rác thải, bảo vệ môi trường.</p>
                </div>
                <!-- Danh mục 3: Phụ kiện xanh -->
                <div class="bg-white p-6 rounded-2xl shadow-lg hover:shadow-xl transition-shadow text-center transform hover:scale-[1.02]">
                    <div class="text-5xl mb-4">🥤</div>
                    <h3 class="text-xl font-semibold stueco-text-green">Phụ kiện xanh</h3>
                    <p class="text-gray-500 text-sm mt-2">Ống hút tre, túi vải, bình nước thân thiện.</p>
                </div>
            </div>
        </section>

        <!-- Product Page (Trang sản phẩm) -->
        <section id="products-view" class="view-section hidden">
            <h2 class="text-4xl font-bold stueco-text-green mb-8 text-center">Khám phá Sản phẩm Xanh</h2>

            <!-- Bộ lọc và Review -->
            <div class="flex flex-col lg:flex-row gap-6 mb-8">
                <!-- Bộ lọc (Filters) -->
                <div class="lg:w-3/4 bg-white p-5 rounded-xl shadow-md">
                    <h3 class="text-lg font-semibold mb-3">Bộ lọc</h3>
                    <div class="flex flex-wrap gap-4 items-center">
                        <select class="p-2 border rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <option>Theo loại sản phẩm</option>
                            <option>Thực phẩm sạch</option>
                            <option>Đồ dùng tái chế</option>
                            <option>Phụ kiện xanh</option>
                        </select>
                        <select class="p-2 border rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <option>Theo doanh nghiệp</option>
                            <option>EcoLife</option>
                            <option>GreenFarm</option>
                        </select>
                        <select class="p-2 border rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <option>Giá</option>
                            <option>Dưới 100k</option>
                            <option>100k - 300k</option>
                        </select>
                    </div>
                </div>

                <!-- Góc nhỏ: Review sinh viên -->
                <div class="lg:w-1/4 bg-yellow-50 p-5 rounded-xl border-l-4 border-yellow-400 shadow-md">
                    <h3 class="text-lg font-bold text-yellow-800 mb-2">📣 Review sinh viên</h3>
                    <p class="text-sm text-gray-700 mb-3">
                        Xem video feedback thực tế từ cộng đồng Green Ambassador!
                    </p>
                    <a href="#" class="text-sm font-semibold text-yellow-700 hover:underline">Xem ngay →</a>
                    <!-- Ảnh/video placeholder -->
                    <img src="https://placehold.co/100x70/fffbe6/a16207?text=Video+Feedback" alt="Video/ảnh feedback thật" class="w-full h-auto mt-2 rounded-lg">
                </div>
            </div>

            <!-- Danh sách sản phẩm (Product Grid) -->
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                
                <!-- Sản phẩm mẫu 1: Túi vải Canvas -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- ĐÃ CẬP NHẬT: Thay thế ảnh placeholder bằng ảnh thật từ người dùng -->
                        <img src="uploaded:image_e92eaa.jpg-a3c72dab-5a59-4a85-934b-51f0e90ff6ea" alt="Túi vải Canvas Đa dụng (3SACH MART)" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Túi vải Canvas Đa dụng</h3>
                        <p class="text-sm text-gray-500">Phụ kiện xanh</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">89.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 2: Bộ 6 Ống hút Tre (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- Đã dùng ảnh placeholder miêu tả rõ ràng -->
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=6+Ống+Hút+Tre" alt="Bộ 6 Ống hút Tre tự nhiên" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Bộ 6 Ống hút Tre tự nhiên</h3>
                        <p class="text-sm text-gray-500">Phụ kiện xanh</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">45.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 3: Xà phòng thảo mộc (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- Đã dùng ảnh placeholder miêu tả rõ ràng -->
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=Xà+Phòng+Organic" alt="Xà phòng thảo mộc Organic" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Xà phòng thảo mộc Organic</h3>
                        <p class="text-sm text-gray-500">Đồ dùng tái chế</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">55.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 4: Bình nước thủy tinh (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- Đã dùng ảnh placeholder miêu tả rõ ràng -->
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=Bình+Nước+Thủy+Tinh" alt="Bình nước thủy tinh Mitomo" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Bình nước thủy tinh Mitomo (500ml)</h3>
                        <p class="text-sm text-gray-500">Phụ kiện xanh</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">120.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 5: Hộp cơm lúa mạch (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=Hộp+cơm+lúa+mạch" alt="Hộp cơm lúa mạch" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Hộp cơm lúa mạch 3 ngăn</h3>
                        <p class="text-sm text-gray-500">Đồ dùng tái chế</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">75.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 6: Rau củ hữu cơ (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- Cập nhật placeholder miêu tả số lượng -->
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=5+Rau+Củ+Hữu+Cơ" alt="Rau củ hữu cơ" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Combo Rau củ hữu cơ (5 món)</h3>
                        <p class="text-sm text-gray-500">Thực phẩm sạch</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">99.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>
                
                <!-- Sản phẩm mẫu 7: Bàn chải tre (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- Cập nhật placeholder miêu tả số lượng -->
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=3+Bàn+chải+Tre" alt="Bàn chải tre" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Bộ 3 Bàn chải tre thân thiện</h3>
                        <p class="text-sm text-gray-500">Phụ kiện xanh</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">35.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 8: Hạt dinh dưỡng (Vẫn dùng placeholder) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <div class="relative">
                        <!-- Cập nhật placeholder miêu tả rõ hơn -->
                        <img src="https://placehold.co/300x192/d1fae5/059669?text=Hạt+Diều+%26+Óc+Chó" alt="Hạt dinh dưỡng" class="w-full h-48 object-cover">
                        <span class="absolute top-2 right-2 bg-emerald-500 text-white text-xs font-semibold px-3 py-1 rounded-full shadow-md">Sản phẩm xanh</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-gray-800">Hạt óc chó & Hạnh nhân rang mộc</h3>
                        <p class="text-sm text-gray-500">Thực phẩm sạch</p>
                        <p class="mt-2 text-xl font-bold stueco-text-green">149.000₫</p>
                        <div class="mt-4 flex space-x-2">
                            <button class="flex-1 bg-emerald-500 text-white text-sm py-2 rounded-lg hover:bg-emerald-600 transition-colors">Mua ngay</button>
                            <button class="flex-1 border border-emerald-500 text-emerald-600 text-sm py-2 rounded-lg hover:bg-emerald-50 transition-colors">Thêm vào giỏ</button>
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <!-- Student Page (Trang kết nối sinh viên) -->
        <section id="students-view" class="view-section hidden">
            <div class="bg-white p-6 md:p-10 rounded-2xl shadow-2xl">
                <div class="flex flex-col lg:flex-row gap-8">
                    <!-- Nội dung và Form -->
                    <div class="lg:w-1/2">
                        <h2 class="text-3xl sm:text-4xl font-extrabold stueco-text-green mb-4">
                            Sinh viên vừa học vừa trải nghiệm – <br> Gia nhập Green Ambassador
                        </h2>
                        <p class="text-gray-600 mb-6">
                            Hãy trở thành Đại sứ Xanh để lan tỏa lối sống bền vững và phát triển bản thân!
                        </p>
                        
                        <!-- Lợi ích -->
                        <h3 class="text-xl font-bold text-gray-800 mb-3">🤝 Lợi ích của bạn:</h3>
                        <ul class="space-y-3 mb-8 text-gray-700">
                            <li class="flex items-start">
                                <span class="text-emerald-500 font-bold mr-2">✅</span> Tăng thu nhập, nhận hoa hồng hấp dẫn.
                            </li>
                            <li class="flex items-start">
                                <span class="text-emerald-500 font-bold mr-2">✅</span> Học kỹ năng Marketing, Bán hàng thực chiến.
                            </li>
                            <li class="flex items-start">
                                <span class="text-emerald-500 font-bold mr-2">✅</span> Lan tỏa lối sống xanh đến cộng đồng sinh viên.
                            </li>
                        </ul>

                        <!-- Form Đăng ký -->
                        <form class="space-y-4">
                            <h3 class="text-xl font-semibold stueco-text-green border-b pb-2 mb-4">Form Đăng ký Cộng tác viên</h3>
                            <input type="text" placeholder="Họ và tên" required class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <input type="email" placeholder="Email" required class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <input type="tel" placeholder="Số điện thoại" required class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <textarea placeholder="Lý do bạn muốn tham gia?" rows="3" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500"></textarea>
                            <button type="submit" class="w-full stueco-green text-white font-bold py-3 rounded-lg shadow-lg hover:bg-emerald-600 transition-colors transform hover:scale-[1.01]">
                                Tham gia ngay
                            </button>
                        </form>
                    </div>

                    <!-- Ảnh minh họa -->
                    <div class="lg:w-1/2 flex items-center justify-center">
                        <img src="https://placehold.co/400x400/ccfbf1/059669?text=Sinh+vien+Livestream" alt="Sinh viên livestream, giới thiệu sản phẩm xanh" class="rounded-xl shadow-2xl object-cover w-full h-auto">
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Partner Page (Trang kết nối Doanh nghiệp Xanh) -->
        <section id="partners-view" class="view-section hidden">
            <div class="bg-white p-6 md:p-10 rounded-2xl shadow-2xl">
                <div class="flex flex-col lg:flex-row-reverse gap-8">
                    <!-- Ảnh minh họa cho Doanh nghiệp Xanh -->
                    <div class="lg:w-1/2 flex items-center justify-center">
                        <img src="https://placehold.co/400x400/ccfbf1/059669?text=Ket+noi+Doanh+nghiep+xanh" alt="Doanh nghiệp hợp tác, kết nối" class="rounded-xl shadow-2xl object-cover w-full h-auto">
                    </div>

                    <!-- Nội dung và Form -->
                    <div class="lg:w-1/2">
                        <h2 class="text-3xl sm:text-4xl font-extrabold stueco-text-green mb-4">
                            Kết nối Doanh nghiệp Xanh & Cộng đồng Sinh viên
                        </h2>
                        <p class="text-gray-600 mb-6">
                            STUECO là cầu nối giúp doanh nghiệp tiếp cận gần **500,000 sinh viên**, thế hệ tiên phong cho lối sống bền vững và tiêu dùng có trách nhiệm.
                        </p>

                        <!-- Lợi ích -->
                        <h3 class="text-xl font-bold text-gray-800 mb-3">🚀 Lợi ích hợp tác:</h3>
                        <ul class="space-y-3 mb-8 text-gray-700">
                            <li class="flex items-start">
                                <span class="text-emerald-500 font-bold mr-2">✅</span> Tăng **nhận diện thương hiệu** với Gen Z.
                            </li>
                            <li class="flex items-start">
                                <span class="text-emerald-500 font-bold mr-2">✅</span> Đẩy mạnh hoạt động **CSR** (Trách nhiệm xã hội doanh nghiệp).
                            </li>
                            <li class="flex items-start">
                                <span class="text-emerald-500 font-bold mr-2">✅</span> Mở rộng **kênh phân phối** sản phẩm xanh trực tiếp đến sinh viên.
                            </li>
                        </ul>

                        <!-- Form Đăng ký -->
                        <form class="space-y-4">
                            <h3 class="text-xl font-semibold stueco-text-green border-b pb-2 mb-4">Đăng ký Hợp tác</h3>
                            <input type="text" placeholder="Tên Doanh nghiệp" required class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <input type="text" placeholder="Lĩnh vực hoạt động" required class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <input type="email" placeholder="Email liên hệ" required class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            <textarea placeholder="Thông điệp/yêu cầu hợp tác" rows="3" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500"></textarea>
                            <button type="submit" class="w-full stueco-green text-white font-bold py-3 rounded-lg shadow-lg hover:bg-emerald-600 transition-colors transform hover:scale-[1.01]">
                                Gửi thông tin
                            </button>
                        </form>
                    </div>

                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white mt-12">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-6 text-center text-sm">
            &copy; 2025 STUECO. | Phát triển vì cộng đồng xanh.
        </div>
    </footer>

    <!-- JavaScript for View Switching -->
    <script>
        // Hàm chuyển đổi giữa các trang (views)
        function showView(viewId) {
            document.querySelectorAll('.view-section').forEach(section => {
                section.classList.add('hidden');
            });
            document.getElementById(viewId + '-view').classList.remove('hidden');

            // Cập nhật trạng thái active của menu
            document.querySelectorAll('.nav-link').forEach(link => {
                // Đảm bảo chỉ có Trang chủ (home) là font-semibold mặc định
                if (link.getAttribute('onclick') !== `showView('home')`) {
                    link.classList.remove('font-semibold', 'text-gray-800');
                    link.classList.add('text-gray-600');
                }
            });
            const activeLink = document.querySelector(`[onclick="showView('${viewId}')"]`);
            if (activeLink) {
                activeLink.classList.remove('text-gray-600');
                activeLink.classList.add('font-semibold', 'text-gray-800');
            }
        }

        // Mặc định hiển thị trang chủ khi tải
        window.onload = () => {
            showView('home');
        };
    </script>
</body>
</html>
