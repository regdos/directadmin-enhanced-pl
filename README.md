# Polskie tłumaczenie dla panelu DirectAdmin - szablon Enhanced

Polish translation of DirectAdmin skin pack "Enhanced".

* wersja DA: **1.54**
* kodowanie: **UTF-8**
* autor: **Tomasz Regdos (regdos.com)**
* licencja: **GPL**

## Instalacja

1. Katalog `/pl/` wraz z zawartościę należy skopiować do `/usr/local/directadmin/data/skins/enhanced/lang/`

1. Zawartość katalogu `/templates/` z zachowaniem struktury katalogów należy skopiować do `/usr/local/directadmin/data/templates/`

   Znaczenie poszczególnych plików:
     * `custom/login.html` - formularz logowania do panelu
     * `custom/mail_settings.html` - potwierdzenie założenia konta pocztowego (wyświetlane w panelu)
     * `custom/reseller_limit.txt` - mail do resellera z ostrzeżeniem o wyczerpującym się transferze
     * `custom/user_limit.txt` - mail do użytkownika z ostrzeżeniem o wyczerpującym się transferze/pojemności
     * `custom/message_tech.txt` - mail do admina/resellera o nowym zgłoszeniu
     * `custom/message_user.txt` - mail do użytkownika o nowej wiadomości
     * `custom/lost_password.html`, `custom/lost_password_email.txt`  - system odzyskiwania haseł do panelu
     * `email_pass_change/index.html` - formularz zmiany hasła dla konta pocztowego

## Konfiguracja

1. W edycji kont użykowników będzie do wyboru dodatkowy język `pl`, który można przypisać dla danego użytkownika

1. W celu ustawiania domyślnego języka na `pl` dla nowo zakładanych kont należy w pliku: `/usr/local/directadmin/conf/directadmin.conf` dodać linię `language=pl` lub w przypadku gdy taka zmienna istnieje zmienić jej wartość na `pl` po wykoniu powyższej czynności należy zrestartować directadmin przy użyciu polecenia `/etc/init.d/directadmin restart`

1. Wiadomości powitalne

   Za wiadomości powitalne odpowiadają pliki:
     * `a_welcome.txt` - dodanie administratora
     * `r_welcome.txt` - dodanie resellera
     * `u_welcome.txt` - dodanie użytkownika

   Treści wiadomości mają neutralny charakter.

   **Powitanie Administratora**

   Plik `a_welcome.txt` należy skopiować do katalogu `/usr/local/directadmin/data/admin`.

   Podczas dodawania nowego Admistratora pobierana jest zawartosć tego pliku i wysyłany jest mail powitalny. Aby zmienić temat wysyłanej wiadomości należy w pliku `/usr/local/directadmin/data/admin/admin.conf` zmienić wartość klucza `subject_admin` na `Twoje konto Administratora zostało aktywowane`.

   **Powitanie Resellera**

   Plik `r_welcome.txt` należy skopiować do katalogu `/usr/local/directadmin/data/admin`.

   Podczas dodawania nowego Resellera pobierana jest zawartosć tego pliku i wysyłany jest mail powitalny. Aby zmienić temat wysyłanej wiadomości należy w pliku `/usr/local/directadmin/data/admin/admin.conf` zmienić wartość klucza `subjectadmin` na `Twoje konto Reselera zostało aktywowane`.

   **Powitanie Użytkownika**

   Plik `u_welcome.txt` należy skopiować do katalogu `/usr/local/directadmin/data/users/admin` oraz do katalogu każdego innego Resellera.

   Podczas dodawania nowego Użytkownika pobierana jest zawartosć tego pliku i wysyłany jest mail powitalny. Aby zmienić temat wysyłanej wiadomości należy w pliku `/usr/local/directadmin/data/users/admin/reseller.conf` zmienić wartość klucza `subject` na `Twoje konto dla |domain| zostało utworzone`.

   Powyższa zmiana zadziała tylko dla konta Administratora, ponieważ każdy reseller ma swój plik `u_welcome.txt` dlatego plik `u_welcome.txt` dodatkowo należy skopiować do `/usr/local/directadmin/data/templates/custom` przez co przy dodawaniu nowego Resellera zostanie mu skopiowany nasz przetłumaczony plik. Niestety zmiana tytułu wiadomości nie następuje automatycznie i musimy dokonać ręcznej zmiany zmienić wartość klucza `subject` na `Twoje konto dla |domain| zostało utworzone` w plikach `/usr/local/directadmin/data/users/nazwa_reselera/reseller.conf`

## Wsparcie
Jeżeli uważasz, że to tłumaczenie Ci się przydało i chcesz żeby autor tłumaczenia dalej pracował nad dopracowaniem tłumaczenia możesz przekazać **dobrowolną**  dotację autorowi. Skorzystaj z systemu PayPal wykonując przelew używając konta odbiorcy: tomek@regdos.com lub skorzystać z  poniższego przycisku.

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=JF2TKCR489V5A&lc=PL&item_name=Wspacie%20tlumaczenia%20DirectAdmin&currency_code=PLN)
