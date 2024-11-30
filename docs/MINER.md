# Panduan Miner Subnet 29

## Gambaran Umum

Miners pada Subnet 29 bertugas untuk meningkatkan model bahasa yang menjadi objek penelitian. Proses ini berjalan secara asinkron, dimana:

1. Miner melatih model secara lokal
2. Model terbaik di-publish ke Hugging Face
3. Metadata model dicommit ke rantai Bittensor
4. Validator mengevaluasi model secara asinkron
5. Reward diberikan berdasarkan performa model

## Keunggulan Sistem Asinkron

- Miner tidak perlu online 24/7
- Evaluasi dilakukan terhadap model terakhir yang dipublish
- Lebih hemat resource dibanding sistem sinkron
- Fleksibel dalam proses training

## Setup Awal

1. Install dependencies:
```bash
python -m pip install -e .
```

2. Setup Hugging Face token:
```bash 
export HF_ACCESS_TOKEN="YOUR_HF_ACCESS_TOKEN"
# atau
echo "HF_ACCESS_TOKEN=YOUR_HF_ACCESS_TOKEN" > .env
```

3. Register ke subnet:
```bash
btcli subnet register --subnet 29 --wallet.name miner --wallet.hotkey default
```

4. Jalankan miner:
```bash
python neurons/miner.py \
    --wallet.name miner \
    --wallet.hotkey default \
    --logging.debug
```

## Tips Optimasi

- Gunakan GPU dengan VRAM minimal 24GB
- Pastikan disk space mencukupi (min. 30GB)
- Monitor performa model melalui wandb
- Perhatikan parameter training sesuai kompetisi aktif
