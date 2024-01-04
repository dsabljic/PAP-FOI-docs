# PAP-FOI-docs

## Zahtjevi
- Python 3.10
- Pip
- Git

## Postavljanje projekta

### Kloniranje repozitorija
```bash
git clone https://github.com/dsabljic/PAP-FOI-docs.git
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

---

Priložena je i finalna csv datoteka data.csv za brzi pristup podacima (bez *scrapinga* i ekstrakcije teksta).

Priprema za upotrebu
```python
df = pd.read_csv('./data.csv')
df['datum'] = pd.to_datetime(df['datum'])
```
