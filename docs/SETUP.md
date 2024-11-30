# Setup Detail Subnet 29

## Persiapan Environment

1. **Python Environment**
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# atau
.\venv\Scripts\activate  # Windows
```

2. **Dependencies**
```bash
pip install torch torchvision torchaudio
pip install transformers==4.44.0
pip install bittensor
pip install -e .
```

3. **Hugging Face Setup**
```bash
huggingface-cli login
# atau
export HF_ACCESS_TOKEN="YOUR_TOKEN"
```

## Konfigurasi Wallet

1. **Buat Wallet Baru**
```bash
btcli wallet new --wallet.name miner
```

2. **Generate Hotkey**
```bash
btcli wallet new_hotkey --wallet.name miner --wallet.hotkey default
```

3. **Register ke Subnet**
```bash
btcli subnet register --subnet 29 --wallet.name miner --wallet.hotkey default
```

## Verifikasi Setup

1. **Cek Registrasi**
```bash
btcli subnet list --wallet.name miner
```

2. **Test Koneksi**
```bash
python neurons/miner.py --wallet.name miner --wallet.hotkey default --logging.debug --offline
```

## Monitoring

1. **Setup Wandb**
```bash
wandb login
```

2. **Cek Storage**
```bash
df -h /path/to/model/storage
```

3. **Monitor GPU**
```bash
nvidia-smi -l 1
```
