
First-Project-Java-Spring


Prosta aplikacja webowa w Javie, stworzona z użyciem Spring Boot, wyświetlająca personalizowaną wiadomość powitalną oraz obraz tła.

Technologie:

Java: Główny język. 
Spring Boot: Framework aplikacji webowej.
Maven: Zarządzanie zależnościami. 
Thymeleaf: Generowanie dynamicznych stron HTML. 
Lombok: Redukcja kodu powtarzalnego.


 Funkcje: Wyświetlanie personalizowanego powitania. Obraz tła na stronie. 
 
 Wymagania Java 17 lub nowsza. Maven.
   
  1.Instalacja git clone https://github.com/your-username/first-project-java-spring.git cd first-project-java-spring 
  
  2.Zbuduj projekt: mvn clean install 
  
  3.Uruchomienie: mvn spring-boot:run Aplikacja będzie dostępna pod adresem: http://localhost:8080.

4.Użycie:

 Strona główna: http://localhost:8080 wyświetla
 "Hello Vistula, in my first project". 
 
 Strona powitalna: http://localhost:8080/greeting?name=Vistula wyświetla spersonalizowane powitanie "Hello, Vistula!". 
 
 Obraz tła znajduje się w katalogu src/main/resources/static/images/background.png i można go zmienić.
