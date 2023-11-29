# grupaA

# wprowadzenie danych

library(readr) agencja_nieruchomosci \<- read_csv("agencja_nieruchomosci-20231118T160815Z-001/agencja_nieruchomosci/agencja_nieruchomosci.csv") View(agencja_nieruchomosci)

## zmiana stop kwadratowych na metry kwadratowe

agencja_nieruchomosci$area_m2 <- agencja_nieruchomosci$area * 0.092903

#zaokraglenie do dwoch miejsc po przecinku
agencja_nieruchomosci$area_m2 <- round(agencja_nieruchomosci$area_m2, 2)

## Dodawanie kolumny z ceną za metr kwadratowy
agencja_nieruchomosci$Price_per_m2 <- agencja_nieruchomosci$price / agencja_nieruchomosci$area_m2

# Zaokrąglanie wartości w kolumnie "Price_per_m2" do dwóch miejsc po przecinku
agencja_nieruchomosci$Price_per_m2 <- round(agencja_nieruchomosci$Price_per_m2, 2)

#zmiana na test




# Wyświetlenie zmodyfikowanych danych

View(agencja_nieruchomosci)

##--------------------

## Wprowadzenie

## Czyszczenie danych

### Brakujace obserwacje

### Obserwacje odstające

### Walidacja danych
