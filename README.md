# Process_Mining_Project
Bu proje, kullanıcıdan alınan bir CSV dosyasını kullanarak temel süreç madenciliği analizi gerçekleştiren bir web uygulamasıdır. Streamlit kütüphanesi kullanılarak geliştirilmiştir.

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
Google Colab ortamında çalışıyorsanız:

```python
!pip install streamlit pyngrok pandas matplotlib seaborn plotly
```
Yerel bir ortamda çalışacaksanız:
```python
pip install streamlit pyngrok pandas matplotlib seaborn plotly
```

### 2. Uygulamayı Çalıştırma
- 1 Gerekli paketleri yükleyin
- 2 Ngrok Token Ayarlayın :
  -  Google Colab üzerinde userdata.get("KEY") kullanılarak otomatik alınması önerilir. Alternatif olarak doğrudan token’ı elle verebilirsiniz:
   ```
     ngrok.set_auth_token("NGROK_TOKENINIZ")
   ```
- 3 app.py Dosyasını Oluşturun ve Çalıştırın:
   ```
   %%writefile app.py
   # (buraya app.py içeriğini yapıştırın)
   ```
- 4 Ngrok Tünelini Başlatın ve Streamlit'i Çalıştırın:
  
```python
from pyngrok import ngrok
from pyngrok.conf import PyngrokConfig
from IPython import get_ipython
public_url = ngrok.connect(addr=8501, proto="http", pyngrok_config=PyngrokConfig(region="eu"))
print(f"Uygulamanız şu adreste erişilebilir: {public_url}")
get_ipython().system('streamlit run app.py --server.port 8501 --server.headless true &>/dev/null &')

```
- 5 Uygulamayı çalıştırın
- 6 Tarayıcınızda http://localhost:8501 adresini açın
### 3. Kullanım 
#### 1. Uygulamayı başlattıktan sonra
-  CSV dosyası yükleyin" butonuna tıklayarak veri dosyanızı yükleyin
 ![1](https://github.com/user-attachments/assets/7a914046-c931-4e27-821f-319d33c7b499)

#### 2.Yüklenen veri otomatik olarak analiz edilecek
#### Veri Önizleme :
 ![2](https://github.com/user-attachments/assets/4483689a-3e95-42d9-9b8d-f55375fe2b06)
#### Aktivite frekansları ve Case süreleri
#### Ortalama süreç tamamlama süresi
 ![3](https://github.com/user-attachments/assets/fc140e31-261e-480b-a3e4-7a916cd53aed)


####  En sık geçişler
görselleştirmeleri gösterilecektir

![4](https://github.com/user-attachments/assets/47df4a96-26ba-45ae-946a-36267de4d44c)

### 4.Kullanım Notları
#### Yüklenen CSV dosyası şu sütunları içermelidir:

-Case ID

-Activity Name

-Start Time

-End Time

##### Uygulama yüklenen dosyadaki tarih bilgilerini datetime formatına çevirir ve Duration hesaplar.

##### Plotly ve Graphviz ile dinamik grafikler oluşturur.

##### Geçiş analizi için süreç sıralaması yapılır.

## Geliştirici
#### Ad Soyad : Enes Elmerdud
#### Bilgisayar Mühendisliği Öğrencisi 
#### 📧 Email: enesmerdud26@gmail.com
#### 📘 GitHub: [https://github.com/AnasMardood](https://github.com/AnasMardood)
