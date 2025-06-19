# Projekt zaliczeniowy z przedmiotu Deep Learning

W tym repozytorium znajduje się realizacja projektu zaliczeniowego na temat klasyfikacji obrazów z wykorzystaniem sieci neuronowych. Do treningu i ewaluacji wykorzystano zbiór CIFAR-10.

https://www.cs.toronto.edu/~kriz/cifar.html

---

## Spis treści

- [Opis projektu](#opis-projektu)  
- [Struktura repozytorium](#struktura-repozytorium)  
- [Notebooki](#notebooki)  
- [Modele i wagi](#modele-i-wagi)  
- [Wyniki i wizualizacje](#wyniki-i-wizualizacje)  
- [Źródła](#źródła)  

---

## Opis projektu

Celem projektu jest porównanie kilku architektur sieci konwolucyjnych w zadaniu klasyfikacji obrazów z popularnego zbioru **CIFAR-10**. Oceniamy między innymi:

- Prosty ConvNet  
- VGG-like  
- ResNet  
- AllCNN

---

## Struktura repozytorium

PROJEKT_ZALICZENIOWY/
├── data_exploration.ipynb # Notebook testowy – nie wykorzystany w finalnej wersji
├── model_training.ipynb # Notebook do trenowania wszystkich modeli
├── model_evaluation.ipynb # Notebook do porównania i wizualizacji wyników
├── model_vgg.bson # Wagi wytrenowanego modelu VGG-like
├── model_resNet.bson # Wagi wytrenowanego modelu ResNet
├── model_allcnn.bson # Wagi wytrenowanego modelu All-CNN
├── model_small_convnet.bson # Wagi wytrenowanego małego ConvNetu
├── plots/ # Wykresy i tabele wygenerowane w trakcie analizy
│ └── …
└── sources/ # Materiały źródłowe (PDF, artykuły)

---

## Notebooki

- **`model_training.ipynb`**  
  Zawiera kod do definicji architektur, przygotowania danych, treningu sieci oraz zapisu wag do plików `.bson`.  

- **`model_evaluation.ipynb`**  
  Analiza porównawcza wytrenowanych modeli: wczytywanie wag, ewaluacja na zbiorze testowym, tworzenie wykresów (macierze klasyfikacji, miary accuracy itp.).  

- **`data_exploration.ipynb`**  
  Eksperymentalny notebook służący do wstępnej eksploracji zbioru CIFAR-10 (wizualizacje, rozkład klas), **nie jest** wykorzystywany w finalnej prezentacji wyników.

---

## Modele i wagi

Pliki **`.bson`** zawierają zapis wag sieci po treningu. Dzięki nim można w łatwy sposób:

1. Wczytać wybrany model.  
2. Przeprowadzić szybką ewaluację lub dalsze eksperymenty (np. fine-tuning).

---

## Wyniki i wizualizacje

W folderze **`plots/`** znajdują się:

- Porównanie skuteczności poszczególnych architektur  
- Macierze klasyfikacji
- Przykładowe klasyfikacje obrazków
- Top 5 najczęstszych błędów w klasyfikacji

---

## Źródła

W folderze **`sources/`** umieszczono materiały, z których korzystano podczas realizacji projektu, m.in.:
