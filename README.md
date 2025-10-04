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
                <a href="#" class="nav-link p-2 rounded-lg transition-colors hover:bg-gray-100 text-gray-600 hidden sm:inline">Doanh nghiệp xanh</a>
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
                    <img src="https://placehold.co/100x70/fffbe6/a16207?text=Video+Feedback" alt="Video/ảnh feedback thật" class="w-full h-auto mt-2 rounded-lg" onerror="this.onerror=null;this.src='https://placehold.co/100x70/fffbe6/a16207?text=Feedback';">
                </div>
            </div>

            <!-- Danh sách sản phẩm (Product Grid) -->
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <!-- Sản phẩm mẫu 1: Túi vải Canvas (Sử dụng image_4eb358.jpg) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <!-- Đã thay đổi đường dẫn ảnh thành tên file đơn giản -->
                    <img src="image_4eb358.jpg" alt="Túi vải Canvas Organic 3SACH MART" class="w-full h-40 object-cover" onerror="this.onerror=null;this.src='https://placehold.co/400x300/e0f2f1/0d9488?text=Tui+vai';">
                    <div class="p-4">
                        <div class="inline-block bg-emerald-100 text-emerald-800 text-xs font-medium px-2.5 py-0.5 rounded-full mb-2">Sản phẩm xanh</div>
                        <h4 class="text-lg font-bold text-gray-800 truncate">Túi vải Canvas Đa dụng (Tái chế)</h4>
                        <p class="text-xl font-extrabold stueco-text-green mt-1 mb-3">120.000 VNĐ</p>
                        <div class="flex gap-2 text-sm">
                            <button class="flex-1 py-2 stueco-green text-white font-semibold rounded-lg hover:bg-emerald-600 transition-colors">Thêm vào giỏ hàng</button>
                            <button class="flex-1 py-2 border border-emerald-500 text-emerald-500 font-semibold rounded-lg hover:bg-emerald-50 transition-colors">Mua ngay</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 2: Ống hút Tre (Sử dụng image_4eb3b6.jpg) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <!-- Đã thay đổi đường dẫn ảnh thành tên file đơn giản -->
                    <img src="image_4eb3b6.jpg" alt="Ống hút Tre tự nhiên" class="w-full h-40 object-cover" onerror="this.onerror=null;this.src='https://placehold.co/400x300/f0fdf4/4ade80?text=Ong+hut+Tre';">
                    <div class="p-4">
                        <div class="inline-block bg-emerald-100 text-emerald-800 text-xs font-medium px-2.5 py-0.5 rounded-full mb-2">Sản phẩm xanh</div>
                        <h4 class="text-lg font-bold text-gray-800 truncate">Bộ 6 Ống hút Tre tự nhiên</h4>
                        <p class="text-xl font-extrabold stueco-text-green mt-1 mb-3">45.000 VNĐ</p>
                        <div class="flex gap-2 text-sm">
                            <button class="flex-1 py-2 stueco-green text-white font-semibold rounded-lg hover:bg-emerald-600 transition-colors">Thêm vào giỏ hàng</button>
                            <button class="flex-1 py-2 border border-emerald-500 text-emerald-500 font-semibold rounded-lg hover:bg-emerald-50 transition-colors">Mua ngay</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 3: Xà phòng hữu cơ (Sử dụng image_4eb40f.jpg) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <!-- Đã thay đổi đường dẫn ảnh thành tên file đơn giản -->
                    <img src="image_4eb40f.jpg" alt="Xà phòng thảo mộc handmade" class="w-full h-40 object-cover" onerror="this.onerror=null;this.src='https://placehold.co/400x300/f5f5f4/78716c?text=Xa+phong';">
                    <div class="p-4">
                        <div class="inline-block bg-emerald-100 text-emerald-800 text-xs font-medium px-2.5 py-0.5 rounded-full mb-2">Sản phẩm xanh</div>
                        <h4 class="text-lg font-bold text-gray-800 truncate">Xà phòng thảo mộc Organic (100g)</h4>
                        <p class="text-xl font-extrabold stueco-text-green mt-1 mb-3">65.000 VNĐ</p>
                        <div class="flex gap-2 text-sm">
                            <button class="flex-1 py-2 stueco-green text-white font-semibold rounded-lg hover:bg-emerald-600 transition-colors">Thêm vào giỏ hàng</button>
                            <button class="flex-1 py-2 border border-emerald-500 text-emerald-500 font-semibold rounded-lg hover:bg-emerald-50 transition-colors">Mua ngay</button>
                        </div>
                    </div>
                </div>

                <!-- Sản phẩm mẫu 4: Bình nước Thủy tinh (Sử dụng image_4eb717.png) -->
                <div class="product-card bg-white rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
                    <!-- Đã thay đổi đường dẫn ảnh thành tên file đơn giản -->
                    <img src="image_4eb717.png" alt="Bình nước Thủy tinh tái chế 500ml" class="w-full h-40 object-contain p-2" onerror="this.onerror=null;this.src='https://placehold.co/400x300/ecfdf5/6ee7b7?text=Binh+nuoc';">
                    <div class="p-4">
                        <div class="inline-block bg-emerald-100 text-emerald-800 text-xs font-medium px-2.5 py-0.5 rounded-full mb-2">Sản phẩm xanh</div>
                        <h4 class="text-lg font-bold text-gray-800 truncate">Bình nước thủy tinh Mitomo 500ml</h4>
                        <p class="text-xl font-extrabold stueco-text-green mt-1 mb-3">150.000 VNĐ</p>
                        <div class="flex gap-2 text-sm">
                            <button class="flex-1 py-2 stueco-green text-white font-semibold rounded-lg hover:bg-emerald-600 transition-colors">Thêm vào giỏ hàng</button>
                            <button class="flex-1 py-2 border border-emerald-500 text-emerald-500 font-semibold rounded-lg hover:bg-emerald-50 transition-colors">Mua ngay</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Student Page (Trang kết nối sinh viên) -->
        <section id="students-view" class="view-section hidden">
            <div class="bg-white rounded-3xl shadow-2xl p-8 md:p-12 lg:p-16">
                <h2 class="text-4xl font-bold text-center mb-10 text-gray-900">
                    Sinh viên vừa học vừa trải nghiệm
                </h2>
                <p class="text-center text-2xl font-semibold stueco-text-green mb-12">
                    Gia nhập <span class="bg-emerald-200 px-3 py-1 rounded-full">Green Ambassador</span>
                </p>

                <div class="flex flex-col lg:flex-row gap-10">
                    <!-- Form đăng ký -->
                    <div class="lg:w-1/2">
                        <h3 class="text-2xl font-bold stueco-text-green mb-5">Đăng ký làm Cộng tác viên</h3>
                        <form class="space-y-4">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700">Họ và tên</label>
                                <input type="text" id="name" placeholder="Nguyễn Văn A" class="mt-1 block w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
                                <input type="email" id="email" placeholder="vana@stueco.vn" class="mt-1 block w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            </div>
                            <div>
                                <label for="phone" class="block text-sm font-medium text-gray-700">Số điện thoại</label>
                                <input type="tel" id="phone" placeholder="09xxxxxxxx" class="mt-1 block w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500">
                            </div>
                            <div>
                                <label for="reason" class="block text-sm font-medium text-gray-700">Lý do tham gia (Tùy chọn)</label>
                                <textarea id="reason" rows="3" placeholder="Tôi muốn lan tỏa lối sống xanh..." class="mt-1 block w-full p-3 border border-gray-300 rounded-lg focus:ring-emerald-500 focus:border-emerald-500"></textarea>
                            </div>
                            <button type="submit" class="w-full stueco-green text-white py-3 mt-4 font-bold rounded-xl shadow-lg hover:bg-emerald-600 transition-transform transform hover:scale-[1.01]">
                                Tham gia ngay
                            </button>
                        </form>
                    </div>

                    <!-- Lợi ích và Ảnh minh họa -->
                    <div class="lg:w-1/2 space-y-8">
                        <div>
                            <h3 class="text-2xl font-bold stueco-text-green mb-4">Lợi ích của Green Ambassador</h3>
                            <ul class="space-y-3 text-lg text-gray-700">
                                <li class="flex items-start">
                                    <span class="mr-2 text-xl stueco-text-green">✅</span>
                                    <span class="font-semibold">Tăng thu nhập:</span> Kiếm thêm hoa hồng từ việc giới thiệu sản phẩm.
                                </li>
                                <li class="flex items-start">
                                    <span class="mr-2 text-xl stueco-text-green">📚</span>
                                    <span class="font-semibold">Học kỹ năng marketing:</span> Trải nghiệm thực tế về bán hàng, content, livestream.
                                </li>
                                <li class="flex items-start">
                                    <span class="mr-2 text-xl stueco-text-green">🌍</span>
                                    <span class="font-semibold">Lan tỏa lối sống xanh:</span> Góp phần xây dựng cộng đồng bền vững.
                                </li>
                            </ul>
                        </div>
                        
                        <!-- Ảnh minh họa (Placeholder) -->
                        <div class="bg-gray-100 p-4 rounded-xl shadow-inner">
                            <img src="https://placehold.co/400x250/ccfbf1/047857?text=Student+Livestreaming+Green+Product" alt="Sinh viên livestream, giới thiệu sản phẩm xanh" class="w-full rounded-lg shadow-xl" onerror="this.onerror=null;this.src='https://placehold.co/400x250/ccfbf1/047857?text=Sinh+vien+gioi+thieu+san+pham';">
                            <p class="text-center text-sm text-gray-500 mt-2">Hình ảnh: Sinh viên giới thiệu sản phẩm xanh trên nền tảng số.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer (Tùy chọn) -->
    <footer class="bg-gray-800 text-white mt-12 py-6">
        <div class="container mx-auto px-4 text-center text-sm">
            &copy; 2025 STUECO – Sinh viên kết nối sản phẩm xanh.
        </div>
    </footer>

    <!-- JavaScript cho chức năng chuyển đổi view -->
    <script>
        // Hàm để chuyển đổi giữa các trang (view)
        function showView(viewId) {
            const views = document.querySelectorAll('.view-section');
            views.forEach(view => {
                view.classList.add('hidden');
            });
            document.getElementById(`${viewId}-view`).classList.remove('hidden');

            // Cập nhật trạng thái active của menu (tùy chọn)
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => {
                link.classList.remove('font-semibold', 'text-gray-800');
                link.classList.add('text-gray-600');
            });

            // Chỉ làm nổi bật Trang chủ, Sản phẩm, Sinh viên
            const currentLink = document.querySelector(`[onclick="showView('${viewId}')"]`);
            if (currentLink) {
                currentLink.classList.add('font-semibold', 'text-gray-800');
                currentLink.classList.remove('text-gray-600');
            }
        }

        // Khởi tạo hiển thị Trang chủ khi tải xong
        window.onload = () => {
            showView('home');
        };
    </script>
</body>
</html>
