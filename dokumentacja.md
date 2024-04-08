# Zadanie 1

Utworzylimy projekt i namespace z interfesju sieciowego, nginxa postawiliśmy następującym poleceniem:

`kubectl create deployment -n nginx nginx --image=nginx:latest --replicas=3`

Stworzono jedynie 3 repliki, reszta podpunktów nie zozstała ruszona

# Zadanie 2

Podłączono się do maszyny i zainstalowano paczki i serwisy (z https://longhorn.io/docs/1.6.1/deploy/install/#installation-requirements):

```sh
sudo zypper install open-iscsi
sudo systemctl enable --now iscsid
```

Przy instalacji longhorna odznaczylem "Use default images"

"default storage class" byl juz zaznaczony, zmienilem jedynie replicaCount na 1

node kubernetes04 istnieje

# Zadanie 3

Dodano repozytorium https://rancher.github.io/rodeo i zainstalowano tetrisa.

# Zadanie 4

Zainstalowano.

auto-scan włączony został z dashboardu w ostatniej pozycji na karuzeli

# Zadanie 5

wszedłem w zakładkę Assets > Registers i dodano repo dockera

Najgroźniejszy jest `nvbeta/node:latest`

# Zadanie 6

Poddajemy się.

# Zadanie 7

Drogi Adrianku, żeby zobaczyć config zasobu możemy użyć następującego polecenia
    
    kubectl get <typ_zasobu> <nazwa_zasobu> -n <namespace> -o yaml
    
np.

    kubectl get deployment nginx -n nginx -o yaml
    
W rancherze możemy wybrać zasób, z kebab menu wybrać Download YAML.

# Zadanie pomiędzy 7 a 8, tzw. teoretyczne albo i 7.5

zaletą uruchamiania na domyślnych ustawieniach jest prostota uruchomienia mysql
natomiast zaletą uruchamiania na własnych ustawieniach jest duża możliwosc konfiguracji oraz bezpieczenstwo 
zalecałbym uruchomienie z własnymi ustawieniami

# Zadanie 8

Gateway w Kubernetes zarządza ruchem sieciowym w klastrze. Gateway przechwytuje ruch z internetu i przekierowywuje go do odpowiednich podów wewnątrz klastra.

# Zadanie 9

Replica Set jedynie stara się zachować wskazaną liczbę replik poda.
Deployment natomiast ułatwia aktualizacje, bo automatycznie on aktualizuje pody jeden po drugim.

# Zadanie 10

poddajemy sie

# Zadanie 11 

W Users & Authentication dodaliśmy dwóch użytkowników. Następnie zmodyfikowaliśmy config projektu aby jeden był Ownerem, a drugi miał tylko dostęp read-only.

---

# Zadanie 14

stworzyliśmy namespace w rancherze, uruchomilismy

    kubectl apply -f https://raw.githubusercontent.com/jbiniek/potyczki24/main/adrian-nginx.yaml -n adrian
    
i na tym się skończyło nasze naprawianie

---

# Zadanie 18

Zmieniono obraz z `arm64v8/hello-world` na `amd64/hello-world`



