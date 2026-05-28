    <div class="form-body" id="formSection">
        <div class="section-title">Online Randevu Talebi</div>
        
        <form id="appointmentForm">
            <div class="form-group">
                <label>Ad Soyad <span class="required">*</span></label>
                <input type="text" id="fullName" placeholder="Adınız ve soyadınız" required>
            </div>

            <div class="form-group">
                <label>Telefon Numarası <span class="required">*</span></label>
                <input type="tel" id="phone" placeholder="05XX XXX XX XX" required>
            </div>

            <div class="form-group">
                <label>E-posta Adresi</label>
                <input type="email" id="email" placeholder="ornek@email.com">
            </div>

            <div class="form-group">
                <label>Etkinlik Türü <span class="required">*</span></label>
                <select id="eventType" required>
                    <option value="">Seçiniz...</option>
                    <option value="Düğün">Düğün</option>
                    <option value="Nişan">Nişan</option>
                    <option value="Kına Gecesi">Kına Gecesi</option>
                    <option value="Dış Çekim">Dış Çekim</option>
                    <option value="Söz">Söz</option>
                    <option value="Doğum Günü">Doğum Günü</option>
                    <option value="Özel Etkinlik">Özel Etkinlik</option>
                </select>
            </div>

            <div class="form-group">
                <label>Etkinlik Tarihi <span class="required">*</span></label>
                <input type="date" id="eventDate" required>
            </div>

            <div class="form-group">
                <label>Etkinlik Yeri / Şehir <span class="required">*</span></label>
                <select id="city" required>
                    <option value="">Şehir seçiniz...</option>
                    <option value="Gaziantep">Gaziantep</option>
                    <option value="Şanlıurfa">Şanlıurfa</option>
                    <option value="Kahramanmaraş">Kahramanmaraş</option>
                    <option value="Adıyaman">Adıyaman</option>
                    <option value="Adana">Adana</option>
                    <option value="Hatay">Hatay</option>
                    <option value="İskenderun">İskenderun</option>
                    <option value="Kilis">Kilis</option>
                    <option value="Diğer">Diğer</option>
                </select>
            </div>

            <div class="form-group">
                <label>Mekan Adı</label>
                <input type="text" id="venue" placeholder="Düğün salonu, otel vb.">
            </div>

            <div class="form-group">
                <label>İstediğiniz Hizmetler <span class="required">*</span></label>
                <div class="services-grid">
                    <input type="checkbox" id="service1" class="service-checkbox" value="Fotoğraf Çekimi">
                    <label for="service1" class="service-label">📸 Fotoğraf</label>

                    <input type="checkbox" id="service2" class="service-checkbox" value="Video Çekimi">
                    <label for="service2" class="service-label">🎥 Video</label>

                    <input type="checkbox" id="service3" class="service-checkbox" value="Drone Çekimi">
                    <label for="service3" class="service-label">🚁 Drone</label>

                    <input type="checkbox" id="service4" class="service-checkbox" value="Klip Çekimi">
                    <label for="service4" class="service-label">🎬 Klip</label>

                    <input type="checkbox" id="service5" class="service-checkbox" value="Albüm">
                    <label for="service5" class="service-label">📔 Albüm</label>

                    <input type="checkbox" id="service6" class="service-checkbox" value="Canlı Yayın">
                    <label for="service6" class="service-label">📡 Canlı Yayın</label>

                    <input type="checkbox" id="service7" class="service-checkbox" value="Jimijip">
                    <label for="service7" class="service-label">🎞️ Jimijip</label>

                    <input type="checkbox" id="service8" class="service-checkbox" value="YouTube Canlı Yayın">
                    <label for="service8" class="service-label">▶️ YouTube Live</label>

                    <input type="checkbox" id="service9" class="service-checkbox" value="Profesyonel Prodüksiyon">
                    <label for="service9" class="service-label">🎭 Prodüksiyon</label>
                </div>
            </div>

            <div class="form-group">
                <label>Ek Notlar / Özel İstekler</label>
                <textarea id="notes" placeholder="Bize iletmek istediğiniz ek bilgiler..."></textarea>
            </div>

            <button type="submit" class="whatsapp-btn">
                <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M21 11.5a8.38 8.38 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.38 8.38 0 0 1-3.8-.9L3 21l1.9-5.7a8.38 8.38 0 0 1-.9-3.8 8.5 8.5 0 0 1 4.7-7.6 8.38 8.38 0 0 1 3.8-.9h.5a8.48 8.48 0 0 1 8 8v.5z"></path>
                </svg>
                WhatsApp ile Randevu Talebi Gönder
            </button>
        </form>

        <div class="footer-info">
            <p>📍 Değirmiçem Mah. Nail Bilen Cad. Barış Apt. No:9/F, Gaziantep</p>
            <span class="phone">📞 0532 675 15 12</span>
            <p style="margin-top: 8px;">
                <a href="https://instagram.com/wedding_art_gaziantep" target="_blank">@wedding_art_gaziantep</a>
            </p>
            <p style="margin-top: 5px; font-size: 0.75rem;">Randevulu sistem - Her zaman çekime çıkabiliyoruz</p>
        </div>
    </div>

    <div class="success-message" id="successMessage">
        <div class="success-icon">✅</div>
        <h2>Randevu Talebiniz Hazır!</h2>
        <p>WhatsApp açılacak ve bilgileriniz otomatik olarak iletilecek.</p>
    </div>
</div>

<script>
    document.getElementById('appointmentForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        const fullName = document.getElementById('fullName').value;
        const phone = document.getElementById('phone').value;
        const email = document.getElementById('email').value;
        const eventType = document.getElementById('eventType').value;
        const eventDate = document.getElementById('eventDate').value;
        const city = document.getElementById('city').value;
        const venue = document.getElementById('venue').value;
        const notes = document.getElementById('notes').value;
        
        const selectedServices = [];
        document.querySelectorAll('.service-checkbox:checked').forEach(function(checkbox) {
            selectedServices.push(checkbox.value);
        });
        
        let message = `*Wedding Art Gaziantep - Randevu Talebi* %0A%0A`;
        message += `*Ad Soyad:* ${fullName}%0A`;
        message += `*Telefon:* ${phone}%0A`;
        if (email) message += `*E-posta:* ${email}%0A`;
        message += `%0A*Etkinlik Detayları*%0A`;
        message += `*Tür:* ${eventType}%0A`;
        message += `*Tarih:* ${eventDate}%0A`;
        message += `*Şehir:* ${city}%0A`;
        if (venue) message += `*Mekan:* ${venue}%0A`;
        message += `%0A*İstenen Hizmetler:*%0A`;
        selectedServices.forEach(function(service) {
            message += `• ${service}%0A`;
        });
        if (notes) message += `%0A*Ek Notlar:* ${notes}%0A`;
        message += `%0A_Bu mesaj Wedding Art Gaziantep online randevu formundan gönderilmiştir._`;
        
        const whatsappNumber = '905326751512';
        const whatsappUrl = `https://wa.me/${whatsappNumber}?text=${message}`;
        
        document.getElementById('formSection').classList.add('hidden');
        document.getElementById('successMessage').classList.add('show');
        
        setTimeout(function() {
            window.open(whatsappUrl, '_blank');
        }, 1000);
    });
</script>
