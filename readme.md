# Subnet 29 - Coldint Validator

Subnet 29 adalah subnet Bittensor yang berfokus pada peningkatan model bahasa (LLM). Miners mendapatkan reward dengan melatih dan meningkatkan model yang menjadi objek penelitian.

## Fitur Utama

- Evaluasi asinkron melalui rantai Bittensor
- Penyimpanan model di Hugging Face
- Sistem reward berdasarkan performa model terhadap dataset Fineweb-2
- Mendukung berbagai arsitektur model (Llama, Phi, dll)

## Persyaratan Sistem

- Python 3.8+
- PyTorch 2.0+
- Transformers 4.44.0 (disarankan)
- Akun Hugging Face dengan token akses
- Disk space yang cukup untuk menyimpan model (min. 30GB)

## Instalasi

```bash
# Clone repository
git clone https://github.com/username/coldint-validator.git
cd coldint-validator

# Install dependencies
python -m pip install -e .
```

## Dokumentasi Terkait

- [Panduan Miner](docs/MINER.md) - Panduan lengkap untuk menjalankan miner
- [Langkah-langkah Setup](docs/SETUP.md) - Instruksi detail untuk setup awal
- [Sistem Reward](docs/REWARDS.md) - Penjelasan tentang mekanisme reward

## Lisensi

MIT License - lihat file [LICENSE](LICENSE) untuk detail lengkap