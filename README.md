first-project-java-spring
Prosty projekt aplikacji webowej w Javie, stworzony z użyciem Spring Boot. Aplikacja wyświetla stronę z możliwością personalizacji wiadomości powitalnej oraz obrazem tła.

Technologie
Java: Główny język programowania.
Spring Boot: Framework użyty do stworzenia aplikacji webowej.
Maven: Narzędzie do zarządzania zależnościami.
Thymeleaf: Silnik szablonów do generowania dynamicznych stron HTML.
Lombok: Biblioteka użyta do redukcji kodu powtarzalnego (np. generowania getterów i setterów).
Funkcje
Wyświetlanie dynamicznej wiadomości powitalnej.
Możliwość personalizacji powitania poprzez parametr w URL.
Obraz tła na stronie.
Wymagania
Przed rozpoczęciem upewnij się, że masz zainstalowane:

Java 17 lub nowsza.
Maven.
Instalacja
Sklonuj repozytorium:

bash
Copy code
git clone https://github.com/your-username/first-project-java-spring.git
Przejdź do katalogu projektu:

bash
Copy code
cd first-project-java-spring
Zbuduj projekt za pomocą Mavena:

bash
Copy code
mvn clean install
Uruchomienie aplikacji
Aby uruchomić aplikację Spring Boot, użyj poniższej komendy Maven:

bash
Copy code
mvn spring-boot:run
Aplikacja uruchomi się i będzie dostępna w przeglądarce pod adresem:

arduino
Copy code
http://localhost:8080
Użycie
Strona główna: Przejdź do http://localhost:8080, a zobaczysz tekst "Hello Vistula, in my first project".
Strona powitalna: Przejdź do http://localhost:8080/greeting, a zobaczysz spersonalizowane powitanie, np. "Hello, World!".
Możesz spersonalizować wiadomość, dodając parametr name w URL, np.:
http://localhost:8080/greeting?name=Vistula wyświetli komunikat "Hello, Vistula!".
Na stronie wyświetlany jest również obraz tła, który można zmodyfikować.
Konfiguracja
Aplikacja domyślnie uruchamia się na porcie 8080, ale możesz to zmienić w pliku application.properties w katalogu src/main/resources.
Obraz tła znajduje się w katalogu src/main/resources/static/images/background.png i może być łatwo podmieniony.
Case Study: Działanie aplikacji
Scenariusz
Wyobraź sobie, że jesteś deweloperem pracującym nad aplikacją, której celem jest wyświetlenie prostej, statycznej strony internetowej, ale z możliwością personalizacji powitania. Chcesz, aby strona była responsywna i mogła dostosowywać powitanie na podstawie parametrów przesłanych w URL. Na dodatek strona ma mieć estetyczny wygląd dzięki obrazowi tła.

Proces działania
Uruchomienie aplikacji: Po uruchomieniu aplikacji za pomocą Spring Boot, serwer zaczyna nasłuchiwać na porcie 8080. Aplikacja ma dwie główne trasy:

Strona główna (/), która zwraca prostą wiadomość powitalną w postaci tekstu "Hello Vistula, in my first project".
Strona powitalna (/greeting), która umożliwia personalizację powitania dzięki parametrowi URL name.
Interakcja z aplikacją:

Jeśli użytkownik przejdzie pod adres http://localhost:8080/greeting, zostanie wyświetlona domyślna wiadomość "Hello, World!".
Gdy użytkownik poda parametr w URL, np. http://localhost:8080/greeting?name=Vistula, na stronie pojawi się komunikat "Hello, Vistula!". Parametr name jest dynamicznie wstrzykiwany w szablon HTML dzięki Thymeleaf.
Dynamiczne wyświetlanie treści: W szablonie greeting.html, Thymeleaf używa zmiennej ${name} do dynamicznego wyświetlenia powitania. Oprócz powitania, szablon zawiera również paragraf z przykładowym tekstem oraz obraz tła (background.png), który jest ładowany za pomocą wyrażenia th:src.

Modyfikacja strony:

Personalizacja: Użytkownik może zmienić tekst powitania, po prostu modyfikując parametr name w URL.
Zmiana wyglądu: Użytkownik może łatwo zmienić obraz tła, podmieniając plik background.png w katalogu src/main/resources/static/images.
Przykład użycia
Użytkownik odwiedza stronę główną: http://localhost:8080/.
Zostaje wyświetlone: "Hello Vistula, in my first project".
Użytkownik odwiedza stronę powitalną: http://localhost:8080/greeting?name=Vistula.
Zostaje wyświetlone: "Hello, Vistula!" z obrazem tła.
Wnioski
Aplikacja działa płynnie, dostosowując wyświetlane powitanie do podanego parametru w URL. Dzięki użyciu Spring Boot i Thymeleaf, implementacja jest prosta, a dodanie kolejnych funkcjonalności (np. większej personalizacji lub nowych stron) może być łatwo zrealizowane. Obraz tła i dynamiczne powitanie dodają estetyki i personalizacji, co sprawia, że aplikacja może być ciekawym punktem wyjściowym do bardziej zaawansowanych projektów webowych.

