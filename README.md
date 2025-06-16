# movie_recommendation 

## System rekomendacji filmów

Projekt implementuje dwa systemy rekomendacji filmów:

- **NeuMF (Neural Matrix Factorization)** – połączenie liniowego GMF (Generalized Matrix Factorization) oraz nieliniowego MLP (Multilayer Perceptron).
- **kNN** – rekomendacje bazujące na podobieństwie użytkowników.

W projekcie wykorzystano dane **MovieLens 1M** (oceny użytkowników i tytuły filmów).

---

## NeuMF 

### Funkcjonalności:

-  Wczytanie i przetwarzanie danych (`ratings.dat`, `movies.dat`)
-  Mapowanie `userId`, `movieId` na embeddingi
-  Trenowanie modelu NeuMF (z embeddingiem gatunku)
-  Generowanie rekomendacji filmów
-  Obliczenie RMSE (błąd predykcji)

---

## Pliki projektu 

- `train_model.ipynb` – notebook treningowy NeuMF
- `recommend_movies.ipynb` – notebook do generowania rekomendacji
- `best_model.h5` – wytrenowany model NeuMF
- `*.pkl` – mapowania użytkowników i filmów

---

## Instrukcja uruchomienia 

### 🔹 1. Pobranie danych

Pobierz dane [MovieLens 1M](https://grouplens.org/datasets/movielens/1m/) i wypakuj do katalogu projektu jeśli checsz korzystać z train_model lub reccomend_movies.

Potrzebne pliki:
- `ratings.dat`
- `movies.dat`

---

### 🔹 2. Trenowanie modelu (`train_model.ipynb`):

Zainstaluj wymagania:
```bash
pip install -r requirements.txt
```

### 🔹 3. Korzystanie z modelu (reccomend_movies.ipynb):
Zainstaluj wymagania:
```bash
pip install -r requirements_predict.txt
```
- dodaj pliki h5 i pkl z repozytorium albo wytrenowane przez Ciebie

### 🔹 4. Jeśli chcesz dodać swoje dane personalne:
Dodaj je do pliku ratings.dot a nastpenie wytrenuj model


## kNN 

### Funkcjonalności:

- Wczytywanie i przetwarzanie danych (`ratings.dat`, `movies.dat`)
- Mapowanie użytkowników i filmów do macierzy ocen
- Obliczanie podobieństwa między użytkownikami (Cosine Similarity)
- Generowanie rekomendacji filmów na podstawie ocen użytkowników podobnych
- Obliczanie błędu predykcji (RMSE)

---

## Pliki projektu

- `knn_recommendation.ipynb` – notebook generujący rekomendacje kNN
- Pliki danych `ratings.dat` i `movies.dat`

---

## Instrukcja uruchomienia 

### 🔹 1. Pobranie danych

Pobierz dane [MovieLens 1M](https://grouplens.org/datasets/movielens/1m/) i wypakuj do katalogu projektu.

Potrzebne pliki:
- `ratings.dat`
- `movies.dat`

---

### 🔹 2. Generowanie rekomendacji (knn.ipynb)

Zainstaluj wymagane biblioteki:
```bash
pip install -r requirements_knn.txt
```

### 🔹 3. Jeśli chcesz dodać swoje dane personalne:
Dodaj je do pliku ratings.dot a nastpenie wytrenuj model
