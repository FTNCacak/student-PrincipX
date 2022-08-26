<img src="Slike/FTNCacak-Logo.png" alt="FTN-logo" width="25"/> <span style="color:#a00000;font-size:24pt">FTN Čačak</span>

### Softversko inženjerstvo 2021/2022.
___

## Design Patterns in C# – Creational Patterns

### Dejan Blagojević 222/2019
### Aleksa Spajić 213/2015

______

### Uvod

#### C# je objektno-orijentisani programski jezik opšte namene. Razvijen je 2000. godine, od strane Microsoft-a. Na čelu tima koji se bavio razvojem C#-a bio je Anders Hejlsberg.

#### Januara 1999. godine, Anders Hejlsberg osnovao je tim za izradu novog programskog jezika koji se u početku zvao COOL (C-like Object Oriented Language), idejno zamišljen kao jezik C, ali objektno orijentisan.

#### Microsoft je hteo da sačuva prvobitno ime, ali je zbog zaštitnog znaka odustao. U julu 2000. godine, okruženje .NET predstavljeno je na Konferenciji profesionalnih programera (Professional Developers Conference), jezik je preimenovan u C#, a biblioteke i ASP.NET prenesene u C#.

#### C# predstavlja naslednika C i C++ jezika, dobio je ime šarp, inspirisano muzičkom notacijom i znači da se napisana nota izvodi za pola koraka više. Fajlovi pisani u ovom jeziku imaju ekstenziju `.cs`.

#### Hejlsberg je glavni dizajner C#-a u Microsoft-u, a ranije je radio i na dizajnu Turbo Pascal-a, Delphi-a i Visual J++. U mnogim intervjuima i tehničkim dokumentima on je naveo da su upravo nedostaci drugih programskih jezika doveli do stvaranja C#.

#### C# se danas koristi širom sveta za razvijanje raznih tipova programa i aplikacija.

#### Iako je izuzetno prilagodljiv jezik, postoje tri oblasti u kojima se obično primenjuje:

##### 1. Razvijanje web aplikacija - Možemo razvijati dinamičke web-sajtove i web-aplikacije koristeći .NET platformu ili neke od drugih platformi otvorenog koda (open-source)

##### 2. Razvijanje Windows aplikacija - Programeri mogu da računaju na podršku zajednice i dokumentaciju za razvoj aplikacija i programa koji su specifični za arhitekturu Microsoft platforme.

##### 3. Razvijanje video igara - Veliki broj game engine-a koji se koriste za razvoj video igara podržava C#. Jedan od njih je i Unity, jedan od najpopularnijih game engine-a uopšte.

<p align="center">
  <img src="Slike/csharp.png" width="300"/>
</p>

______

### Design Patterns
#### U svetu razvoja softvera često se suočavamo sa istim problemima iznova i iznova. Takođe, nije neuobičajeno da se ovi problemi pojave kada je kod već završen. Ovo se može izbeći jednostavnom upotrebom Design pattern-a (obrazaca).

#### 'Gang of Four' design pattern-i je kolekcija od 23 dizajn obrasca iz knjige "Design Patterns: Elements of Reusable Object-Oriented Software".
#### Ova knjiga je prvi put objavljena 1994. godine i jedna je od najpopularnijih knjiga za učenje design pattern-a. Autori knjige su Erich Gamma, Richard Helm, Ralph Johnson i John Vlissides. Knjiga je dobila nadimak 'Gang of Four Design Patterns' zbog četiri autora. Štaviše, dobili su još kraće ime kao 'GoF Design Patterns'.


<p align="center">
  <img src="Slike/bookImage.png" width="300"/>
</p>

#### Dizajn obrasci predstavljaju rešenje visokog kvaliteta za višekratnu upotrebu za dati zahtev, zadatak ili problem koji se ponavlja.

#### Obrasci se odnose na dizajn i interakciju objekata, kao i na obezbedjivanje komunikacijske platforme koja se tiče elegantnih rešenja koja se mogu ponovo koristiti za uobičajene izazove programiranja.

