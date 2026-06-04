# Eksperimen_SML_Maheza

Project machine learning untuk analisis sentimen kandidat presiden Indonesia 2024 menggunakan data Twitter.

## Struktur Project

```
Eksperimen_SML_Maheza
├── dataset_raw
│   ├── Anies Baswedan.csv        # Dataset mentah tweet Anies Baswedan
│   ├── Ganjar Pranowo.csv        # Dataset mentah tweet Ganjar Pranowo
│   └── Prabowo Subianto.csv      # Dataset mentah tweet Prabowo Subianto
└── preprocessing
    ├── Eksperimen_Maheza.ipynb   # Notebook eksplorasi & preprocessing
    └── dataset_preprocessing.csv # Dataset hasil preprocessing
```

## Deskripsi Dataset

Dataset berisi tweet berbahasa Inggris yang telah diterjemahkan, berkaitan dengan tiga kandidat presiden Indonesia pada Pemilu 2024:
- **Anies Baswedan**
- **Ganjar Pranowo**
- **Prabowo Subianto**

Sumber: [Indonesia Presidential Candidates Dataset 2024](https://www.kaggle.com/datasets/jocelyndumlao/indonesia-presidential-candidates-dataset-2024) (Kaggle)

| Kolom | Keterangan |
|-------|------------|
| `Text` | Teks tweet yang sudah dibersihkan |
| `label` | Sentimen: `Positive` / `Negative` |
| `Candidate` | Nama kandidat yang dirujuk |

Total data: **30.000 baris** (10.000 per kandidat)

## Setup

### 1. Clone Repository

```bash
git clone https://github.com/firzadillah0192-source/Eksperimen_SML_Maheza.git
cd Eksperimen_SML_Maheza
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk
```

### 3. Jalankan Notebook

Buka file notebook di folder `preprocessing/`:

```bash
jupyter notebook preprocessing/Eksperimen_Maheza.ipynb
```

## Alur Preprocessing

1. **Load Dataset** — membaca 3 file CSV raw dan menggabungkannya
2. **EDA** — eksplorasi distribusi label, kandidat, dan panjang teks
3. **Text Cleaning** — menghapus karakter spesial, stopwords, dan normalisasi teks
4. **Labeling** — konversi label `Positive`/`Negative` ke `1`/`0`
5. **Export** — menyimpan hasil ke `dataset_preprocessing.csv`

## Author

**Maheza Firzadillah**  
firzadillah0192@gmail.com
