Title: ObrASCII
Date: 2009-05-27 19:05:08
Slug: obrascii

<h3>Jakieś znaczki, o co tu właściwie chodzi?</h3>

<p>Rysunki ze znaczków które można tu znaleźć zwane są ASCII-artami. Nie każdy obrazek można tym mianem określić. Czym więc są te ASCII-arty (zwane dalej w skrócie AA)?</p>

<p>ASCII to pewien standard przyporządkujący znakom wartości liczbowe, zrozumiałe dla komputera. I tak np. litera 'a' widziana jest przez komputer (który rozumie tylko liczby) jako wartość 97. Przyporządkowania te zebrane są w tablicy zwanej tablicą ASCII. Nas interesuje podstawowa tablica ASCII, a dokładniej część tych znaków, które są przez nas widzialne (z wyjątkiem spacji i znaku nowej linii). Listę tych znaków można znaleźć na wikipedii <a href="http://en.wikipedia.org/wiki/ASCII#ASCII_printable_characters">w tabelce pod artykułem o ASCII</a>.</p>

<p>ASCII-Arty są zatem rysunkami złożonymi tylko z takich znaków. W tej nazwie ważny jest jeszcze drugi człon: <strong>art</strong>. W internecie znaleźć można wiele programów czy skryptów, stron, które nakarmione plikiem graficznym wygenerują nam obrazek złożony tylko ze znaków ASCII. Ten mechaniczny, wygenerowany, brzydki stwór nie ma jednak za wiele wspólnego ze sztuką, dlatego tak powstałych obrazków ASCII-artem nazwać nie można, a nawet <strong>nie wolno</strong>!</p>
    
<p>Kolejną ważną rzeczą jest zachowanie <em>czystej formy</em>. AA rozkwitło głównie dzięki grupom dyskusyjnym. To tam ludzie dyskutując tworzyli swoje dzieła. Ważny był czysty tekst. Żadnego kolorowania, pogrubiania, podkreślania, zmiany rozmiaru fontów, czy ich typu. Powstały obiekt na rysunku powinien być tak samo rozróżnialny z pokolorowaniem jak i bez! Piszę o tym dlatego, gdyż (znów) w internecie można trafić na wiele galerii, na których ludzie zamieścili bardzo kolorowe rysunki, które po wyłączeniu kolorów są... Masą tekstu bez żadnego większego ładu, składu, nie przedstawiają tego co powinny.</p>

<p>AA tworzy się w edytorach tekstu. Wystarczy zwykły notatnik, vim czy emacs i można rysować. Prawie. Aby poprawnie oglądać takie rysunki, potrzebne jest ustawienie w edytorze odpowiedniego fontu. Musi on się charakteryzować tym, że po napisaniu dwóch wierszy za pomocą dwóch różnych liter, wiersze te zaczynają i kończą się w tym samym miejscu.</p>

<pre>
                       WWWWWWWWWWWWWWWWWWWWWWWWWWWWWW
                       ..............................
</pre>

<p>W podanym wyżej przykładzie obie linie - ze znaków W oraz kropki powinny mieć tą samą długość. Fonty takie najczęściej posiadają w swoich nazwach słowo mono, monospace, fixed, terminal, czy console (choć są i wyjątki). Do najpopularniejszych należą Courier New, Lucida Console, Terminal oraz monospace. Na swoim blogu większość artów (jeśli nie wszystkie) wyświetlane są za pomocą Lucida Console. Jako ciekawostkę dodam, że dwa najpopularniejsze fonty: Courier New i Lucida Console mają za sobą rzeszę (jeśli można to tak nazwać) fanów, co przekładało się na wiele dyskusji, kłótni i wojen na temat tego, który font jest najlepszy. Cała ta wojna jest moim zdaniem zupełnie bez senu, ponieważ nie ma wątpliwości, że najładniejszym fontem jest Lucida Console.</p>
    
