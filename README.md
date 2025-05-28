# Process_Mining_Project
This project is a web application that performs basic process mining analysis using a CSV file received from the user. It was developed using the Streamlit library.

- Vaka (Case ID) süreleri

- Adım frekansları (Hangi adım kaç kere geçilmiş?)

- Adımlar arası geçiş sayıları (Transition Matrix)

# Özellikler

- Basit ve kullanışlı bir arayüz

- CSV yüklenerek analiz

- Grafik ve tablo gösterimleri

- Streamlit tabanlı

## 🔧 Kullanılan Teknolojiler

- Python
- Streamlit
- PyNgrok
- Pandas
- Matplotlib / Seaborn
- Plotly
- Google Colab
## 📁## 📁 Proje Dosyaları

- `app.py` – Streamlit uygulamasının ana dosyası.
- `process_mining_data.csv` – Örnek veri üretici script tarafından oluşturulan CSV dosyası.
- `README.md` – Bu kılavuz dosyası.

#  Kurulum & Çalıştırma Adımları
### 1. Gerekli Kütüphanelerin Kurulumu
- !pip install streamlit pyngrok pandas matplotlib seaborn plotly

### 2. Uygulamayı Çalıştırma
- 1 Gerekli paketleri yükleyin
- 2 Uygulamayı çalıştırın
- 3 Tarayıcınızda http://localhost:8501 adresini açın
### 3. Kullanım 
#### 1. Uygulamayı başlattıktan sonra
-  CSV dosyası yükleyin" butonuna tıklayarak veri dosyanızı yükleyin
 ![1](https://github.com/user-attachments/assets/7a914046-c931-4e27-821f-319d33c7b499)

#### 2.Yüklenen veri otomatik olarak analiz edilecek
- Aktivite frekansları
- Case süreleri
- Ortalama süreç tamamlama süresi
- En sık geçişler
görselleştirmeleri gösterilecektir
![2](https://github.com/user-attachments/assets/4483689a-3e95-42d9-9b8d-f55375fe2b06)
![3](https://github.com/user-attachments/assets/fc140e31-261e-480b-a3e4-7a916cd53aed)
![4](https://github.com/user-attachments/assets/47df4a96-26ba-45ae-946a-36267de4d44c)



