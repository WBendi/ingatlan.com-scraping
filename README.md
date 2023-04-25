# ingatlan.com-scraping

##################### EN
For scraping the hungarian housing market.

####################  HU
Eme script a magyar ingatlanok adatait gyűjti, az összes adatot ami elérhető, rezsiköltségtől kezdve a szobák számáig. 
Kommenteltem hogy esetleg a Sys.sleep() parancs paraméterét érdemes átírni >180 másodpercre, ha a sok read parancs miatt 401 error kapunk.

6-8 óra alatt az egész budapesti ingatlanpiac adatát le tudjuk tölteni, biztos van kifinomultabb módszer beautiful-souppal vagy seleniummal, de ez gyakorlás céljából lett elkészítve.



Az alábbi probléma van még a kóddal:
(néhány oszlop adatai elcsúsznakak mert hiányosan töltötték fel a hirdetést, de ez csak 1-3%ra érvényes)
Ha hiányos  az egyik mező (mondjuk rezsiköltség mezőt üresen hagyták) akkor elcsúsznak az adatok és a következő oszlop adatai jelennek meg,
Ez egyszerűen javítható, de ez egy ilyen low-effort project.
Példa:

![image](https://user-images.githubusercontent.com/65070163/234425456-54f4b372-362b-4e19-97f4-dd2f3bb4c6cb.png)

Emiatt minimális adatranszformáció van benne, de ha nem akarunk bajlódni a szűréssel akkor csak kihagyjuk őket 
