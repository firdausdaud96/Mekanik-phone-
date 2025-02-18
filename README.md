// 1. Smooth Scrolling untuk Navigasi Halaman
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        const targetElement = document.getElementById(targetId);
        if (targetElement) {
            targetElement.scrollIntoView({
                behavior: 'smooth',
                block: 'start'
            });
        }
    });
});

// 2. Popup Promosi Istimewa
document.addEventListener('DOMContentLoaded', () => {
    const popup = document.getElementById('promo-popup');
    const closeBtn = document.getElementById('close-popup');

    // Tampilkan popup selepas 3 saat
    setTimeout(() => {
        popup.style.display = 'block';
    }, 3000);

    // Tutup popup apabila butang close ditekan
    closeBtn.addEventListener('click', () => {
        popup.style.display = 'none';
    });
});

// 3. Form Hubungi Kami - Simulasi Penghantaran Data
document.getElementById('contact-form').addEventListener('submit', function (e) {
    e.preventDefault(); // Mengelakkan penghantaran borang sebenar

    const name = document.getElementById('name').value;
    const phone = document.getElementById('phone').value;
    const message = document.getElementById('message').value;

    // Validasi input
    if (!name || !phone || !message) {
        alert('Sila isi semua medan.');
        return;
    }

    // Simulasi penghantaran data
    alert(`Terima kasih, ${name}! Pesanan anda telah diterima. Kami akan hubungi anda di ${phone}.`);

    // Reset borang
    this.reset();
});# Mekanik-phone-
Test
