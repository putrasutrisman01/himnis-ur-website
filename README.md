<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HIMNIS UR - Himpunan Mahasiswa Nias Universitas Riau</title>
    
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary-color: #C8102E;
            --secondary-color: #FFFFFF;
            --accent-color: #FFD700;
            --dark-color: #1a1a1a;
            --light-bg: #f8f9fa;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--dark-color);
        }

        /* Navbar */
        .navbar {
            background-color: var(--primary-color) !important;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .navbar-brand {
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--secondary-color) !important;
        }

        .navbar-nav .nav-link {
            color: var(--secondary-color) !important;
            font-weight: 500;
            margin: 0 10px;
            transition: all 0.3s ease;
        }

        .navbar-nav .nav-link:hover {
            color: var(--accent-color) !important;
        }

        /* Hero Section */
        .hero-section {
            position: relative;
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://picsum.photos/seed/nias-culture/1920/1080.jpg');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 30px;
        }

        .btn-custom {
            background-color: var(--primary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            border: none;
        }

        .btn-custom:hover {
            background-color: var(--accent-color);
            color: var(--dark-color);
            transform: translateY(-2px);
        }

        /* Section Styles */
        .section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--accent-color);
        }

        /* About Section */
        .about-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            height: 100%;
            transition: transform 0.3s ease;
        }

        .about-card:hover {
            transform: translateY(-10px);
        }

        .about-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        /* Program Cards */
        .program-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            margin-bottom: 30px;
        }

        .program-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .program-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .program-card-body {
            padding: 20px;
        }

        /* Gallery */
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            margin-bottom: 20px;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(200, 16, 46, 0.8);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        /* News Section */
        .news-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            height: 100%;
        }

        .news-card:hover {
            transform: translateY(-5px);
        }

        .news-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .news-card-body {
            padding: 20px;
        }

        .news-date {
            color: var(--primary-color);
            font-size: 0.9rem;
            font-weight: 500;
        }

        /* Contact Section */
        .contact-info {
            background: var(--primary-color);
            color: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 30px;
        }

        .contact-info i {
            font-size: 2rem;
            margin-bottom: 15px;
            color: var(--accent-color);
        }

        .form-control, .form-select {
            border-radius: 10px;
            border: 1px solid #ddd;
            padding: 12px;
            margin-bottom: 20px;
        }

        .form-control:focus, .form-select:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 0.2rem rgba(200, 16, 46, 0.25);
        }

        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 50px 0 20px;
        }

        .footer-widget h4 {
            color: var(--accent-color);
            margin-bottom: 20px;
            font-weight: 600;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            margin-right: 15px;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--accent-color);
        }

        /* Modal Login */
        .modal-content {
            border-radius: 15px;
            border: none;
        }

        .modal-header {
            background-color: var(--primary-color);
            color: white;
            border-radius: 15px 15px 0 0;
        }

        /* Chat Widget */
        #chatWidget {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
            display: none;
        }

        #chatButton {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: var(--primary-color);
            color: white;
            border: none;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            z-index: 999;
            transition: all 0.3s ease;
        }

        #chatButton:hover {
            background-color: var(--accent-color);
            transform: scale(1.1);
        }

        #chatContainer {
            width: 350px;
            height: 500px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            display: flex;
            flex-direction: column;
            overflow: hidden;
        }

        #chatHeader {
            background-color: var(--primary-color);
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        #chatMessages {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            background-color: #f5f5f5;
        }

        .chat-message {
            margin-bottom: 15px;
            padding: 10px;
            border-radius: 10px;
            max-width: 80%;
        }

        .chat-message.sent {
            background-color: var(--primary-color);
            color: white;
            margin-left: auto;
        }

        .chat-message.received {
            background-color: white;
            border: 1px solid #ddd;
        }

        .chat-message .sender {
            font-weight: bold;
            font-size: 0.8rem;
            margin-bottom: 5px;
        }

        .chat-message .time {
            font-size: 0.7rem;
            opacity: 0.7;
            margin-top: 5px;
        }

        #chatInput {
            display: flex;
            padding: 10px;
            background-color: white;
            border-top: 1px solid #ddd;
        }

        #chatInput input {
            flex: 1;
            border: 1px solid #ddd;
            border-radius: 20px;
            padding: 8px 15px;
            margin-right: 10px;
        }

        #chatInput button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            cursor: pointer;
        }

        /* Notification */
        .notification-container {
            position: fixed;
            top: 80px;
            right: 20px;
            z-index: 1050;
            max-width: 350px;
        }

        .notification {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            margin-bottom: 10px;
            padding: 15px;
            border-left: 4px solid var(--primary-color);
            animation: slideIn 0.3s ease;
        }

        @keyframes slideIn {
            from {
                transform: translateX(100%);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .notification .close {
            position: absolute;
            top: 10px;
            right: 10px;
            cursor: pointer;
            font-size: 18px;
        }

        /* Dashboard Admin */
        #adminDashboard {
            display: none;
            padding: 30px;
            background-color: var(--light-bg);
            border-radius: 15px;
            margin-top: 30px;
        }

        .stat-card {
            background: white;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
        }

        .stat-card i {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .stat-card h3 {
            font-size: 2rem;
            font-weight: 700;
            margin: 0;
        }

        /* Loading Animation */
        .loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: white;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }

        .spinner {
            width: 50px;
            height: 50px;
            border: 5px solid #f3f3f3;
            border-top: 5px solid var(--primary-color);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 60px 0;
            }

            #chatContainer {
                width: 90%;
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div class="loader" id="loader">
        <div class="spinner"></div>
    </div>

    <!-- Notification Container -->
    <div class="notification-container" id="notificationContainer"></div>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#home">
                <i class="fas fa-graduation-cap"></i> HIMNIS UR
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#home">Beranda</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">Profil</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#programs">Program</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#gallery">Galeri</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#news">Berita</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">Kontak</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="loginLink">
                            <i class="fas fa-user"></i> Anggota
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section">
        <div class="hero-content">
            <h1>Himpunan Mahasiswa Nias Universitas Riau<div>(HIMNIS UR)</div></h1>
            <p>Menjalin Kebersamaan, Melestarikan Budaya, Mencetak Prestasi</p>
            <a href="#about" class="btn btn-custom">Kenali Kami Lebih Dekat</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <div class="section-title">
                <h2>Tentang Kami</h2>
            </div>
            <div class="row">
                <div class="col-md-4 mb-4">
                    <div class="about-card text-center">
                        <i class="fas fa-history"></i>
                        <h4>Sejarah</h4>
                        <p>HIMNIS UR didirikan pada tahun 1995 sebagai wadah silaturahmi mahasiswa asal Nias di Universitas Riau. Hingga kini, organisasi ini terus berkembang dan memberikan kontribusi positif bagi kampus dan masyarakat.</p>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="about-card text-center">
                        <i class="fas fa-bullseye"></i>
                        <h4>Visi &amp; Misi</h4>
                        <p><strong>Visi:</strong> Menjadi organisasi kemahasiswaan yang unggul dalam menjaga kebudayaan Nias dan mencetak generasi muda yang berkarakter.</p>
                        <p><strong>Misi:</strong> Membina kekerabatan, melestarikan budaya, dan meningkatkan prestasi akademik anggota.</p>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="about-card text-center">
                        <i class="fas fa-users"></i>
                        <h4>Struktur Organisasi</h4>
                        <p>Dipimpin oleh Ketua Umum dan dibantu oleh Sekretaris Umum serta Bendahara Umum. Didukung oleh divisi-divisi yang bergerak di berbagai bidang sesuai kebutuhan organisasi.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Programs Section -->
    <section id="programs" class="section" style="background-color: var(--light-bg);">
        <div class="container">
            <div class="section-title">
                <h2>Program &amp; Kegiatan</h2>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <div class="program-card">
                        <img src="https://picsum.photos/seed/budaya-nias/400/200.jpg" alt="Pelestarian Budaya">
                        <div class="program-card-body">
                            <h5>Pelestarian Budaya Nias</h5>
                            <p>Kegiatan rutin untuk melestarikan budaya Nias melalui tari, musik, dan adat istiadat.</p>
                            <a href="#" class="btn btn-sm btn-custom">Selengkapnya</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="program-card">
                        <img src="https://picsum.photos/seed/akademik/400/200.jpg" alt="Bimbingan Akademik">
                        <div class="program-card-body">
                            <h5>Bimbingan Akademik</h5>
                            <p>Program mentoring untuk membantu anggota mencapai prestasi akademik yang optimal.</p>
                            <a href="#" class="btn btn-sm btn-custom">Selengkapnya</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="program-card">
                        <img src="https://picsum.photos/seed/sosial/400/200.jpg" alt="Kegiatan Sosial">
                        <div class="program-card-body">
                            <h5>Kegiatan Sosial</h5>
                            <p>Bakti sosial dan pengabdian masyarakat sebagai bentuk kepedulian terhadap sesama.</p>
                            <a href="#" class="btn btn-sm btn-custom">Selengkapnya</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="section">
        <div class="container">
            <div class="section-title">
                <h2>Galeri Kegiatan</h2>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <div class="gallery-item">
                        <img src="https://picsum.photos/seed/kegiatan1/400/300.jpg" alt="Kegiatan 1">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus fa-3x text-white"></i>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="gallery-item">
                        <img src="https://picsum.photos/seed/kegiatan2/400/300.jpg" alt="Kegiatan 2">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus fa-3x text-white"></i>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="gallery-item">
                        <img src="https://picsum.photos/seed/kegiatan3/400/300.jpg" alt="Kegiatan 3">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus fa-3x text-white"></i>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="gallery-item">
                        <img src="https://picsum.photos/seed/kegiatan4/400/300.jpg" alt="Kegiatan 4">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus fa-3x text-white"></i>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="gallery-item">
                        <img src="https://picsum.photos/seed/kegiatan5/400/300.jpg" alt="Kegiatan 5">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus fa-3x text-white"></i>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="gallery-item">
                        <img src="https://picsum.photos/seed/kegiatan6/400/300.jpg" alt="Kegiatan 6">
                        <div class="gallery-overlay">
                            <i class="fas fa-search-plus fa-3x text-white"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- News Section -->
    <section id="news" class="section" style="background-color: var(--light-bg);">
        <div class="container">
            <div class="section-title">
                <h2>Berita &amp; Artikel</h2>
            </div>
            <div class="row" id="newsContainer">
                <!-- News items will be loaded here -->
            </div>
        </div>
    </section>

    <!-- Registration Section -->
    <section class="section">
        <div class="container">
            <div class="section-title">
                <h2>Pendaftaran Anggota Baru</h2>
            </div>
            <div class="row justify-content-center">
                <div class="col-md-8">
                    <div class="card">
                        <div class="card-body p-5">
                            <form id="registrationForm">
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label class="form-label">Nama Lengkap</label>
                                            <input type="text" class="form-control" name="nama" required>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label class="form-label">NIM</label>
                                            <input type="text" class="form-control" name="nim" required>
                                        </div>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label class="form-label">Fakultas</label>
                                            <select class="form-select" name="fakultas" required>
                                                <option value="">Pilih Fakultas</option>
                                                <option value="teknik">Fakultas Teknik</option>
                                                <option value="ekonomi">Fakultas Ekonomi</option>
                                                <option value="hukum">Fakultas Hukum</option>
                                                <option value="kedokteran">Fakultas Kedokteran</option>
                                                <option value="pertanian">Fakultas Pertanian</option>
                                                <option value="kip">Fakultas KIP</option>
                                                <option value="perikanan">Fakultas Perikanan</option>
                                                <option value="isipol">Fakultas ISIPOL</option>
                                            </select>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label class="form-label">Jurusan</label>
                                            <input type="text" class="form-control" name="jurusan" required>
                                        </div>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label class="form-label">Email</label>
                                            <input type="email" class="form-control" name="email" required>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <label class="form-label">No. HP</label>
                                            <input type="tel" class="form-control" name="noHp" required>
                                        </div>
                                    </div>
                                </div>
                                <div class="mb-3">
                                    <label class="form-label">Asal Daerah (Kabupaten/Kota di Nias)</label>
                                    <input type="text" class="form-control" name="asalDaerah" required>
                                </div>
                                <div class="mb-3">
                                    <label class="form-label">Alasan Bergabung</label>
                                    <textarea class="form-control" name="alasan" rows="3" required></textarea>
                                </div>
                                <div class="text-center">
                                    <button type="submit" class="btn btn-custom btn-lg">Daftar Sekarang</button>
                                </div>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section" style="background-color: var(--light-bg);">
        <div class="container">
            <div class="section-title">
                <h2>Hubungi Kami</h2>
            </div>
            <div class="row">
                <div class="col-md-4">
                    <div class="contact-info text-center">
                        <i class="fas fa-map-marker-alt"></i>
                        <h5>Alamat</h5>
                        <p>Sekretariat HIMNIS UR<br>Gedung Kemahasiswaan Lt. 2<br>Universitas Riau, Pekanbaru</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-info text-center">
                        <i class="fas fa-phone"></i>
                        <h5>Telepon</h5>
                        <p>+62 812-3456-7890<br>+62 823-4567-8901</p>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="contact-info text-center">
                        <i class="fas fa-envelope"></i>
                        <h5>Email</h5>
                        <p>himnis@unri.ac.id<br>info@himnisur.org</p>
                    </div>
                </div>
            </div>
            <div class="row mt-5">
                <div class="col-md-8 mx-auto">
                    <form id="contactForm">
                        <div class="row">
                            <div class="col-md-6">
                                <input type="text" class="form-control" name="nama" placeholder="Nama Anda" required>
                            </div>
                            <div class="col-md-6">
                                <input type="email" class="form-control" name="email" placeholder="Email Anda" required>
                            </div>
                        </div>
                        <input type="text" class="form-control" name="subjek" placeholder="Subjek" required>
                        <textarea class="form-control" name="pesan" rows="5" placeholder="Pesan Anda" required></textarea>
                        <div class="text-center">
                            <button type="submit" class="btn btn-custom btn-lg mt-3">Kirim Pesan</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Admin Dashboard (Hidden by default) -->
    <section id="adminDashboard" class="section">
        <div class="container">
            <div class="section-title">
                <h2>Dashboard Admin</h2>
            </div>
            <div class="row">
                <div class="col-md-3">
                    <div class="stat-card">
                        <i class="fas fa-users text-primary"></i>
                        <h3 id="totalMembers">0</h3>
                        <p>Total Anggota</p>
                    </div>
                </div>
                <div class="col-md-3">
                    <div class="stat-card">
                        <i class="fas fa-user-plus text-success"></i>
                        <h3 id="newRegistrations">0</h3>
                        <p>Pendaftaran Baru</p>
                    </div>
                </div>
                <div class="col-md-3">
                    <div class="stat-card">
                        <i class="fas fa-envelope text-warning"></i>
                        <h3 id="newMessages">0</h3>
                        <p>Pesan Masuk</p>
                    </div>
                </div>
                <div class="col-md-3">
                    <div class="stat-card">
                        <i class="fas fa-calendar-check text-info"></i>
                        <h3 id="activeActivities">0</h3>
                        <p>Kegiatan Aktif</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <div class="footer-widget">
                        <h4>Tentang HIMNIS UR</h4>
                        <p>Himpunan Mahasiswa Nias Universitas Riau adalah wadah silaturahmi dan pengembangan potensi mahasiswa suku Nias di Universitas Riau.</p>
                        <div class="social-links mt-3">
                            <a href="#"><i class="fab fa-facebook"></i></a>
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                            <a href="#"><i class="fab fa-youtube"></i></a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="footer-widget">
                        <h4>Link Cepat</h4>
                        <ul class="list-unstyled">
                            <li><a href="#about" class="text-white text-decoration-none">Profil</a></li>
                            <li><a href="#programs" class="text-white text-decoration-none">Program Kerja</a></li>
                            <li><a href="#gallery" class="text-white text-decoration-none">Galeri</a></li>
                            <li><a href="#news" class="text-white text-decoration-none">Berita</a></li>
                            <li><a href="#contact" class="text-white text-decoration-none">Kontak</a></li>
                        </ul>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="footer-widget">
                        <h4>Newsletter</h4>
                        <p>Dapatkan informasi terbaru dari HIMNIS UR</p>
                        <form id="newsletterForm">
                            <div class="input-group mb-3">
                                <input type="email" class="form-control" placeholder="Email Anda" name="email">
                                <button class="btn btn-custom" type="submit">Subscribe</button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
            <hr class="my-4" style="border-color: #444;">
            <div class="text-center">
                <p>© 2023 HIMNIS UR. All Rights Reserved. | Developed with <i class="fas fa-heart text-danger"></i> for Nias Community</p>
            </div>
        </div>
    </footer>

    <!-- Login Modal -->
    <div class="modal fade" id="loginModal" tabindex="-1">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Login Anggota</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button>
                </div>
                <div class="modal-body p-4">
                    <form id="loginForm">
                        <div class="mb-3">
                            <label class="form-label">NIM</label>
                            <input type="text" class="form-control" name="nim" required>
                        </div>
                        <div class="mb-3">
                            <label class="form-label">Password</label>
                            <input type="password" class="form-control" name="password" required>
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="rememberMe">
                            <label class="form-check-label" for="rememberMe">Ingat saya</label>
                        </div>
                        <button type="submit" class="btn btn-custom w-100">Login</button>
                    </form>
                    <div class="text-center mt-3">
                        <a href="#" class="text-decoration-none">Lupa password?</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Chat Widget -->
    <button id="chatButton" onclick="toggleChat()">
        <i class="fas fa-comments"></i>
    </button>
    <div id="chatWidget">
        <div id="chatContainer">
            <div id="chatHeader">
                <h5 class="mb-0">Chat HIMNIS UR</h5>
                <button class="btn btn-sm text-white" onclick="toggleChat()">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            <div id="chatMessages">
                <div class="chat-message received">
                    <div class="sender">HIMNIS UR Bot</div>
                    <div>Selamat datang di chat HIMNIS UR! Silakan ajukan pertanyaan Anda.</div>
                    <div class="time">Just now</div>
                </div>
            </div>
            <div id="chatInput">
                <input type="text" placeholder="Ketik pesan..." id="messageInput">
                <button onclick="sendMessage()">
                    <i class="fas fa-paper-plane"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    
    <!-- Firebase SDK -->
    <script src="https://www.gstatic.com/firebasejs/9.15.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.15.0/firebase-auth-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.15.0/firebase-database-compat.js"></script>
    
    <script>
        // Firebase Configuration - GANTI dengan konfigurasi Firebase Anda
        const firebaseConfig = {
            apiKey: "YOUR_API_KEY",
            authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
            databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com",
            projectId: "YOUR_PROJECT_ID",
            storageBucket: "YOUR_PROJECT_ID.appspot.com",
            messagingSenderId: "YOUR_SENDER_ID",
            appId: "YOUR_APP_ID"
        };

        // Initialize Firebase
        firebase.initializeApp(firebaseConfig);
        const auth = firebase.auth();
        const database = firebase.database();

        // Google Sheets Configuration - GANTI dengan URL Apps Script Anda
        const GOOGLE_SCRIPT_URL = 'https://script.google.com/macros/s/WEB_APP_ID/exec';

        // Backend Server Configuration - GANTI dengan URL server Anda
        const BACKEND_URL = 'http://localhost:3000/api';

        // Hide loader when page is loaded
        window.addEventListener('load', function() {
            setTimeout(function() {
                document.getElementById('loader').style.opacity = '0';
                setTimeout(function() {
                    document.getElementById('loader').style.display = 'none';
                }, 500);
            }, 1000);
            
            // Check login status
            checkLoginStatus();
            
            // Load news
            loadNews();
            
            // Load dashboard stats if admin
            loadDashboardStats();
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Navbar background on scroll
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.backgroundColor = 'rgba(200, 16, 46, 0.95)';
            } else {
                navbar.style.backgroundColor = 'var(--primary-color)';
            }
        });

        // Check login status
        function checkLoginStatus() {
            const isLoggedIn = localStorage.getItem('isLoggedIn') === 'true';
            const userData = JSON.parse(localStorage.getItem('userData') || '{}');
            
            if (isLoggedIn && userData.nim) {
                const loginLink = document.getElementById('loginLink');
                loginLink.innerHTML = `<i class="fas fa-user"></i> ${userData.nama}`;
                loginLink.removeAttribute('data-bs-toggle');
                loginLink.addEventListener('click', function(e) {
                    e.preventDefault();
                    if (confirm('Logout?')) {
                        logout();
                    }
                });
                
                // Show chat button for logged in users
                document.getElementById('chatButton').style.display = 'block';
                
                // Show admin dashboard if admin
                if (userData.role === 'admin') {
                    document.getElementById('adminDashboard').style.display = 'block';
                }
            }
        }

        // Registration Form Handler (Google Sheets + Firebase)
        document.getElementById('registrationForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = new FormData(this);
            const data = Object.fromEntries(formData);
            
            // Show loading
            showNotification('Memproses pendaftaran...', 'info');
            
            // Send to Google Sheets
            fetch(`${GOOGLE_SCRIPT_URL}?sheetName=Registrations`, {
                method: 'POST',
                body: JSON.stringify(data),
                mode: 'no-cors'
            })
            .then(() => {
                // Create Firebase user
                const email = `${data.nim}@unri.ac.id`;
                const password = 'himnis123'; // Default password
                
                auth.createUserWithEmailAndPassword(email, password)
                    .then((userCredential) => {
                        // Save additional data to Firebase
                        database.ref('users/' + userCredential.user.uid).set({
                            nama: data.nama,
                            nim: data.nim,
                            fakultas: data.fakultas,
                            jurusan: data.jurusan,
                            email: data.email,
                            noHp: data.noHp,
                            asalDaerah: data.asalDaerah,
                            role: 'member',
                            registrationDate: new Date().toISOString()
                        });
                        
                        // Send to backend server
                        fetch(`${BACKEND_URL}/register`, {
                            method: 'POST',
                            headers: {
                                'Content-Type': 'application/json'
                            },
                            body: JSON.stringify(data)
                        });
                        
                        showNotification('Pendaftaran berhasil! Kami telah mengirim email konfirmasi.', 'success');
                        this.reset();
                    })
                    .catch((error) => {
                        console.error('Error creating user:', error);
                        showNotification('Pendaftaran berhasil namun gagal membuat akun. Silakan hubungi admin.', 'warning');
                    });
            })
            .catch(error => {
                console.error('Error:', error);
                showNotification('Terjadi kesalahan. Silakan coba lagi.', 'error');
            });
        });

        // Contact Form Handler (Google Sheets + Backend)
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = new FormData(this);
            const data = Object.fromEntries(formData);
            
            // Show loading
            showNotification('Mengirim pesan...', 'info');
            
            // Send to Google Sheets
            fetch(`${GOOGLE_SCRIPT_URL}?sheetName=Contacts`, {
                method: 'POST',
                body: JSON.stringify(data),
                mode: 'no-cors'
            })
            .then(() => {
                // Send to backend server
                fetch(`${BACKEND_URL}/contact`, {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json'
                    },
                    body: JSON.stringify(data)
                });
                
                showNotification('Pesan Anda telah terkirim! Kami akan segera merespons.', 'success');
                this.reset();
            })
            .catch(error => {
                console.error('Error:', error);
                showNotification('Terjadi kesalahan. Silakan coba lagi.', 'error');
            });
        });

        // Login Form Handler (Firebase + Backend)
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = new FormData(this);
            const data = Object.fromEntries(formData);
            
            // Show loading
            showNotification('Memproses login...', 'info');
            
            // Login with Firebase
            const email = `${data.nim}@unri.ac.id`;
            
            auth.signInWithEmailAndPassword(email, data.password)
                .then((userCredential) => {
                    // Get user data from Firebase
                    database.ref('users/' + userCredential.user.uid).once('value')
                        .then((snapshot) => {
                            const userData = snapshot.val();
                            
                            // Verify with backend
                            fetch(`${BACKEND_URL}/login`, {
                                method: 'POST',
                                headers: {
                                    'Content-Type': 'application/json'
                                },
                                body: JSON.stringify(data)
                            })
                            .then(response => response.json())
                            .then(backendData => {
                                if (backendData.success) {
                                    // Save login state
                                    localStorage.setItem('isLoggedIn', 'true');
                                    localStorage.setItem('userData', JSON.stringify(userData));
                                    
                                    showNotification('Login berhasil! Selamat datang ' + userData.nama, 'success');
                                    bootstrap.Modal.getInstance(document.getElementById('loginModal')).hide();
                                    this.reset();
                                    
                                    // Reload to update UI
                                    location.reload();
                                } else {
                                    showNotification('Login gagal: ' + backendData.message, 'error');
                                }
                            });
                        });
                })
                .catch((error) => {
                    showNotification('Login gagal: ' + error.message, 'error');
                });
        });

        // Newsletter Form Handler
        document.getElementById('newsletterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const email = this.querySelector('input[name="email"]').value;
            
            // Send to Google Sheets
            fetch(`${GOOGLE_SCRIPT_URL}?sheetName=Newsletter`, {
                method: 'POST',
                body: JSON.stringify({ email: email }),
                mode: 'no-cors'
            })
            .then(() => {
                showNotification('Terima kasih telah berlangganan newsletter!', 'success');
                this.reset();
            })
            .catch(error => {
                showNotification('Terjadi kesalahan. Silakan coba lagi.', 'error');
            });
        });

        // Logout function
        function logout() {
            auth.signOut()
                .then(() => {
                    localStorage.removeItem('isLoggedIn');
                    localStorage.removeItem('userData');
                    showNotification('Anda telah logout', 'info');
                    location.reload();
                });
        }

        // Load news from backend
        function loadNews() {
            fetch(`${BACKEND_URL}/news`)
                .then(response => response.json())
                .then(data => {
                    const newsContainer = document.getElementById('newsContainer');
                    newsContainer.innerHTML = '';
                    
                    data.forEach(news => {
                        const newsCard = `
                            <div class="col-md-4 mb-4">
                                <div class="news-card">
                                    <img src="${news.image || 'https://picsum.photos/seed/news' + news.id + '/400/200.jpg'}" alt="${news.title}">
                                    <div class="news-card-body">
                                        <div class="news-date">
                                            <i class="far fa-calendar"></i> ${new Date(news.date).toLocaleDateString('id-ID')}
                                        </div>
                                        <h5>${news.title}</h5>
                                        <p>${news.content.substring(0, 100)}...</p>
                                        <a href="#" class="btn btn-sm btn-custom">Baca Selengkapnya</a>
                                    </div>
                                </div>
                            </div>
                        `;
                        newsContainer.innerHTML += newsCard;
                    });
                })
                .catch(error => {
                    console.error('Error loading news:', error);
                    // Fallback to static news
                    const newsContainer = document.getElementById('newsContainer');
                    newsContainer.innerHTML = `
                        <div class="col-md-4 mb-4">
                            <div class="news-card">
                                <img src="https://picsum.photos/seed/berita1/400/200.jpg" alt="Berita 1">
                                <div class="news-card-body">
                                    <div class="news-date">
                                        <i class="far fa-calendar"></i> 15 November 2023
                                    </div>
                                    <h5>Festival Budaya Nias 2023</h5>
                                    <p>HIMNIS UR sukses menyelenggarakan Festival Budaya Nias yang dihadiri oleh ratusan peserta...</p>
                                    <a href="#" class="btn btn-sm btn-custom">Baca Selengkapnya</a>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 mb-4">
                            <div class="news-card">
                                <img src="https://picsum.photos/seed/berita2/400/200.jpg" alt="Berita 2">
                                <div class="news-card-body">
                                    <div class="news-date">
                                        <i class="far fa-calendar"></i> 10 November 2023
                                    </div>
                                    <h5>Pengukuhan Pengurus Baru</h5>
                                    <p>Prosesi pengukuhan pengurus HIMNIS UR periode 2023/2024 berlangsung khidmat...</p>
                                    <a href="#" class="btn btn-sm btn-custom">Baca Selengkapnya</a>
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 mb-4">
                            <div class="news-card">
                                <img src="https://picsum.photos/seed/berita3/400/200.jpg" alt="Berita 3">
                                <div class="news-card-body">
                                    <div class="news-date">
                                        <i class="far fa-calendar"></i> 5 November 2023
                                    </div>
                                    <h5>Bakti Sosial di Desa Adat</h5>
                                    <p>Kegiatan bakti sosial HIMNIS UR memberikan dampak positif bagi masyarakat...</p>
                                    <a href="#" class="btn btn-sm btn-custom">Baca Selengkapnya</a>
                                </div>
                            </div>
                        </div>
                    `;
                });
        }

        // Load dashboard stats
        function loadDashboardStats() {
            const userData = JSON.parse(localStorage.getItem('userData') || '{}');
            
            if (userData.role === 'admin') {
                // Fetch stats from backend
                fetch(`${BACKEND_URL}/stats`)
                    .then(response => response.json())
                    .then(data => {
                        document.getElementById('totalMembers').textContent = data.totalMembers || 0;
                        document.getElementById('newRegistrations').textContent = data.newRegistrations || 0;
                        document.getElementById('newMessages').textContent = data.newMessages || 0;
                        document.getElementById('activeActivities').textContent = data.activeActivities || 0;
                    })
                    .catch(error => {
                        console.error('Error loading stats:', error);
                    });
            }
        }

        // Chat functions
        function toggleChat() {
            const chatWidget = document.getElementById('chatWidget');
            chatWidget.style.display = chatWidget.style.display === 'none' ? 'block' : 'none';
        }

        function sendMessage() {
            const input = document.getElementById('messageInput');
            const message = input.value.trim();
            
            if (message) {
                const userData = JSON.parse(localStorage.getItem('userData') || '{}');
                
                // Add message to UI
                addMessageToChat(message, userData.nama || 'Anonymous', 'sent');
                
                // Send to Firebase
                database.ref('chat').push({
                    user: userData.nama || 'Anonymous',
                    nim: userData.nim || 'Guest',
                    message: message,
                    timestamp: new Date().toISOString()
                });
                
                input.value = '';
                
                // Simulate bot response
                setTimeout(() => {
                    const responses = [
                        'Terima kasih atas pesan Anda. Kami akan segera merespons.',
                        'Pesan Anda telah diterima. Tim HIMNIS UR akan membantu Anda.',
                        'Mohon tunggu sebentar, kami akan segera merespons pesan Anda.'
                    ];
                    const randomResponse = responses[Math.floor(Math.random() * responses.length)];
                    addMessageToChat(randomResponse, 'HIMNIS UR Bot', 'received');
                }, 1000);
            }
        }

        function addMessageToChat(message, sender, type) {
            const chatMessages = document.getElementById('chatMessages');
            const messageElement = document.createElement('div');
            messageElement.className = `chat-message ${type}`;
            messageElement.innerHTML = `
                <div class="sender">${sender}</div>
                <div>${message}</div>
                <div class="time">${new Date().toLocaleTimeString()}</div>
            `;
            chatMessages.appendChild(messageElement);
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }

        // Listen for new chat messages
        database.ref('chat').on('child_added', (snapshot) => {
            const message = snapshot.val();
            const userData = JSON.parse(localStorage.getItem('userData') || '{}');
            
            // Don't show own messages
            if (message.nim !== userData.nim) {
                addMessageToChat(message.message, message.user, 'received');
            }
        });

        // Notification system
        function showNotification(message, type = 'info') {
            const container = document.getElementById('notificationContainer');
            const notification = document.createElement('div');
            notification.className = 'notification';
            
            const colors = {
                success: '#28a745',
                error: '#dc3545',
                warning: '#ffc107',
                info: '#17a2b8'
            };
            
            notification.style.borderLeftColor = colors[type] || colors.info;
            notification.innerHTML = `
                <span class="close" onclick="this.parentElement.remove()">&times;</span>
                <div>${message}</div>
            `;
            
            container.appendChild(notification);
            
            // Auto remove after 5 seconds
            setTimeout(() => {
                notification.remove();
            }, 5000);
        }

        // Gallery lightbox effect
        document.querySelectorAll('.gallery-item').forEach(item => {
            item.addEventListener('click', function() {
                const img = this.querySelector('img');
                const modal = document.createElement('div');
                modal.style.cssText = `
                    position: fixed;
                    top: 0;
                    left: 0;
                    width: 100%;
                    height: 100%;
                    background: rgba(0,0,0,0.9);
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    z-index: 9999;
                    cursor: pointer;
                `;
                modal.innerHTML = `<img src="${img.src}" style="max-width: 90%; max-height: 90%; object-fit: contain;">`;
                modal.addEventListener('click', () => modal.remove());
                document.body.appendChild(modal);
            });
        });

        // Listen for login state changes
        auth.onAuthStateChanged((user) => {
            if (user) {
                // User is signed in
                const userData = JSON.parse(localStorage.getItem('userData') || '{}');
                if (!userData.nim) {
                    // Get user data from Firebase
                    database.ref('users/' + user.uid).once('value')
                        .then((snapshot) => {
                            const userData = snapshot.val();
                            localStorage.setItem('userData', JSON.stringify(userData));
                            checkLoginStatus();
                        });
                }
            } else {
                // User is signed out
                if (localStorage.getItem('isLoggedIn') === 'true') {
                    localStorage.removeItem('isLoggedIn');
                    localStorage.removeItem('userData');
                    location.reload();
                }
            }
        });
    </script>
</body>
</html>
