import React, { useState } from "react";

const OshiNoKoRental = () => {
  const [activeTab, setActiveTab] = useState("home");
  
  return (
    <div className="min-h-screen bg-pink-50 font-sans">
      {/* Header */}
      <header className="bg-white shadow-md">
        <div className="container mx-auto px-4 py-4 flex flex-col md:flex-row justify-between items-center">
          <div className="flex items-center mb-4 md:mb-0">
            <img 
              src="https://placehold.co/60x60" 
              alt="Logo usaha rental cosplay Oshi no Ko dengan ilustrasi bintang dan pita" 
              className="mr-3"
            />
            <h1 className="text-2xl font-bold text-pink-600">OshiCosplay Rental</h1>
          </div>
          <nav className="flex space-x-6">
            <button 
              onClick={() => setActiveTab("home")}
              className={`text-lg font-medium ${activeTab === "home" ? "text-pink-600 underline" : "text-gray-700"}`}
               >
              Beranda
            </button>
            <button 
              onClick={() => setActiveTab("gallery")}
              className={`text-lg font-medium ${activeTab === "gallery" ? "text-pink-600 underline" : "text-gray-700"}`}
            >
              Kostum
            </button>
            <button 
              onClick={() => setActiveTab("about")}
              className={`text-lg font-medium ${activeTab === "about" ? "text-pink-600 underline" : "text-gray-700"}`}
            >
              Tentang Kami
            </button>
            <button 
              onClick={() => setActiveTab("contact")}
              className={`text-lg font-medium ${activeTab === "contact" ? "text-pink-600 underline" : "text-gray-700"}`}
            >
              Kontak
            </button>
          </nav>
        </div>
      </header>

       {/* Hero Section */}
      {activeTab === "home" && (
        <section className="container mx-auto px-4 py-12">
          <div className="bg-gradient-to-r from-pink-100 to-blue-100 rounded-2xl p-8 md:p-12 text-center">
            <h2 className="text-4xl font-bold text-pink-700 mb-6">Selamat Datang di OshiCosplay Rental</h2>
            <p className="text-xl text-gray-700 mb-8">
              Temukan kostum cosplay Oshi no Ko terbaik untuk acara dan foto shoot Anda!
            </p>
            <button 
              onClick={() => setActiveTab("gallery")}
              className="bg-pink-600 hover:bg-pink-700 text-white font-bold py-3 px-8 rounded-full text-lg transition duration-300"
            >
              Lihat Kostum Tersedia
            </button>
          </div>
          
          {/* Features */}
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8 mt-16">
            <div className="bg-white p-6 rounded-lg shadow-md text-center">
              <div className="bg-pink-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                <img 
                  src="https://placehold.co/40x40" 
                  alt="Icon kualitas tinggi dengan simbol bintang" 
                />
              </div>
              <h3 className="text-xl font-semibold mb-2">Kualitas Premium</h3>
              <p className="text-gray-600">Kostum dibuat dengan bahan berkualitas tinggi dan detail akurat.</p>
            </div>
            
            <div className="bg-white p-6 rounded-lg shadow-md text-center">
              <div className="bg-blue-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                <img 
                  src="https://placehold.co/40x40" 
                  alt="Icon harga terjangkau dengan simbol mata uang" 
                />
              </div>
               <h3 className="text-xl font-semibold mb-2">Harga Terjangkau</h3>
              <p className="text-gray-600">Sewa kostum favorit Anda dengan harga yang ramah kantong.</p>
            </div>
            
            <div className="bg-white p-6 rounded-lg shadow-md text-center">
              <div className="bg-pink-100 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
                <img 
                  src="https://placehold.co/40x40" 
                  alt="Icon pengiriman cepat dengan simbol paket" 
                />
              </div>
              <h3 className="text-xl font-semibold mb-2">Pengiriman Cepat</h3>
              <p className="text-gray-600">Kami siap mengirimkan pesanan Anda dengan cepat dan aman.</p>
            </div>
          </div>
        </section>
      )}
      
      {/* Gallery */}
      {activeTab === "gallery" && (
        <section className="container mx-auto px-4 py-12">
          <h2 className="text-3xl font-bold text-center text-pink-700 mb-10">Koleksi Kostum Oshi no Ko</h2>
          
          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
            {/* Kostum 1 */}
            <div className="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-lg transition duration-300">
              <img 
                src="https://placehold.co/400x500" 
                alt="Kostum Ai Hoshino dengan rambut pink, pita besar, dan pakaian idol yang cerah" 
                className="w-full h-64 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-bold text-pink-700 mb-2">Ai Hoshino - Idol Outfit</h3>
                <p className="text-gray-600 mb-4">Kostum idol dengan detail pita dan aksesori lengkap.</p>
                <div className="flex justify-between items-center">
                  <span className="font-bold text-lg">Rp 150.000/hari</span>
                  <button className="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded">
                    Sewa Sekarang
                  </button>
                </div>
              </div>
            </div>
            
              {/* Kostum 2 */}
            <div className="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-lg transition duration-300">
              <img 
                src="https://placehold.co/400x500" 
                alt="Kostum Ruby Hoshino dengan pakaian sekolah dan aksesori karakter" 
                className="w-full h-64 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-bold text-pink-700 mb-2">Ruby Hoshino - School Uniform</h3>
                <p className="text-gray-600 mb-4">Seragam sekolah dengan kemeja, dasi, dan rok lipit.</p>
                <div className="flex justify-between items-center">
                  <span className="font-bold text-lg">Rp 120.000/hari</span>
                  <button className="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded">
                    Sewa Sekarang
                  </button>
                </div>
              </div>
            </div>
            
           {/* Kostum 3 */}
            <div className="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-lg transition duration-300">
              <img 
                src="https://placehold.co/400x500" 
                alt="Kostum Aqua Hoshino dengan setelan panggung dan aksesori pita" 
                className="w-full h-64 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-bold text-pink-700 mb-2">Aqua Hoshino - Stage Costume</h3>
                <p className="text-gray-600 mb-4">Kostum panggung dengan detail bordir dan bahan mewah.</p>
                <div className="flex justify-between items-center">
                  <span className="font-bold text-lg">Rp 170.000/hari</span>
                  <button className="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded">
                    Sewa Sekarang
                  </button>
                </div>
              </div>
            </div>

             {/* Kostum 4 */}
            <div className="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-lg transition duration-300">
              <img 
                src="https://placehold.co/400x500" 
                alt="Kostum Kana Arima dengan gaun elegant dan aksesori rambut" 
                className="w-full h-64 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-bold text-pink-700 mb-2">Kana Arima - Elegant Dress</h3>
                <p className="text-gray-600 mb-4">Gaun elegan dengan sulaman detail dan bahan flowing.</p>
                <div className="flex justify-between items-center">
                  <span className="font-bold text-lg">Rp 160.000/hari</span>
                  <button className="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded">
                    Sewa Sekarang
                  </button>
                </div>
              </div>
            </div>

            {/* Kostum 5 */}
            <div className="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-lg transition duration-300">
              <img 
                src="https://placehold.co/400x500" 
                alt="Kostum Mem-cho dengan gaya idol colorful dan aksesori rambut" 
                className="w-full h-64 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-bold text-pink-700 mb-2">Mem-cho - Colorful Idol</h3>
                <p className="text-gray-600 mb-4">Kostum warna-warni dengan aksesori rambut khas karakter.</p>
                <div className="flex justify-between items-center">
                  <span className="font-bold text-lg">Rp 140.000/hari</span>
                  <button className="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded">
                    Sewa Sekarang
                  </button>
                </div>
              </div>
            </div>

             {/* Kostum 6 */}
            <div className="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-lg transition duration-300">
              <img 
                src="https://placehold.co/400x500" 
                alt="Kostum Akane Kurokawa dengan pakaian casual dan aksesori sederhana" 
                className="w-full h-64 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-bold text-pink-700 mb-2">Akane Kurokawa - Casual Outfit</h3>
                <p className="text-gray-600 mb-4">Pakaian kasual sehari-hari dengan sentuhan karakter.</p>
                <div className="flex justify-between items-center">
                  <span className="font-bold text-lg">Rp 110.000/hari</span>
                  <button className="bg-pink-600 hover:bg-pink-700 text-white py-2 px-4 rounded">
                    Sewa Sekarang
                  </button>
                </div>
              </div>
            </div>
          </div>
        </section>
      )}

       {/* About */}
      {activeTab === "about" && (
        <section className="container mx-auto px-4 py-12">
          <h2 className="text-3xl font-bold text-center text-pink-700 mb-10">Tentang Kami</h2>
          
          <div className="bg-white rounded-xl shadow-md p-8 max-w-4xl mx-auto">
            <div className="flex flex-col md:flex-row items-center mb-8">
              <img 
                src="https://placehold.co/200x200" 
                alt="Foto pemilik usaha rental cosplay Oshi no Ko" 
                className="rounded-full w-40 h-40 object-cover mb-4 md:mb-0 md:mr-8"
              />
              <div>
                <h3 className="text-2xl font-bold text-pink-700 mb-2">OshiCosplay Rental</h3>
                <p className="text-gray-700">
                  Kami adalah penyedia layanan sewa kostum cosplay khusus serial Oshi no Ko. 
                  Berdiri sejak 2023, kami berkomitmen memberikan pengalaman cosplay terbaik 
                  dengan kostum berkualitas tinggi dan detail yang akurat.
                </p>
              </div>
            </div>

            <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div className="bg-pink-50 p-4 rounded-lg">
                <h4 className="font-bold text-lg mb-2">Visi</h4>
                <p>
                  Menjadi penyedia kostum cosplay Oshi no Ko terpercaya dengan kualitas terbaik 
                  dan pelayanan memuaskan bagi seluruh komunitas cosplayer Indonesia.
                </p>
              </div>
              
              <div className="bg-blue-50 p-4 rounded-lg">
                <h4 className="font-bold text-lg mb-2">Misi</h4>
                <p>
                  Menyediakan kostum dengan detail akurat, bahan nyaman, dan harga terjangkau. 
                  Serta mendukung perkembangan komunitas cosplay di Indonesia.
                </p>
              </div>
            </div>
          </div>
        </section>
      )}

      {/* Contact */}
      {activeTab === "contact" && (
        <section className="container mx-auto px-4 py-12">
          <h2 className="text-3xl font-bold text-center text-pink-700 mb-10">Hubungi Kami</h2>
          
          <div className="bg-white rounded-xl shadow-md p-8 max-w-2xl mx-auto">
            <form className="space-y-6">
              <div>
                <label className="block text-gray-700 font-medium mb-2" htmlFor="name">
                  Nama Lengkap
                </label>
                <input
                  type="text"
                  id="name"
                  className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-500"
                  placeholder="Masukkan nama lengkap Anda"
                />
              </div>

              <div>
                <label className="block text-gray-700 font-medium mb-2" htmlFor="email">
                  Email
                </label>
                <input
                  type="email"
                  id="email"
                  className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-500"
                  placeholder="Masukkan alamat email Anda"
                />
              </div>

              <div>
                <label className="block text-gray-700 font-medium mb-2" htmlFor="message">
                  Pesan
                </label>
                <textarea
                  id="message"
                  rows={4}
                  className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-pink-500"
                  placeholder="Tulis pesan Anda di sini..."
                ></textarea>
              </div>

              <button
                type="