<p>Każdy font posiada swoje własne smaczki, odróżniajace go od innych. Lucida Console na przykład posiada szerokie, rozlazłe litery i bardzo niskie przerwy między kolejnymi liniami. Courier New przy tym jest bardzo chudy i drobny, odstępy międzyliniowe są spore. Fonty różnią się między sobą też położeniem niektórych znaków. Najbardziej problematycznymi znakami są znaki takie jak: wielka litera I (jak Iwona), znak tyldy ~, daszka (dash) ^ oraz gwiazdki *. W różnych fontach znajdują się na różnych wysokościach – począwszy od bardzo wysokiej do nawet środka znaku; często różnią się też kształtem (np. wielka litera I może posiadać na dole i górze szeryfy lub być gołą pionową kreską) dlatego najczęściej ASCII-artowcy starają się tych znaków unikać.</p>

<pre>
                        .---------------------.
                        | Co to znaczy ROTFL? |
                        |_  __________________|
                          |/              .--------------------------.
                                        __| Nie wiem, nigdy          |
                      _   _       _ _   `-. nie lubiłem chińszczyzny.|
                      \7_F/       \|\|    `--------------------------'
                      / oo\       |oo \
                     /_\,_@_______@_,/ \
                   ,/|`.             .'||  __
                   |\|  j-----------f  |/ |\ `\
                   `\|  |           |  | _| |  |
                     |  |           |  |(m| |=:|
                     l  |           |  j  | |=:\)
               fsc    `.|_________c_|.'    \|_||
                                  `----....---'
</pre>


<p>Wracając do tematu edytorów: AA można tworzyć w zwykłym, normalnym edytorze dostępnym praktycznie na wszystko co ma klawiaturę, jednak niektóre edytory mogą wspomóc tworzenie nieco lepiej niż inne – jeśli posiadają dodatkowe narzędzia. Pierwszym z nich jest <strong>kopiowanie blokowe</strong>. Ciężko opisać to bez pomocy graficznej, zatem niech kopiowanie blokowe wyjaśni poniższy tekst.</p>

<pre>
 (wymaga odświeżenia strony – zmiany w stylach)

 W normalnym <span class="mark">kopiowaniu zaznaczając pewien fragment tekstu zaznaczenie
 podąża od strony lewej do prawej. Tekst wyświetlany w edytorze
 jest tak naprawdę w postaci jednej długiej linii. Edytor wyświetla
 go jednak wieloliniowo, ponieważ znajdują się w nim niewidzialne
 znaki końca</span> linii. Ty też takie znaki potrafisz wytworzyć: naciskając
 enter. Te niewidzialne znaki "powrotu" i "nowej linii" mówią edytorowi,
 który wyświetla dany fragment tekstu, że w tym miejscu należy przejść
 do początku ekranu, do następnej linii.


            Wiedziałaś, że każda
            linia zakończona jest
           niewidzialnymi znakami?       Niewidzialnymi,
                                        różowymi znakami.
                                            `
               '  .--.           _           .--.
                 /  oo|         |_|         (..  )
          -------\____|---------' `----------)__(-----------------


     Kopiowanie blokowe działa nieco inaczej. Edytor
     jest tu bardziej in<span class="mark">teligetny. Tekst zapi</span>suje w pewnym
     sensie w postaci du<span class="mark">żej tablicy. Każdy wi</span>ersz tablicy
     to nowa linia, a ka<span class="mark">żdy znak w tej linii </span>umieszczony jest
     w osobnej kolumnie.<span class="mark"> Kopiując blokowo wyb</span>ieramy tylko
     niektóre kolumny, co ilustruje zaznaczony fragment.

</pre>

<p>Drugą z takich pomocnicznych opcji jest możliwość ustawienia tła pod tekstem. Dzięki temu możemy najpierw narysować coś na kartce (lub w programie graficznym), a następnie podążać za pomocą znaków po narysowanych liniach. Dzięki temu komuś, kto nie ma ogromnego talentu do grafiki, jest dużo łatwiej zachować odpowiednie proporcje. Taka technika określana jest słowem „<strong>watermark</strong>”.</p>


<p>Na dzisiaj koniec. W przygotowaniu arty o historii oraz o polskiej scenie AA.</p>
<p>Do przeczytania!</p>
