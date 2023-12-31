
# PAP-FOI-docs

## Zahtjevi
- Python 3.10
- Jupyter Notebook
- Pip
- Git

## Postavljanje projekta

### Kloniranje repozitorija
```bash
git clone [URL repozitorija]
```

### Kreiranje virtualnog okruženja
```bash
cd PAP-FOI-docs
python3 -m venv env
```

### Aktivacija virtualnog okruženja
```bash
source env/bin/activate
```

### Deaktivacija virtualnog okruženja
```bash
deactivate
```

### Instaliranje potrebnih modula
```bash
pip3 install -r requirements.txt
```

## Postavljanje Tesseract OCR-a

### Ažuriranje paket menadžera
```bash
sudo apt update
```

### Instalacija Tesseract OCR-a
```bash
sudo apt install tesseract-ocr
```

### Instalacija hrvatskog jezičnog paketa za Tesseract
```bash
sudo apt-get install tesseract-ocr-hrv
```

### Dodavanje Tesseract-a u path
```bash
export PATH=$PATH:/putanja/do/tesseract
```
