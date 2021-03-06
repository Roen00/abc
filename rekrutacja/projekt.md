# Projekt

Jedną z najważniejszych rzeczy, jakie musisz zrobić przed przystąpieniem do procesu rekrutacyjnego jest stworzenie projektu. Będzie on twoją kartą przetargową. Będzie on dowodem na to, że znasz nie tylko teorię, podstawowe pojęcia, elementy składni języka, ale również potrafisz wykorzystać daną technologię (technologie) w praktyce. Im więcej masz projektów, własnych i współtworzonych, tym lepiej. Z drugiej strony korzystniej mieć jedną aplikację porządnie napisaną, niż kilka o miernej jakości kodu. Najważniejsze jest posiadanie przynajmniej jednego, własnego projektu, który mówi o tobie: 'to nie jest pierwsza lepsza osoba z ulicy. Autor potrafi okiełznać język, i zrobić w nim coś działającego'. W przypadku braku takowego, nasze umiejętności będą mogły zostać sprawdzone prawdopodobnie dopiero podczas rozmowy rekrutacyjnej. Posiadanie projektu zwiększa szansę na to, że rekruter odpowie na wysłane CV, i może zwiększyć twoje szanse na pozytywne przejście następnych etapów rekrutacji (np. jeśli nie pójdzie ci najlepiej z zadaniem programistycznym podczas części technicznej rozmowy o pracę).

## Jaki język, technologię wybrać?

Nie należy przesadzać z ilością języków programowania, bibliotek które będą użyte. Przede wszystkim warto użyć te języki, technologie które są wymieniane w wymaganiach w interesujących nas ofertach pracy. Brak wykorzystanej danej technologii nie zamyka możliwości złożenia CV. Istnieje taka możliwość, ponieważ niektóre technologie są dosyć podobne, i stosunkowo łatwo można się tej pożądanej nauczyć. Czasem pracodawcę może interesować przede wszystkim fakt, że umiesz programować w jakimkolwiek języku, i może on pozwolić sobie na twoją naukę innego języka już w pracy.


Przykłady języków, technologii wartych zastosowania:
- front-end: czysty JavaScript, lub wraz z JQuery. Pluginy JQuery w zależności od potrzeb. Być może warto wykorzystać framework JavaScriptowy, typu AngularJS, EmberJS. Być może przydatny będzie Bootstrap.
- baza danych: PostgreSQL, MariaDB, SQLite. Lub baza NoSQL, jeśli jej użycie jest uzasadnione: MongoDB, Redis, Cassandra.
- framework backendowy: Django, Ruby on Rails, Spring, Symfony, Laravel, Play itp.

## Jaka ma być tematyka aplikacji?

Istnieją w Internecie listy pomysłów na projekty. Można się z nimi zapoznać, aby zaczerpnąć inspiracji. Jednak najlepszym pomysłem może być wykonanie aplikacji, która rozwiąże jakiś nasz problem. Na przykład zautomatyzuje czynność, którą musieliśmy wcześniej mozolnie robić ręcznie. Dzięki temu potencjalnie będziemy mieć większą motywacją i radość z jej tworzenia, w porównaniu do realizacji jakiegoś losowo wybranego zadania. Dodatkowo, kwestia pobudek urzeczywistnienia takiego pomysłu może być poruszona przez rekrutera, a realizacja projektu na własne potrzeby powinna być lepiej odebrana.

Interesującym projektem może być aplikacja, która automatyzuje wykonywane przez nas czynności. Załóżmy, że regularnie wchodzimy na jakąś stronę, i pobieramy z niej jakąś treść, typu 10 najpopularniejszych obrazków. Możemy zautomatyzować ten proces, np. z użyciem API strony z obrazkami, jeśli ona takowe udostępnia. Możemy pobierać te obrazki, zapisać je na zewnętrznym serwerze. Dodatkowo dokładamy prosty interfejs, poprzez który możemy zobaczyć statystki pobranych obrazków, pogrupować je w katalogi, usuwać, zmieniać nazwę itp.

Inny podejściem może być zrobienie kopii jakiegoś serwisu. Nie chodzi oczywiście o bezpośrednie skopiowanie kodu, ale o stworzenie identycznej/podobnej funkcjonalności.

## Szczegóły techniczne własnego projektu

Czy wykorzystywać gotowe pluginy/biblioteki, czy napisać potrzebną funkcjonalność samemu? W pracy zawodowej generalnie zwykle wykorzystuje się gotowe "półfabrykanty". Nie warto wynajdywać koła na nowo. Prawdopodobnie będzie istniała taka biblioteka (czasem jest ich wiele), która rozwiązuje dany problem. Zwykle jest już ona starannie przetestowana; jeśli jest popularna, to sporo osób/firm ją używa, dzięki czemu obsługuje ona więcej edge caseów niż potrafilibyśmy sami wymyślić. Autorskie rozwiązanie (podczas pracy w firmie) ma sens głównie jeśli nie ma istniejących bibliotek, gdy jest słabo otestowana/ma kiepskiej jakości kod (np. niewydajny), tudzież wtedy, gdy użycie jej wymagałoby i tak napisania dużej ilości kodu.

