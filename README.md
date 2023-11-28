# DataScienceExamples

## Week 1
### Exercise 1:
Write a function that receives a list as parameter and return how many elements it has; if it doesn't have any element return an error.

### Solution 1:
def listfunc(list):
    if(len(list)>0):
        uzunluk = len(list)
        return uzunluk
    else:
        return "HATA: Liste boş girilmiştir, lütfen listeyi boş bırakmayınız."
    
mesaj = list(input("Lütfen bir liste giriniz: "))
listfunc(mesaj)

### Solution 2: 
def listefonk(liste):
    if(len(liste)<=0):
        raise ValueError("HATA: Liste boş olmamalı.")
    
    liste_uzunluk = len(liste)
    return liste_uzunluk
        
liste_mesaj = list(input("Lütfen bir liste giriniz: "))
listefonk(liste_mesaj)

## Week 2
### Exercise 2:
Write a function that receives a string as parameter and return the number of each character in it.

### Solution 1:
def kac_tane_index(string_parametresi):
    items_sayac = {} #bu bir dictionarydir
    for item in string_parametresi:
            if item in items_sayac:
                items_sayac[item] +=1
            else:
                items_sayac[item] = 1
    return items_sayac

string_mesaj = "sartre asathe"
kac_tane_index(string_mesaj)

### Solution 2:
def find_string_index(string_parameter):
    ogeler = [char for char in string_parameter]
    istenen_index = int(input("Lütfen istediğiniz indexi giriniz: "))
    print(ogeler[istenen_index])

mesaj = "melsa sağın"
find_string_index(mesaj)