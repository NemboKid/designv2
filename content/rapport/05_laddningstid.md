---
---
Laddningstider kmom05
=========================

Rapporten handlar om att designmässigt analysera tre olika hemsidor, där man ska träna på att bli medveten om design, färger och olika mönster som kan finnas. Egentligen ska jag bara förmedla vad jag noterar och sedan skriva en kort analys av det.

Urval
-----------------------
Jag valde bokningssajter för hotell. Det känns som att det är ett segment där laddningstider, prestanda och SEO är mer viktigt än i de flesta andra branscher. Jag tog de två som jag hade i bakhuvudet, hotels.com och booking.com. Sedan kom jag inte på någon mer och googlade fram kayak.com som kom i toppen bland sökresultaten, vilket kanske indikerar att de har en väldigt bra SEO.



Metod
------------------------
Jag körde först respektive hemsida i https://developers.google.com/speed/pagespeed/insights, både mobile och desktop. Därefter körde jag Lighthouse tre gånger för varje hemsida och satte in varje resultat i ett spreadsheet. Sedan drog jag snitt av resultatet. Slutligen i devtools kollade jag laddningstiden och storleken för varje hemsida.



Resultat
------------------------
Jag listar mina resultat nedan i inbördes ordning och skriver sedan några avslutande ord om vad jag hittat.


###1. Hotels.com

[FIGURE src="image/hotels.png?w=400"]

#####Kommentar
Jag tyckte sidan laddade ganska bra, om än något segt kanske. De skulle kunna minimera sin javascript.

#####Resultat

<table>
<tr>
  <th>Sida</th>
    <td>Hotels.com</td>
    <td>hotels.com/hotellerbjudanden/</td>
    <td>groups.hotels.com</td>
</tr>
<tr>
  <th>Laddningstid</th>
    <td>4.62</td>
    <td>2.56</td>
    <td>6.6</td>
</tr>
<tr>
  <th>Resources</th>
    <td>2.1MB</td>
    <td>2.4MB</td>
    <td>4.2MB</td>
</tr>
<tr>
  <th>Requests</th>
    <td>31.7</td>
    <td>30</td>
    <td>73</td>
</tr>
<tr>
  <th>Mobile</th>
    <td>59/100</td>
    <td>-</td>
    <td>-</td>
</tr>
<tr>
  <th>Desktop</th>
    <td>91/100</td>
    <td>-</td>
    <td>-</td>
</tr>
</table>



###2. Booking.com

[FIGURE src="image/booking.png?w=400"]

#####Kommentar
Lite som Hotels.com, fast ytterligare lite segare. Hade förväntat mig bättre hastighet från en så stor sida. De kan minska javascript, men även DOM-trädet, där de har för många element.

#####Resultat

<table>
<tr>
  <th>Sida</th>
    <td>Booking.com</td>
    <td>flight.booking.com</td>
    <td>experience.booking.com</td>
</tr>
<tr>
  <th>Laddningstid</th>
    <td>5.7</td>
    <td>2.1</td>
    <td>3.5</td>
</tr>
<tr>
  <th>Resources</th>
    <td>4.9MB</td>
    <td>1.5MB</td>
    <td>3.7MB</td>
</tr>
<tr>
  <th>Requests</th>
    <td>154</td>
    <td>31.3</td>
    <td>89.3</td>
</tr>
<tr>
  <th>Mobile</th>
    <td>52/100</td>
    <td>-</td>
    <td>-</td>
</tr>
<tr>
  <th>Desktop</th>
    <td>89/100</td>
    <td>-</td>
    <td>-</td>
</tr>
</table>


###3. Kayak

[FIGURE src="image/kayak.png?w=400"]

#####Resultat
Väldigt seg hemsida som laddar väldigt länge och bara gör fler requests hela tiden. De har precis som Booking många DOM-element, men nästan det femdubbla. Javscript kan minskas.

<table>
<tr>
  <th>Sida</th>
    <td>kayak.com</td>
    <td>kayak.com/hotels</td>
    <td>kayak.com/cars</td>
</tr>
<tr>
  <th>Laddningstid</th>
    <td>11.5</td>
    <td>5.8</td>
    <td>5.4</td>
</tr>
<tr>
  <th>Resources</th>
    <td>10.8MB</td>
    <td>8.1MB</td>
    <td>6.2MB</td>
</tr>
<tr>
  <th>Requests</th>
    <td>151.7</td>
    <td>120</td>
    <td>87.3</td>
</tr>
<tr>
  <th>Mobile</th>
    <td>38/100</td>
    <td>-</td>
    <td>-</td>
</tr>
<tr>
  <th>Desktop</th>
    <td>51/100</td>
    <td>-</td>
    <td>-</td>
</tr>
</table>


####Länk till Spreadsheet:
<a href="https://docs.google.com/spreadsheets/d/1YoH_a0nsZQTsfkVX2Mx8mCQX5NQ3YZEJ3qMQIublPmE/edit?usp=sharing">Google Sheets</a>



####Slutkommentar:

Hotels.com presterade lite bättre än Booking, medan Kayak hamnade långt efter. Allas mobilsidor är anmärkningsvärt dåliga, men jag tror det beror på att de har appar och att fokus ligger där.

Alla sidor behöver minska sin javascript, medan Booking och Kayak har för många DOM-element sett till vad som är rekommenderat (runt 1500).

Jag tycker att en sida bör ha en laddningstid på under 2 sekunder, men det beror så klart på vad sidan innehåller. I Kayaks fall var den stor, så då kan man förstå att det tar något längre, men jag tror alla tappar lite kunder på detta och skulle kunna se detta som ett förbättringsområde. Generellt trodde jag att dessa typer av hemsidor skulle ha topp på allt, men de är ganska tunga och därför är det kanske svårt att få toppresultat.

För <a href="https://developers.google.com/speed/pagespeed/insights/">PageSpeed Insights</a> så mätte jag endast huvudsidan, både mobilt och desktop. Därför finns inget betyg för undersidorna i tabellerna.



#####Grupp:
Jag var ensam.
