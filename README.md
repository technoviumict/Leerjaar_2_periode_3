# Leerjaar 2 Periode 3 Jquery Ajax Opdracht

### Eisen:
    - ophalen JSON bestand
    - JSON bestand filteren
    - informatie vanuit JSON bestand gebruiken in HTML

# Casus
Maak een landingspagina met een form waarbij de gebruikers zich kunnen aanmelden voor nieuwsbrief. 
In de form zijn de volgende velden verplicht:
    - naam
    - achternaam
    - email adres
    - telefoon nummer
Alle velden zijn verplicht. 
Aan FrontEnd:
Als een van de velden leeg zijn of 
email is niet zoals email hoort te zijn,
dan laat je duidelijk melding geven in de HTML met CSS maar ook tekst.

zie tutorial: https://www.wdb24.com/jquery-form-validation-example-without-plugin/
Voorbeeld:
Check if inputveld leeg is:
https://stackoverflow.com/questions/42751647/check-if-input-is-empty-jquery
Als het leeg is, geef aan met css en tekst melding onder het veld waar de error is!

Aan BackEnd:
Het wordt gebruik gemaakt van mailchimp.com 
Het wordt alleen gebruikt gemaakt van Jquery aan de kant van landingspagina.
Met jquery door middel van AJAX wordt gecomuniceerd met mailchimp.
Mailchimp heeft ook API waarmee je met PHP kan werken,
maar dit lossen we op met frontend (met jquery).
#### Belangrijk! gebruik van required in input veld is niet de bedoeling 
<input text="" required /> <-- nee!

VERKEERD ---> https://www.jquery-az.com/boots/demo.php?ex=54.0_1

GOED ---> zie volgende url https://www.jquery-az.com/boots/demo.php?ex=54.0_2

Mailchimp geeft altijd een error melding. 
Voorbeeld: Stel je voor dat een gebruiker zich voor 2de keer aanmeld,
dan geeft mailchimp error terug: Gebruiker met het volgende email is al geregistreerd.
Alle errors laat je zien in HTML.

Er zijn genoeg plugins die zijn met Jquery gemaakt, maar 
gebruik van plugins zijn verboden.
Maak alles zelf met AJAX functie:

$.ajax({
        url: "https://<--eigen mailchimp url -->.us4.list-manage.com/subscribe/post-json",
        type: "POST",
        crossDomain: true,
        contentType: 'application/json',
        data: data,
        dataType: "jsonp", //<-- belangrijk voor cors error
        success: function(data) {
            console.log('success')
            //success handler
        },
        error: function() {
            //error handler
            console.log('error')
        }
    });
});

Gebruik van frameworks zoals "bootstrap" zijn wel toegestaan.

