# Zadanie 3.1

## Konwencje nazewnicze:

### Ogólne reguły

> Nazwy zasobów piszemy z małych liter i po angielsku. Nazwa powinna być krótka ale opisowa. Dla każdego projektu budowanego w oparciu o Microsoft Azure, należy określić krótki prefiks, który będzie rozpoczynał nazwę każdego definiowanego zasobu w Microsoft Azure.

Prefiks może się składać z cyfr i liter a jego minimalna długość to 2 a maksymalna 3.

> Na potrzeby tego dokumentu przyjmujemy prefiks: **pd3** dla projektu Praca Domowa nr. 3.

Stosowane skróty dla regionów:
- North Europe - ne
- West Europe - we
- France Central - fc
- France South - fs
- UK West - uw
- UK South - us
- Germany Central - gc
- Germany Northeast - gne
- Germany North - gn
- Germany West Central - gwc
- Switzerland North - sn
- Switzerland West - sw
- Norway East - nye
- Norway West - nyw

Stosowane skróty dla środowisk:
- prod - środowisko produkcyjne
- dev - środowisko deweloperskie
- qa - środowisko testowe


### Zasady dla poszczególnych zasobów:


**Grupa zasobów**

`<prefix>-rg-<region>-<environment>-<nazwa>`
- długość pola nazwa: 3-60 znaków
- dozwolone znaki: litery, cyfry, podkreślenie, myślnik
- nazwa powinna być krótka i odnosić się do przeznaczenia danej grupy zasobów


**Maszyna wirtualna**

`<prefix>-vm<number>-[region]-<nazwa>`
- długość maksymalna: 15 (Windows), 17 (Linux)
- długość pola nazwa: 2-3 (Windows), 2-5 (Linux)
- pole number może przyjmować wartości od 1 do 9
- region:wymagane w przypadku, gdy zasób należy do innego regionu niż grupa robocza do którego został przypisany
- dozwolone znaki: litery, cyfry, podkreślenie, myślnik
- nazwa powinna być krótka i odnosić się do przeznaczenia/roli danej maszyny wirtualnej


**Wirtualne sieci**

`<prefix>-vnet-[region]-<nazwa>`
- długość pola nazwa: 2-50 
- region:wymagane w przypadku, gdy zasób należy do innego regionu niż grupa - - - robocza do którego został przypisany
- dozwolone znaki: litery, cyfry, podkreślenie, myślnik
- nazwa powinna być krótka i odnosić się do przeznaczenia danej sieci wirtualnej


**Podsieci**

`<nazwa wirtualnej sieci>-subnet<number>-name`
- długość pola nazwa: 2-7
- pole number może przyjmować wartości od 1 do 99, przy czym wartości poniżej 10 - zapisywane muszą być z poprzedzającym zerem, np. 01
- dozwolone znaki: litery, cyfry, podkreślenie, myślnik
nazwa powinna być krótka i odnosić się do przeznaczenia danej podsieci


**Karta sieciowa**

`<nazwa wirtualnej maszyny>-nic<number>`
- maksymalna długość: 80
- pole number może przyjmować wartości od 1 do 9


**Sieciowa grupa zabezpieczeń**

`<prefix>-nsg-<nazwa>`
- długość pola nazwa: 2-70
- dozwolone znaki: litery, cyfry, podkreślenie, myślnik
- nazwa powinna być krótka i odnosić się do przeznaczenia grupy zabezpieczeń


**Dysk**

`<nazwa wirtualnej maszyny>-osdisk`
- maksymalna długość: 24


**Konto składowania danych**

`<prefix>sa<globalnie unikalna nazwa>`
- maksymalna długość: 24
- należy użyć funkcji do wygenerowania unikalnej nazwy


**Publiczny adres ip**

`<nazwa>-pip`
- długość pola nazwa: 2-40
- nazwa powinna zawierać nazwę maszyny wirtualnej lub innego zasobu/usługi do którego zostanie przypisany publiczny adres ip

