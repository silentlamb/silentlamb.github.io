Title: Pirate Wars
Date: 2009-02-03 14:20:32
Slug: pirate-wars

<p>Wpis ten ma zapoczątkować serię artykułów z kategorii "Game Design" - czyli pomysły na (mikro)gry.</p>

<div class="image" style="width: 519px;"><img src="http://img.photobucket.com/albums/v202/Vall/blog/pirates.png" title="Pirates, stara i niezapomniana gra." alt="Pirates, screenshot" width="509" height="400" /></div>

<p>Niedawno zostałem poczęstowany <a href="http://www.youtube.com/watch?v=H0QfVDebLFg&amp;fmt=18">czołówką z programu "Morze"</a>. Utwór z niej, The Pirates &amp; Mike Brady - Victory jest genialny. Od razu sprawił, że dzięki UAE włączyłem starą grę Pirates, przy której trochę życia mi minęło. Programistyczne podejście do wszystkiego nie mogło oczywiście nie zadziałać; od razu zacząłem zastanawiać się jak jeszcze wykorzystać motyw tej gry.</p>

<h3>Pirate Wars</h3>

<p>Czemu nie napisać wersji gry dla wielu graczy? To była pierwsza myśl, która pojawiła się w mojej głowie. Głównym celem gry jest rozrywka w grupie (nie)znajomych. Dostajemy sparametryzowany, losowo wygenerowany akwen oraz łajbę z załogą w której przypadkowy pijak znudzony uczciwym życiem stanowi jej główny trzon. Pirate Wars ma udostępnić kilka trybów gry. Nie jest to nic odkrywczego - <strong>Free for All</strong>, gdzie chwała przypada tylko najlepszemu, <strong>Team Deathmatch</strong>, gdzie dwie i więcej flot za pomocą swych dział wytwarzają ogromne ilości dB, co raczej nie podoba się okolicznym mieszkańcom schowanym już zapewne w najgłębszych czeluściach swoich piwnic. Jest też <strong>Capture the Flag</strong>, oraz tryb <strong>Domination</strong>, w którym chwałę zgarnia ten, kto najdłużej jest w stanie kontrolować pewien punkt strategiczny.</p>

<p>Gra ma dostarczyć dużo rozrywki, ale nie być przy tym symulatorem okrętu - dlatego realizm został zepchnięty na dalsze miejsca. Nie jest jednak bez znaczenia. Każdy ze statków posiada jakiś niewielki martwy kąt, który powoduje, że pod wiatr, choćby nie wiem ile piwa wypić, nie da rady płynąć. Z wiatrem płynie się również szybciej niż pod wiatr (ale i przelatujący na drugą burtę bom potrafi zgarnąć niezłe żniwo zagapionych marynarzy. W pierwowzorze - Pirates - można dokonać abordażu na statek przeciwnika. Tutaj takiej możliwości nie ma. Skomplikowałoby to za bardzo rozgrywkę. Wszak sensem tej gry, obok 42, są bitwy morskie.</p>

<p>Kolejnym elementem obok pływania (bo ile można?) są właśnie bitwy. Po naładowaniu dział wystarczy nakierować mychą na pole, w które polecą armatnie kule, a następnie Pewnym Ustalonym Klawiszem zrobić PUK. Kuku. Zatopić, zerżnąć, spalić, zabić.</p>

<div class="image" style="width: 515px"><img src="http://img.photobucket.com/albums/v202/Vall/blog/walka.png" title="Tryb celowania w Pirate Wars na przykładzie grafiki z Pirates" alt="Pirate Wars, walka" width="505" height="254"/></div>

<p>Zatem jak już wspomniałem, zanim wydamy komendę do wystrzału należy przekazać załodze gdzie i w jaki sposób mają wycelować lufy swoich wypolerowanych nie jeden raz przez niejedną rękę (a czasem i usta) luf armatnich. Odbywa się to w ten sposób, że ustawiamy pewnym klawiszem tryb strzału (o tym za chwilę), następnie trzymając lewą mychę rysujemy okrąg, a gdy puścimy cel zostanie zatwierdzony. Po pewnej chwili (załoga musi mieć czas na ustawienia) naciskamy PUK i kule lecą tam gdzie chcemy. Im większy promień okręgu, tym większe pole rażenia kul, ale i mniejsza siła na Pewną Jednostkę Powierzchni. Możemy zatem wybrać czy chcemy uderzyć raz, a porządnie, czy może masować okręt wroga naszymi, hm, kulkami. Tryb strzału to rozkład kul na zaznaczonej powierzchni. Domyślnie jest stały - w każdym miejscu prawdopodobieństwo wylądowania pojedynczej kuli jest takie samo. Możemy jednak chcieć, aby prawa/lewa/górna/dolna część tego pola była "bardziej", niż pozostałe.</p>

<p>Ze względu na brak abordażu w grze dostępny jest również inny rodzaj ataku: strzał z broni palnej. Ma to na celu atak bezpośrednio na załogę przeciwnika. Im mniej ludzi na statku, tym dłużej trwa ładowanie dział, mniejsza jest siła strzału z tejże broni, czy wolniej trwają drobne naprawy statku.</p>

<div class="image" style="width: 284px"><img src="http://img.photobucket.com/albums/v202/Vall/blog/wiatr2.png" alt="Chmury napędowe" title="Chmury jako jednostki wiatru" width="284" height="251"/></div>

<p>Tak jak ludzi napędza rum, tak statki poruszają się dzięki istnieniu wiatru. W grze źródłem wiatru są chmury. W silniku gry zawarty jest symulator mikroklimatu. Chmury oddziałują nie tylko na zdolność poruszania się okrętów, ale także i siebie. Dwie chmury płynące prawie równolegle mogą się połączyć tworząc jedną, silną chmurę. Gdy jedna z nich natomiast biegnie prostopadle i nastąpi kolizja - tworzy się chmura burzowa, w której okolicach lepiej być się nie powinno (utrudnione sterowanie, brak możliwości oddania strzału). Z tego powodu kapitan musi cały czas widzieć co się dzieje wokół, gdyż warunki pogodowe są bardzo zmienne.</p>

<div class="image" style="width: 225px;"><img src="http://img.photobucket.com/albums/v202/Vall/blog/wiatr.png" alt="Zrodlo wiatru" title="Budowa chmury" width="225" height="225" /></div>

<p>Sama chmura obejmuje swym zasięgiem pewną powierzchnię. Posiada jakąś prędkość (co logiczne: im mocniej wieje, tym szybciej płyniemy) oraz kierunek uprzywilejowany, dla którego siła wiatru będzie największa.</p>

<p>Gra ma zawierać też niewielkie elementy humorystyczne. Gdy okręt próbuje zmierzyć się oko w oko, dziobem w dziób z nieruchomą przeszkodą nieorganiczną jaką jest wystający ponad taflę wody swym ułamkiem powierzchni kamień, jeden z członków załogi zostaje wystrzelony jak z procy przez połowę ekranu by tam utonąć (lub rozbić się na lądzie). Jeśli podczas lotu trafi na chmurkę następuje zderzenie i z chmury spada... muminek. Tego typu sytuacji w grze ma być wiele.</p>

<p>Na zakończenie tylko dodam, że screeny pochodzą z gry Pirates. Nie rysowałem własnej wizji, ponieważ marny ze mnie grafik.</p>