W przypadku nauki programowania próba napisania własnego modułu ma większy sens. Jest to pożyteczne, ponieważ implementując jakąś funkcjonalność zwykle uczymy się przy okazji wielu rzeczy. Przykładowo pisząc własnoręcznie moduł uwierzytelnienia uczymy się bezpiecznie przechowywać hasła użytkowników i ustawiać sesję po zalogowaniu. Mimo to raczej nie należy przesadzać z ilością autorskich rozwiązań.

Projekt nie musi być bardzo rozbudowany. Nie mniej jednak im jest on większy, tym lepiej. Nie powinien być on zbyt prymitywny. Najlepiej skupić się na zakończeniu kluczowej funkcjonalności. Aplikacja powinna na tym etapie robić jedną rzecz (np. pobierać listę newsów z zewnętrznej strony), i robić ja dobrze, bez błędów. Potem ten prosty projekt można rozwinąć, dokładając kolejne części, 'cegiełki'.

Dobrze, gdy projekt zawiera różnorodne funkcjonalności. Poniżej znajduje się lista przykładowych składowych, które warto umieścić w projekcie:
- autoryzacja użytkowników - np. dany typ użytkowników może wejść na konkretne podstrony aplikacji. Osobna sekcja moderatora/admina.
- uwierzytelnienie użytkowników: możliwość założenie konta użytkownika, zalogowania się, wylogowania się, zapamiętywanie zalogowania, przypominanie hasła. Najlepiej wykorzystać do tego jakąś popularną bibliotekę. W przypadku własnego rozwiązania hasła należy hashować bcryptem lub podobnym rozwiązaniem, a nie np. md5 + sól. Logowanie przez social media (facebook, twitter, google) za pomocą OmniAuth.
- integracja z zewnętrznymi serwisami: bezpośrednio przez API, lub najlepiej korzystając z biblioteki, która komunikuje się za pomocą API. Przykładowo upload zdjęć/obrazków na Amazon S3; możliwość odczytania listy plików z Dropboxa w aplikacji; przycisk z opcją udostępnienia treści na facebooku.
- mailing - czyli wysyłka e-maili do użytkowników. Może to być on powiązany z uwierzytelnieniem (email z potwierdzeniem rejestracji/powitalny/z linkiem do resetu hasła)
- manipulacja obrazkami: np. możliwość przycięcia/obrotu zdjęcia do avatara, generowanie kilku rozmiarów zuploadowanych obrazków (np. oryginalny rozmiar i dwa różne rozmiary miniatur).
- paginacja: automatyczne rozłożenie treści na kilka stron, z przyciskami do przeskoczenia do pierwszej, poprzedniej, następnej i ostatniej strony.
- szukajka - możliwość znalezienia słowa/słów w aplikacji
- przetwarzanie w tle: w celu przyspieszenia działania strony, pewne rzeczy, które można przeliczyć/przetworzyć umieszczając zadania w kolejce. Wyspecjalizowana biblioteka/oprogramowanie ściąga po kolei te zadania i wykonuje je w stosownym czasie.
- tagi - możliwość oznaczania danej zawartości przez słowa/wyrażenia. Klikając na dany tag użytkownik powinien zobaczyć listę elementów nim oznaczonych. Przykład: aplikacja umożliwia dodawanie historyjek tekstowych/obrazkowych. Użytkownik może wybrać kilka tagów które zawierają słowa kluczowe tekstu (z istniejącej listy, lub samemu tworząc nowy tag).
- geolokalizacja - możliwość określenia geograficznej lokalizacji użytkownika na podstawie adresu IP, wpisanego adresu miejscowości czy za pomocą geolokalizacji HTML5 (przez zezwolenie przeglądarce na udostępnienie położenia)
- system powiadomień: aplikacja będzie powiadamiać użytkownika o ważnych wydarzeniach, poprzez ikonkę w menu z liczbą powiadomień. Po kliknięciu na ikonę rozwija się lista nieprzeczytanych powiadomień.
- system wiadomości: możliwość wysyłania wiadomości do danego użytkownika/grupy użytkowników, w obrębie aplikacji
- komunikacja serwer-klient za pomocą WebSockets

Aplikacja nie musi dobrze wyglądać, o ile nie aplikujemy na stanowisko web designera czy frontend developera. Należy skupić się przede wszystkim na funkcjonalności. To, że jakaś część aplikacji nie działa, lub występują w niej błędy nie stanowi problemu, o ile nie dzieje się tak w zakresie wielu funkcjonalności/podstron.

Aplikacja powinna być wersjonowana (najlepiej pod gitem). Źródła powinny być przechowywane również poza lokalnym komputerem, tzn. w zewnętrznym serwisie (github.com, bitbucket.com, własny serwer gita z użyciem GitLaba, Gogs itp.). Aktualna wersja aplikacji powinna działać na jakimś hostingu, powinna być zdeployowana. Nie jest konieczne wykupywanie domeny (adresu www). Posiadanie aplikacji w wersji produkcyjnej/stagingowej jest ważne, ponieważ rekruter może poprosić nie tylko o dostęp do kodu, ale również być może zechce zobaczyć aplikacją 'w akcji'. Dodatkowo, będziesz mógł pochwalić się doświadczeniem w deploymencie, co jest też bardzo istotne.

Aplikacja powinna posiadać testy. Przynajmniej jej część powinna być pokryta testami jednostkowymi i integracyjnymi.
