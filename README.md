# 📡 minitalk

`minitalk`, UNIX sinyalleri (SIGUSR1 / SIGUSR2) ile iki süreç arasında mesajlaşma yapılmasını sağlar. Bu projede, bir sunucu ve bir istemci bulunur.

## 📦 Bileşenler

- `server`: Gelen mesajları alır ve çözer
- `client`: Verilen PID'ye mesaj yollar

## 🛠️ Derleme

```bash
make
````

## 🚀 Kullanım

```bash
# Sunucuyu başlat
./server
# Çıktı: PID: 12345

# İstemci mesaj göndersin
./client 12345 "Merhaba dünya"
```

## 💡 Nasıl Çalışır?

Her karakter, bit bit gönderilir.

* SIGUSR1: `0`
* SIGUSR2: `1`

Sunucu gelen sinyalleri toparlayarak karakteri oluşturur.

## 🧠 Öğrenilenler

* `kill`, `signal`, `pause` gibi sinyal fonksiyonları
* Bit manipülasyonu
* Süreçler arası iletişim (IPC)
