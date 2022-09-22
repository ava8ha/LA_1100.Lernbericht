# Lern-Bericht
Ava Hassani

## Einleitung

Wir haben im Lernatelier ein Zahlenratespiel programmiert mit C# auf VisualStudio.

## Was habe ich gelernt?

Ich habe gelernt, wie man Fehleingaben so wie man will auffängt, also eine Ausgabe dazu, was alles dazu passieren soll, wenn der User eine ungültige Eingabe macht, usw. In diesem Fall, wie man den User nicht weiterspielen lässt, bis er die Bedingungen des Spiels erfüllt, Zahlen zwischen 1 und 100

## Beschreibung
 Drei Medien zum Prozess
 Beschreibung:
Für diesen ganzen Prozess habe ich als erstes Eine Do-While schleife gesetzt und ins D-Statement eine weitere Try-Catch Schleife gesetzt. Ins Try-Statement habe ich ``Console.WriteLine("")`` und ``"Zahl eingeben zwischen 1 und 100"``. Danach wird die Eingabe gespeichert und konvertiert. Dann habe ich die bool Variable ``BenutzerHatsGecheckt`` aufgerufen und zu true geändert. Also wenn der Benutzer das, was im Try-statement steht, erfüllt, hat er es gecheckt und das Spiel wird fortgesetzt. Falls nicht, fällt er in das Catch-statement. In welches ich ``Console.WriteLine("Bitte nur Zahlen!")`` schrieb um den User zu Recht weisen. Das alles wird im Do-Statement festgehalten. Nun zum While-Statement, in welchem die Bedingung war, dass solange der Benutzer es nicht checkt, er in der Schleife festhängt. Dies habe wich mit `` while (! benutzerHatsGecheckt)`` festgehalten. 
Somit ist die Schleife vollendet und der User hängt so lange fest bis er die Bedingung des Spiels erfüllt.

Wie das ganze in Code aussieht:

```C#
using System;
namespace LA_1100
{
    class  Zahlenspiel
    {
        static void Main(string [] args)
        {
            string eingabe;
            int gerateneZahl = 0;
            bool benutzerHatsGecheckt = false;
            int geheimeZahl = new Random().Next(1, 100);
                        do
                        {
                            try
                            {
                                Console.Write("Zahl eingeben (1-100): ");
                                eingabe = Console.ReadLine();
                                gerateneZahl = Convert.ToInt32(eingabe);
                                benutzerHatsGecheckt = true;
                            }
                            catch
                            {
                                Console.WriteLine("Bitte nur Zahlen!");
                            }
                        } while (! benutzerHatsGecheckt)
```
Ausgabe:

<img width="662" alt="image" src="https://user-images.githubusercontent.com/111045914/191711778-ab4da45f-0e42-4e65-bba7-b1390eae52b2.png">

## Verifikation
Text: beschreibt den Vorgang um diese Schleife zu Programmieren und erklärt die Funktion verschiedener Elemente.
Code: Wie es dann schlussendlich auf VisualStudio aussieht und das im Text umgesetzt in Code (ohne restlichen Code für's Spiel).
Bild: Die Ausgabe und dass man tatsächlich nicht weiterspielen kann und es einen jedes Mal korrigiert und erneut eingeben lässt, wenn eine Fehleingabe gemacht wird. Zeigt, dass Fehleingaben aller Art (Zahlen über 100, Minuszahlen, 0, Wörter, Buchstaben) korrigiert werden mit diesem Code.

# Reflexion zum Arbeitsprozess

Ich hatte immer Lust an meinem Code zu Arbeiten und das trial and erorr bzw. ständige Problemlösen bis es funktioniert, hat mir auch spass gemacht. Ich musste mich nicht zwingen am Code zu arbeiten- Was nicht sehr seblstverständlich ist für mich.

Ich hatte sehr viele technische Probleme mit VisualStudio und dem abspeichern meiner Arbeit, was sehr frustrierend war und das Lösen dieser Probleme hat mich insgesamt viel zeit gekostet. Es war ein ständiges Rausfinden, ob mein Weg zur Lösung des Problems funktioniert oder nicht. Dabei bestand auch immer die gefahr, dass der Code, welchen ich angefertigt habe und funktioniert, verloren gehen würde, weil er nicht aufging.
Ich hatte am Anfang, also in den ersten fünf lektionen, keine Ahnung wie ich mit dem Code anfangen soll. Zur lösung hatte ich dann halt einfach anderes zum Projekt erledigt und mich mit C# angewöhnt durch kleine Programme und Videos dazu.

**VBV**: Den Code, der funktioniert, in Notizen abspeichern. So kann ich im schlimmsten Fall den Code immer noch in ein neues Projekt reinkopieren kann.