#### Ako ste usred projekta i razmišljate u sebi, kako niko nikada nije prošao kroz ovo ranije - velike su šanse da neko zapravo jeste.

#### Dizajn obrasci su dokumentovana verzija svih tih stvari. Razlog zašto je ovo toliko dragoceno je zato što čini aplikaciju irelevantnom, a informacije su prenosive.

#### Dizajn obrasci imaju 2 glavne prednosti:

#### 1. Pružaju nam način da rešimo probleme u vezi sa razvojem softvera koristeći proverena rešenja

##### - Koristeći proverena rešenja ne moramo da problem rešavamo samostalno, kreirajući naše sopstveno rešenje, čime utičemo na uštedu vremena.

#### 2. Dizajn obrasci čine komunikaciju između dizajnera efikasnijom

##### - Poznajući dizajn obrasce činimo komunikaciju tokom izrade projekta dosta efikasnijom, jer svi poznaju ideje korišćene za specifične dizajn obrasce, nasuprot idejama rešenja problema koje smo samostalno kreirali.

#### Dizajn obrasci se dele u 3 grupe:

##### 1. Creational patterns (kreacioni)

##### 2. Structural patterns (strukturalni)

##### 3. Behavioral patterns (bihevioralni)


______

### Creational Patterns

#### Kreacioni dizajn obrasci se bave mehanizmima kreiranja objekata. Fokus je na tome kako se objekti kreiraju i koriste u aplikaciji.

#### Kreacioni pattern-i se sastoje od dve dominantne ideje. Jedna je enkapsulacija znanja o tome koje konkretne klase sistem koristi, a druga predstavlja skrivanje toga kako se instance ovih konkretnih klasa kreiraju i kombinuju.

#### Kreacioni pattern-i su dalje kategorisani u pattern-e za kreiranje objekata i pattern-e za kreiranje klasa, gde se pattern-i za kreiranje objekata bave kreiranjem objekata, a pattern-i za kreiranje klasa bave instanciranjem klase.

#### Detaljnije, pattern-i za kreiranje objekata odlažu deo kreiranja svog objekta na drugi objekat, dok pattern-i za kreiranje klasa odlažu kreiranje svog objekta na podklase.

#### Kreacioni pattern-i se dele u pet kategorija

##### 1. Factory Method - Kreira instancu nekoliko izvedenih klasa

##### 2. Abstract Factory - Kreira instancu nekoliko porodica klasa

##### 3. Builder - Odvaja konstrukciju objekta od njegovog predstavljanja

##### 4. Prototype - Potpuno inicijalizovana instanca za kopiranje ili kloniranje

##### 5. Singleton - Klasa kod koje može postojati samo jedna instanca

______

### Factory Method

#### Factory Method je kreacioni dizajn pattern koji rešava problem kreiranja objekata bez specificiranja njihovih konkretnih klasa.

#### Factory Method definiše metodu koja treba da se koristi za kreiranje objekata umesto direktnog poziva konstruktora (`new` operator). Podklase mogu zameniti ovaj metod da bi promenile klasu objekata koji će biti kreirani.

#### KORIŠĆENJE: Factory Method pattern se veoma često koristi u C# kodu. Veoma je koristan u slučajevima kada je potrebno obezbediti visok nivo fleksibilnosti našeg koda.

#### PREPOZNAVANJE: Factory Method se može prepoznati po metodama kreiranja koje konstruišu objekte iz konkretnih klasa. Dok se konkretne klase koriste tokom kreiranja objekata, tip vraćanja factory metoda se obično deklariše ili kao apstraktna klasa ili kao interfejs.
______

### Abstract Factory
#### Tekst

______

### Builder
#### Tekst

______

### Prototype
#### Tekst

______

### Singleton
#### Tekst

______


### Reference

1. https://www.c-sharpcorner.com/UploadFile/nipuntomar/creational-design-pattern-for-net/

2. https://www.wikipedia.com

3. https://www.digitalocean.com/community/tutorials/gangs-of-four-gof-design-patterns

4. https://insight.averna.com/en/resources/blog/how-can-design-patterns-solve-all-your-problems

5. https://stackify.com/what-is-c-used-for/