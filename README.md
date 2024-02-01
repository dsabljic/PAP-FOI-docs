# PAP-FOI-docs

## Zahtjevi
- Python 3.10
- Pip
- Git

## Postavljanje projekta za prikupljanje podataka sa [FOI stranice](https://www.foi.unizg.hr/hr/dokumenti)

### Kloniranje repozitorija
```bash
git clone https://github.com/dsabljic/PAP-FOI-docs.git
cd PAP-FOI-docs
```

### Kreiranje virtualnog okruženja
```bash
python3 -m venv env
```

### Aktivacija virtualnog okruženja
```bash
source env/bin/activate
```

### Instalacija Jupyter Notebook-a
```bash
pip3 install notebook
```

### Deaktivacija virtualnog okruženja
```bash
deactivate
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

Nakon toga može se pokrenuti Main.ipynb *notebook* kako bi se dokumenti preuzeli lokalno

---

Priložena je i finalna csv datoteka `data.csv` te `docs.db` za brzi pristup podacima (bez *scrapinga* i ekstrakcije teksta).

Priprema za upotrebu (csv)
```python
df = pd.read_csv('./data.csv')
df['datum'] = pd.to_datetime(df['datum'])
```

Nakon toga može se odmah pokrenuti baza i nastaviti s radom.

Učitavanje podataka iz baze u DataFrame

```python
df = pd.read_sql('dokument', 'sqlite:///docs.db')
```