---
title: "Praxisphasenbericht"
#subtitle: "From Markdown to LaTeX to PDF"
author: "Fayez Sohaila"

studentnumber: "1303146"
date: "30. November 2026"

reviewer1:  "Prof.Dr.Robin Rasch, HSBI"

#keywords: [Markdown, Example]
lang: de-DE


## The behaviour of headers and footers in Eisvogel is a bit ... unusual. The following
## metadata variables change the format to the standard format. Please adjust as needed.
##
## When using Eisvogel, very long titles may require (multiple) line breaks in the page
## headers. In this case, please define a shortened one-line version of your long title
## to be used in the page headers.
### Example: header-left: "Shortened version of title for running page headers ..."
##
header-left:   "\\hspace{1mm}"  # off
header-center: "\\headmark"     # chapter name
header-right:  "\\hspace{1mm}"  # off
footer-left:   "\\hspace{1mm}"  # off
footer-center: "\\pagemark"     # page number
footer-right:  "\\hspace{1mm}"  # off



---





# Einleitung

Dieses Dokument beschreibt den Ablauf und die Inhalte meiner Praxisphase, die ich im Zeitraum vom 17.08.2026 bis 30.11.2026 bei der ecomify GmbH am Standort Bielefeld absolviert habe. Die ecomify GmbH ist ein IT-Beratungsunternehmen, das sich auf E-Commerce-Lösungen, Systemintegration sowie die Entwicklung von Open-Source-Software spezialisiert hat. Im Rahmen meiner Praxisphase war ich hauptsächlich im Bereich der Softwareentwicklung tätig. Dabei erhielt ich Einblicke in verschiedene Entwicklungsprozesse und konnte mit unterschiedlichen Technologien und Werkzeugen arbeiten.
Zu Beginn meiner Praxisphase wurde ich in das Team und die bestehenden Arbeitsabläufe eingeführt. Dabei lernte ich meine Kollegen kennen und erhielt eine Einführung in die organisatorischen und technischen Rahmenbedingungen meiner Tätigkeit. Außerdem wurden mir die für meine Arbeit benötigten Zugänge und Arbeitsmittel eingerichtet und die grundlegenden Abläufe zur Bearbeitung von Aufgaben erklärt.
Ein wichtiger Bestandteil meiner Praxisphase war die Arbeit mit Apache OFBiz. Dabei handelt es sich um ein Open-Source-Framework, das unter anderem für die Entwicklung von Unternehmensanwendungen und E-Commerce-Lösungen eingesetzt wird. Im Verlauf der Praxisphase konnte ich mich mit dem Aufbau und der Funktionsweise von Apache OFBiz vertraut machen und praktische Erfahrungen bei der Entwicklung und Anpassung von Anwendungen sammeln.
Für die Bearbeitung meiner Aufgaben kamen verschiedene Programmiersprachen und Technologien zum Einsatz. Dazu gehörten insbesondere Java, SQL, Groovy, FreeMarker (FTL) und HTML. Darüber hinaus wurde Git zur Versionsverwaltung verwendet. Die einzelnen Aufgaben wurden über ein Ticketsystem organisiert. Für jede Aufgabe wurde ein eigenes Ticket erstellt, anschließend bearbeitet und nach Abschluss dokumentiert. Die Änderungen am Quellcode wurden mithilfe von Git in das entsprechende Repository übertragen.
Ein wesentlicher Bestandteil der Praxisphase war ein Ausarbeitungsprojekt, das aus insgesamt zehn Aufgaben bestand. Die Aufgaben behandelten unterschiedliche Bereiche der Softwareentwicklung und dienten dazu, die verwendeten Technologien und Arbeitsweisen praktisch anzuwenden. Der Aufgaben bestand beispielsweise in der Entwicklung eines eigenen Wetterstations-Plugins innerhalb von Apache OFBiz. Dafür erstellte ich eine Benutzeroberfläche mit HTML und FreeMarker, implementierte die Benutzerinteraktionen mit Groovy und entwickelte eine Java-Klasse zur Verarbeitung der benötigten Events. Die Anwendung ermöglichte es, Temperaturwerte einzugeben, zu speichern und verschiedene statistische Auswertungen durchzuführen. Im weiteren Verlauf wurde die Speicherung der Daten von einer Session auf eine Datenbank umgestellt.
Neben der Entwicklung der Wetterstations-Anwendung beschäftigte ich mich mit der Erstellung von Services und Workern sowie der Entwicklung einer REST-API innerhalb von Apache OFBiz. Weitere Aufgaben umfassten die Anpassung und Verschiebung bestehender Klassen und Methoden zwischen Plugins, die Verbesserung der Wartbarkeit von Code sowie die Hinterlegung von AGB-Inhalten und deren englischen Übersetzungen.
Ein weiterer Schwerpunkt meiner Praxisphase war das Thema Softwaretesting. Nach einer selbstständigen Einarbeitung in die Grundlagen des Testens beschäftigte ich mich mit der Analyse und Überprüfung der Klasse EcsPartyWorker. Dabei plante ich zunächst geeignete Testfälle, dokumentierte diese und setzte sie anschließend in Form von Integrationstests um. Zusätzlich beschäftigte ich mich mit der Bereitstellung benötigter Testdaten mithilfe von XML-Konfigurationsdateien.
Neben der eigentlichen Implementierung spielte auch die Fehleranalyse und Fehlerbehebung eine wichtige Rolle. Während der Bearbeitung der Aufgaben traten verschiedene Fehler auf, die ich untersuchte und behob. Dadurch konnte ich meine Fähigkeiten bei der systematischen Suche nach Fehlerursachen erweitern und ein besseres Verständnis für den Aufbau und das Zusammenspiel der verschiedenen Komponenten entwickeln.
Die Praxisphase war insgesamt darauf ausgerichtet, theoretische Kenntnisse aus dem Studium auf konkrete praktische Problemstellungen anzuwenden. Durch die Bearbeitung der verschiedenen Aufgaben konnte ich sowohl meine technischen Kenntnisse in der Softwareentwicklung erweitern als auch Erfahrungen mit typischen Arbeitsabläufen in einem professionellen Entwicklungsumfeld sammeln. Der Schwerpunkt dieses Berichts liegt daher auf den während der Praxisphase durchgeführten Aufgaben, den dabei eingesetzten Technologien sowie den gewonnenen Erfahrungen und Erkenntnissen.

# Einführung in Apache OFBiz und die Entwicklungsumgebung


Zu Beginn meiner Praxisphase erhielt ich eine Einführung in Apache OFBiz, da dieses Framework eine zentrale Rolle bei den Entwicklungsaufgaben spielte. Apache OFBiz ist ein Open-Source-Framework, das zur Entwicklung von Unternehmensanwendungen eingesetzt wird. Es stellt verschiedene Funktionen und Komponenten bereit, die bei der Umsetzung komplexer Geschäftsanwendungen verwendet werden können.
Das Framework bietet eine umfangreiche technische Grundlage, auf der Anwendungen aufgebaut und erweitert werden können. Dazu gehören unter anderem Funktionen zur Datenverwaltung, zur Verarbeitung von Geschäftsprozessen und zur Kommunikation zwischen verschiedenen Anwendungskomponenten.
Während meiner Praxisphase arbeitete ich hauptsächlich innerhalb der bestehenden Apache-OFBiz-Umgebung. Dabei lernte ich schrittweise den Aufbau des Frameworks kennen und beschäftigte mich mit der Entwicklung eigener Komponenten sowie der Anpassung bereits vorhandener Funktionen.
Da ich vor Beginn der Praxisphase noch keine praktischen Erfahrungen mit Apache OFBiz gesammelt hatte, musste ich mich zunächst mit dessen Struktur und Funktionsweise vertraut machen. Durch die Bearbeitung der verschiedenen Aufgaben konnte ich mein Wissen kontinuierlich erweitern und die einzelnen Bestandteile des Frameworks besser verstehen.

## Aufbau und Funktionsweise von Plugins

Ein wichtiger Bestandteil meiner Arbeit mit Apache OFBiz war die Verwendung von Plugins. Plugins ermöglichen es, zusätzliche Funktionen innerhalb des Frameworks zu entwickeln und bestehende Anwendungen zu erweitern.
Im Rahmen meiner Entwicklungsaufgabe erstellte ich ein eigenes Plugin für eine Wetterstations-Anwendung. Dabei lernte ich, wie ein Plugin aufgebaut ist und welche Dateien und Komponenten für die Implementierung benötigt werden.
Die Entwicklung innerhalb eines eigenen Plugins ermöglicht eine strukturierte Trennung verschiedener Funktionen. Dadurch können einzelne Bestandteile unabhängig voneinander entwickelt, angepasst und wiederverwendet werden.
Im weiteren Verlauf meiner Praxisphase arbeitete ich auch mit bereits vorhandenen Plugins. Dabei erhielt ich Aufgaben, bei denen Klassen und Methoden zwischen verschiedenen Plugins verschoben werden mussten. Dadurch lernte ich, wie die einzelnen Plugins miteinander verbunden sind und welche Anpassungen erforderlich sind, wenn bestehender Code an eine andere Stelle innerhalb des Frameworks verschoben wird.

## Verwendete Programmiersprachen und Technologien

Für die Bearbeitung der Entwicklungsaufgaben kamen verschiedene Programmiersprachen und Technologien zum Einsatz. Jede davon erfüllte innerhalb der Anwendungen eine bestimmte Aufgabe. Java wurde insbesondere für die Entwicklung von Klassen und die Implementierung bestimmter Anwendungsfunktionen verwendet. Während meiner Praxisphase erstellte ich unter anderem eine Java-Klasse zur Verarbeitung von Events innerhalb der Wetterstations-Anwendung. Außerdem beschäftigte ich mich mit bestehenden Java-Klassen, deren Funktionsweise ich zunächst verstehen musste, bevor ich Änderungen vornehmen oder Tests implementieren konnte. Ein Beispiel dafür war die Klasse EcsPartyWorker, für die ich später Integrationstests entwickelte.
Groovy wurde innerhalb der Apache-OFBiz-Umgebung für die Verarbeitung von Anwendungslogik und Benutzerinteraktionen eingesetzt. Bei der Entwicklung der Wetterstations-Anwendung verwendete ich Groovy, um die eingegebenen Daten zu verarbeiten und die benötigten Funktionen umzusetzen. Dadurch konnte ich praktische Erfahrungen mit der Verwendung von Groovy innerhalb eines bestehenden Frameworks sammeln.
SQL wird zur Abfrage und Verwaltung von Datenbanken verwendet. Im Rahmen meiner Praxisphase beschäftigte ich mich insbesondere mit der Speicherung und dem Abruf von Daten. Bei der Entwicklung der Wetterstations-Anwendung sollten die eingegebenen Temperaturwerte zunächst innerhalb einer Session gespeichert werden. In einem späteren Entwicklungsschritt wurde diese Speicherung auf eine Datenbank umgestellt. Dadurch konnten die Daten dauerhaft gespeichert und bei Bedarf erneut abgerufen werden.
HTML wurde zur Erstellung und Strukturierung der Benutzeroberflächen verwendet. Für die dynamische Darstellung der Inhalte kam FreeMarker zum Einsatz. Bei der Wetterstations-Anwendung erstellte ich mithilfe dieser Technologien eine Benutzeroberfläche, über die Benutzer Temperaturwerte eingeben und die Ergebnisse der Berechnungen anzeigen lassen konnten. FreeMarker ermöglichte dabei die dynamische Einbindung der von der Anwendung bereitgestellten Daten in die HTML-Seiten.

## Versionsverwaltung mit Git

Für die Verwaltung des Quellcodes wurde Git verwendet. Während meiner Praxisphase war Git ein fester Bestandteil der täglichen Entwicklungsarbeit. Für jede Aufgabe wurde zunächst ein eigenes Ticket erstellt. Anschließend bearbeitete ich die jeweilige Aufgabe und speicherte die vorgenommenen Änderungen mit Git.
Nach Abschluss einer Aufgabe wurden die Änderungen durch einen Commit dokumentiert und anschließend in das entsprechende Repository übertragen. Bei bestimmten Aufgaben erfolgte die Übertragung auf einen Feature-Branch.
Durch diese Vorgehensweise konnten die einzelnen Änderungen nachvollzogen und die verschiedenen Entwicklungsaufgaben voneinander getrennt bearbeitet werden.
Im Verlauf meiner Praxisphase konnte ich dadurch praktische Erfahrungen mit der Versionsverwaltung sammeln und den Umgang mit Repositories, Commits und Feature-Branches verbessern.

## Organisation der Entwicklungsaufgaben

Die Aufgaben während meiner Praxisphase wurden über ein Ticketsystem organisiert. Für jede neue Aufgabe musste zunächst ein eigenes Ticket erstellt werden. In diesem wurde die jeweilige Aufgabenstellung festgehalten.
Anschließend begann ich mit der Analyse der Anforderungen und der Untersuchung der betroffenen Komponenten. Nach der Klärung der Aufgabenstellung setzte ich die erforderlichen Änderungen im Quellcode um.
Während der Implementierung überprüfte ich die Änderungen und behob gegebenenfalls auftretende Fehler. Nach erfolgreicher Fertigstellung wurde die Aufgabe abgeschlossen und der geänderte Quellcode mit Git in das Repository übertragen.
Diese Arbeitsweise ermöglichte eine strukturierte Bearbeitung der Aufgaben und sorgte dafür, dass die durchgeführten Änderungen nachvollziehbar dokumentiert wurden.

# Entwicklung einer Wetterstations-Anwendung

Eine der ersten praktischen Aufgaben während meiner Praxisphase bestand darin, eine Wetterstations-Anwendung innerhalb von Apache OFBiz zu entwickeln. Die Anwendung sollte als eigenständiges Plugin erstellt werden, um die verschiedenen Funktionen unabhängig von anderen bestehenden Plugins zu implementieren und in das Framework zu integrieren.
Das Ziel der Anwendung war es, dem Benutzer die Möglichkeit zu geben, einen Tag und die dazugehörige Temperatur einzugeben. Die eingegebenen Werte sollten anschließend gespeichert und auf der Benutzeroberfläche dargestellt werden. Zusätzlich sollte die Anwendung verschiedene statistische Auswertungen auf Grundlage der eingegebenen Temperaturwerte durchführen. Dazu gehörten der Durchschnittswert, die minimale Temperatur, die maximale Temperatur sowie die maximale Differenz zwischen den gespeicherten Temperaturwerten.
Für die Umsetzung kamen verschiedene Technologien zum Einsatz. Die Benutzeroberfläche wurde mit HTML und FreeMarker erstellt. Für die Verarbeitung der Benutzerinteraktionen und die Anwendungslogik verwendete ich Groovy. Zusätzlich entwickelte ich eine Java-Klasse zur Verarbeitung der benötigten Events.
Die Aufgabe bestand aus mehreren aufeinander aufbauenden Schritten. Zunächst sollte die Wetterstations-Anwendung erstellt werden, bei der die eingegebenen Daten innerhalb einer Session gespeichert werden. In einem weiteren Schritt sollte die Speicherung auf eine Datenbank umgestellt werden, sodass die Daten dauerhaft verfügbar sind und bei Bedarf erneut abgerufen werden können.

## Implementierung der Benutzeroberfläche mit FreeMarker und HTML

Für die Erstellung der Benutzeroberfläche verwendete ich HTML und FreeMarker. HTML diente zur Strukturierung der Oberfläche, während FreeMarker zur dynamischen Darstellung der Inhalte eingesetzt wurde.
Die Oberfläche wurde so aufgebaut, dass Benutzer einen Tag und die dazugehörige Temperatur eingeben konnten. Die Eingabefelder ermöglichten es, die benötigten Informationen an die Anwendung zu übermitteln.
Zusätzlich wurde ein Bereich zur Darstellung der bereits eingegebenen Temperaturwerte erstellt. Die Anwendung sollte die gespeicherten Daten übersichtlich anzeigen und die berechneten statistischen Ergebnisse ebenfalls auf der Benutzeroberfläche darstellen.
Durch die Verwendung von FreeMarker konnten die von der Anwendungslogik bereitgestellten Daten dynamisch in die HTML-Seiten eingebunden werden. Dadurch war es möglich, die Oberfläche abhängig von den eingegebenen und gespeicherten Werten zu aktualisieren.

## Implementierung der Interaktionen mit Groovy und Java

Nachdem die grundlegende Benutzeroberfläche erstellt worden war, implementierte ich die Verarbeitung der Benutzereingaben.
Für die Anwendungslogik und die Benutzerinteraktionen verwendete ich Groovy. Die eingegebenen Informationen mussten entgegengenommen, verarbeitet und anschließend für die weitere Verwendung bereitgestellt werden.
Zusätzlich entwickelte ich eine Java-Klasse zur Verarbeitung der benötigten Events. Diese Klasse wurde für die entsprechenden Ereignisse innerhalb der Anwendung verwendet und ermöglichte die Verbindung zwischen den Benutzereingaben und der weiteren Verarbeitung.
Dabei musste ich verstehen, wie die verschiedenen Komponenten innerhalb von Apache OFBiz zusammenarbeiten und wie die Informationen zwischen der Benutzeroberfläche und der Anwendungslogik übertragen werden.
Nachdem die einzelnen Bestandteile implementiert waren, verband ich sie miteinander, sodass die Eingaben des Benutzers verarbeitet und die entsprechenden Ergebnisse auf der Benutzeroberfläche angezeigt werden konnten.

## Speicherung der Temperaturwerte in der Session

Im ersten Umsetzungsschritt sollten die eingegebenen Temperaturwerte innerhalb einer Session gespeichert werden.
Eine Session ermöglicht es, Informationen für einen Benutzer während seiner Interaktion mit einer Anwendung vorübergehend zu speichern. Dadurch können Daten über mehrere Anfragen hinweg verfügbar bleiben, ohne dass sie unmittelbar dauerhaft in einer Datenbank gespeichert werden müssen.
In meiner Implementierung wurden die vom Benutzer eingegebenen Tages- und Temperaturwerte entgegengenommen und in der Session abgelegt. Anschließend konnten diese Informationen wieder abgerufen und auf der Benutzeroberfläche angezeigt werden.
Auf Grundlage der gespeicherten Werte implementierte ich außerdem die Berechnung verschiedener statistischer Kennzahlen.
Dazu gehörten:
- Average: Berechnung der durchschnittlichen Temperatur aller eingegebenen Werte.
- Minimum: Ermittlung der niedrigsten eingegebenen Temperatur.
- Maximum: Ermittlung der höchsten eingegebenen Temperatur.
- Maximale Differenz: Ermittlung der größten Differenz zwischen den gespeicherten Temperaturwerten.

Die berechneten Ergebnisse wurden anschließend ebenfalls auf dem Bildschirm dargestellt. Damit war die erste Version der Wetterstations-Anwendung umgesetzt.

## Erweiterung um eine Datenbankspeicherung

In einem weiteren Entwicklungsschritt sollte die Anwendung so angepasst werden, dass die Temperaturwerte nicht mehr ausschließlich innerhalb der Session gespeichert werden, sondern dauerhaft in einer Datenbank abgelegt werden.
Der Grund dafür war, dass die Daten bei einer reinen Session-Speicherung nur vorübergehend verfügbar sind. Durch die Verwendung einer Datenbank können die Informationen dauerhaft gespeichert und zu einem späteren Zeitpunkt erneut abgerufen werden.
Für diese Erweiterung musste ich den bestehenden Code entsprechend anpassen. Die bisherige Verarbeitung, bei der die Daten aus der Session gelesen wurden, sollte durch einen Zugriff auf die Datenbank ersetzt werden.
Dafür passte ich die Implementierung so an, dass die eingegebenen Temperaturwerte in der Datenbank gespeichert und bei der Anzeige wieder aus der Datenbank abgerufen werden konnten.
Auch die Berechnungen der statistischen Werte mussten entsprechend angepasst werden. Die Anwendung sollte weiterhin den Durchschnitt, die minimale und maximale Temperatur sowie die maximale Differenz ermitteln. Die dafür benötigten Werte sollten nun jedoch aus der Datenbank stammen und nicht mehr aus der Session.
Nach der Anpassung wurden die Daten somit dauerhaft gespeichert und konnten unabhängig von der ursprünglichen Session erneut abgerufen werden.

## Fehleranalyse und Fehlerbehebung

Während der Implementierung traten verschiedene Fehler auf, die ich zunächst untersuchen und anschließend beheben musste.
Da ich mich zu diesem Zeitpunkt noch mit den grundlegenden Strukturen von Apache OFBiz vertraut machte, war die Fehlersuche teilweise eine Herausforderung. Insbesondere musste ich nachvollziehen, an welcher Stelle die Fehler auftraten und welche Komponenten davon betroffen waren.
Ich analysierte die entsprechenden Codeabschnitte, überprüfte die Implementierung und nahm die erforderlichen Anpassungen vor. Anschließend testete ich die Anwendung erneut, um sicherzustellen, dass die Funktionen korrekt ausgeführt wurden.
Durch diesen Prozess konnte ich lernen, Fehler systematisch zu untersuchen und mögliche Ursachen schrittweise einzugrenzen. Außerdem gewann ich ein besseres Verständnis für das Zusammenspiel zwischen Benutzeroberfläche, Anwendungslogik, Session und Datenbank.

## Abschluss und Übertragung in das Repository

Nachdem die Implementierung abgeschlossen und die aufgetretenen Fehler behoben waren, überprüfte ich die Funktionsfähigkeit der Wetterstations-Anwendung.
Dabei stellte ich sicher, dass die Benutzereingaben verarbeitet, die Temperaturwerte gespeichert und die statistischen Ergebnisse korrekt angezeigt wurden.
Nach erfolgreichem Abschluss übertrug ich die vorgenommenen Änderungen mithilfe von Git in das entsprechende Repository.
Mit dieser Aufgabe konnte ich eine vollständige kleine Anwendung innerhalb von Apache OFBiz entwickeln. Besonders hilfreich war dabei die praktische Arbeit mit mehreren Technologien, die gemeinsam für die Umsetzung der verschiedenen Funktionen benötigt wurden.
Durch die Entwicklung des eigenen Plugins konnte ich meine Kenntnisse in HTML, FreeMarker, Groovy und Java erweitern. Außerdem sammelte ich Erfahrungen mit der Session-Verwaltung, der Datenbankspeicherung und der Fehlerbehebung innerhalb eines bestehenden Frameworks.


# Entwicklung von Services, Workern und einer REST-API

Nach der Entwicklung der Wetterstations-Anwendung beschäftigte ich mich mit einer weiteren Aufgabe innerhalb von Apache OFBiz. Dabei ging es um die Erstellung und Verwendung von Services und Workern. Ziel dieser Aufgabe war es, bestimmte Funktionen so umzusetzen, dass sie wiederverwendbar sind und bei Bedarf von verschiedenen Stellen innerhalb der Anwendung aufgerufen werden können.
Im Anschluss daran sollte eine REST-API entwickelt werden, über die die zuvor erstellten Services aufgerufen werden können. Dadurch sollte eine Schnittstelle entstehen, über die die Funktionalitäten auch außerhalb des unmittelbaren Anwendungskontexts angesprochen werden können.

## Einarbeitung in Services und Worker

Zu Beginn der Aufgabe musste ich mich zunächst mit dem Konzept der Services und Worker in Apache OFBiz vertraut machen. Da ich bis zu diesem Zeitpunkt noch keine umfangreichen Erfahrungen mit diesen Bestandteilen des Frameworks gesammelt hatte, stellte die Aufgabe eine neue Herausforderung für mich dar.
Ich setzte mich mit ihrer Funktionsweise und ihrer Verwendung innerhalb von OFBiz auseinander. Dabei lernte ich, wie Funktionen ausgelagert und so strukturiert werden können, dass sie nicht ausschließlich an eine einzelne Stelle im Programm gebunden sind. Insbesondere die Wiederverwendbarkeit des Codes spielte dabei eine wichtige Rolle.
Durch die praktische Arbeit konnte ich besser verstehen, wie Services in Apache OFBiz eingesetzt werden und wie sie von anderen Komponenten aufgerufen werden können. Auch die Arbeit mit Workern war ein neuer Bestandteil meiner Einarbeitung. Im Verlauf der Aufgabe gewann ich zunehmend Sicherheit im Umgang mit diesen Konzepten.

## Umsetzung der Services und Worker

Nach der Einarbeitung begann ich mit der Umsetzung der geforderten Funktionalitäten. Dabei bestand die Herausforderung darin, die Aufgabenstellung auf die Struktur und Funktionsweise von Apache OFBiz zu übertragen.
Ich arbeitete daran, die benötigten Funktionen in Services und Workern umzusetzen. Dadurch sollte der Code übersichtlicher aufgebaut und die Wiederverwendung einzelner Funktionalitäten ermöglicht werden. Die ausgelagerten Funktionen sollten bei Bedarf aufgerufen werden können, ohne dass die entsprechende Logik an mehreren Stellen erneut implementiert werden muss.
Während der Umsetzung setzte ich mich intensiv mit der vorhandenen OFBiz-Struktur auseinander. Da die Arbeit mit Services und Workern für mich zunächst neu war, musste ich verschiedene Zusammenhänge nachvollziehen und die Funktionsweise anhand der bestehenden Projektstruktur verstehen.
Die Aufgabe konnte ich schließlich erfolgreich abschließen. Dabei konnte ich meine Kenntnisse über den Aufbau von Apache OFBiz erweitern und besser nachvollziehen, wie sich wiederverwendbare Programmfunktionen innerhalb des Frameworks organisieren lassen.

## Entwicklung einer REST-API

Im nächsten Schritt sollte eine REST-API aufgebaut werden, über die die zuvor erstellten Services aufgerufen werden können. Damit wurde die bisherige Arbeit um eine Schnittstelle erweitert, über die die Funktionalitäten erreichbar sein sollten.
Auch dieser Teil der Aufgabe erforderte eine weitere Einarbeitung, da ich mich zunächst mit dem Zusammenhang zwischen der REST-API und den Services beschäftigen musste. Dabei war insbesondere wichtig zu verstehen, wie die Schnittstelle mit den vorhandenen Services verbunden wird, damit die gewünschten Funktionen über die API aufgerufen werden können.
Anschließend setzte ich die REST-API entsprechend der Aufgabenstellung um. Dabei achtete ich darauf, dass die Schnittstelle den Aufruf der zuvor erstellten Services ermöglicht. Die Entwicklung der API stellte somit den nächsten Schritt dar, um die implementierten Funktionalitäten über eine definierte Schnittstelle zugänglich zu machen.
Die REST-API konnte ich erfolgreich fertigstellen. Damit war die gestellte Aufgabe abgeschlossen.

# Weitere Entwicklungsaufgaben

Neben der Entwicklung der Wetterstations-Anwendung sowie der Arbeit mit Services, Workern und einer REST-API erhielt ich im Verlauf meiner Praxisphase weitere Entwicklungsaufgaben. Diese Aufgaben dienten dazu, bestehende Funktionalitäten innerhalb von Apache OFBiz anzupassen, die Codequalität zu verbessern und mich mit unterschiedlichen Bereichen der vorhandenen Projektstruktur vertraut zu machen.
Die Aufgaben wurden jeweils über Tickets organisiert. Nach der Bearbeitung überprüfte ich meine Änderungen und übertrug den entsprechenden Code mithilfe von Git in das Repository. Im Folgenden werden einige dieser Aufgaben näher beschrieben.

## Verschieben einer Klasse und Methode zwischen Plugins

Eine weitere Aufgabe erhielt ich vom Projektleiter. Dabei sollte eine Klasse sowie eine Methode von einem Plugin in ein anderes verschoben werden. Anschließend musste der betroffene Code entsprechend angepasst werden, damit die Funktionalität weiterhin an der vorgesehenen Stelle verwendet werden konnte.
Zunächst musste ich nachvollziehen, wo sich die betreffende Klasse und Methode innerhalb der bestehenden Plugin-Struktur befanden und welche Zusammenhänge mit anderen Bestandteilen des Systems bestanden. Anschließend führte ich die erforderlichen Änderungen durch und passte die entsprechenden Code-Stellen an.
Die Aufgabe erforderte ein Verständnis der Struktur von Apache OFBiz und der Abhängigkeiten zwischen den einzelnen Plugins. Nach Abschluss der Anpassungen übertrug ich meine Änderungen in das Repository.
Im Zusammenhang mit dieser Aufgabe fand außerdem ein Meeting mit Projektleiter statt, in dem er mir weitere Informationen zu ecomify Suite erklärte. Dadurch erhielt ich zusätzliche Einblicke in das Projekt und dessen Aufbau.

## Verbesserung der Wartbarkeit durch Anpassung hardcodierter Werte

Eine weitere Aufgabe bestand darin, bestimmte hardcodierte Werte im bestehenden Code so anzupassen, dass sie einfacher verändert werden können. Hardcodierte Werte sind direkt im Programmcode hinterlegte Angaben. Werden solche Werte an mehreren Stellen verwendet, können spätere Änderungen aufwendiger sein, da die entsprechenden Stellen einzeln gefunden und angepasst werden müssen.
Um die Wartbarkeit des Codes zu verbessern, definierte ich für die betreffenden Werte Variablen und passte den vorhandenen Code entsprechend an. Dadurch sollten Änderungen an diesen Werten einfacher möglich sein, ohne dass dafür jedes Mal mehrere Stellen im Programmcode bearbeitet werden müssen.
Bei der Umsetzung musste ich zunächst die betroffenen Code-Stellen nachvollziehen und erkennen, welche Werte angepasst werden sollten. Anschließend nahm ich die Änderungen vor und überprüfte den angepassten Code.
Durch diese Aufgabe lernte ich, wie bereits kleine strukturelle Anpassungen dazu beitragen können, die Wartbarkeit und Übersichtlichkeit eines Programms zu verbessern.

## Hinterlegen von AGB-Inhalten und englischen Übersetzungen

Eine weitere Aufgabe wurde mir ebenfalls vom Projektleiter zugewiesen. Dabei sollte ich Inhalte aus einer vorgegebenen Datei als AGB-Content hinterlegen. Zusätzlich sollten die jeweiligen Inhalte um englische Übersetzungen ergänzt werden.
Zunächst beschäftigte ich mich mit den bereitgestellten Inhalten und übernahm die entsprechenden Daten in die dafür vorgesehene Struktur. Anschließend ergänzte ich die englischen Übersetzungen der jeweiligen Inhalte.
Bei dieser Aufgabe war es wichtig, die vorgegebenen Inhalte korrekt zu übernehmen und darauf zu achten, dass die deutschen und englischen Inhalte einander zugeordnet werden können. Nach der Bearbeitung übertrug ich die Änderungen auf einen Feature-Branch im Git-Repository.

## Aufbau einer wissenschaftlichen Arbeit

Bitte lesen Sie den online frei verfügbaren Text zum wissenschaftlichen Arbeiten von @Balzert2022 durch.


## Markdown und -Erweiterungen durch Pandoc

Für eine Einführung in (Pandoc-) Markdown vgl. [pandoc.org/MANUAL.html](https://pandoc.org/MANUAL.html).

Da als Backend \LaTeX{} zum Einsatz kommt, können alle entsprechenden Befehle und Umgebungen ebenfalls
genutzt werden (ggf. muss noch das jeweilige Paket importiert werden).

**Tipp**: Für eine schnelle Übersicht einfach den Quelltext dieser Datei ansehen ([thesis.md](./thesis.md)).


## Zitieren

Einfach den Bibtex-Key mit einem `@` davor in eckigen Klammern schreiben: Aus `[@Dietz2018]` wird [@Dietz2018] ...
Mit Seiten- oder Kapitelangabe: Aus `[@Dietz2018, Seite 111]` oder `[@Dietz2018, Kapitel 111]` wird
[@Dietz2018, Seite 111] oder [@Dietz2018, Kapitel 111] ...

Pandoc (bzw. `pandoc-citeproc`) nutzt per Default den *Chicago Manual of Style*-Stil^[vgl.
[pandoc.org/MANUAL.html#citations](https://pandoc.org/MANUAL.html#citations)].
Für andere Zitierstile (etwa numerisch oder als Fußnote) sind auf [zotero.org/styles](https://www.zotero.org/styles)
die passenden CSL-Dateien zum Download zu finden. Die Aktivierung erfolgt über die Option
`--csl=XXX.csl` in der Datei `Makefile`.

**Tipp**: Unter [editor.citationstyles.org/searchByName/](https://editor.citationstyles.org/searchByName/)
können Sie sich die Wirkung der jeweiligen Zitierstile/CSL-Definitionen anschauen.


## Abbildungen

![Hier steht die Bildunterschrift, Quelle: [@Dietz2018] \label{fig:foo}](figs/wuppie.png){width=80%}


## Source-Code

```{.python caption="The preprocessing step, cf. [@Dietz2018]" #lst:huh}
def foo():
  """ Wuppie! """
  pass
```

## Mathe

Display-Math geht wie in \LaTeX{} mit einem doppelten Dollarzeichen (entspricht der `equation`-Umgebung):

$$
    \label{eq:wuppie}
    \nabla E(\mathbf{w}) = \left( \frac{\partial E}{\partial w_{0}}, \frac{\partial E}{\partial w_{1}}, \ldots, \frac{\partial E}{\partial w_{n}} \right)^T
$$

Inline-Math geht mit einem einfachen Dollar-Zeichen: $\mathbf{w} \gets \mathbf{w} + \Delta\mathbf{w}$ ...


## Tabellen

| Rechtsbündig | Linksbündig | Default | Zentriert |
|-------------:|:------------|---------|:---------:|
|          foo | foo         | foo     |    foo    |
|          123 | 123         | 123     |    123    |
|          bar | bar         | bar     |    bar    |

: Tabelle als Markdown-Pipe-Table, vgl. [@Dietz2018] \label{tab:ugh}


Leider gibt es derzeit einen Bug (siehe [github.com/Wandmalfarbe/pandoc-latex-template/issues/29](https://github.com/Wandmalfarbe/pandoc-latex-template/issues/29)
bzw. [github.com/jgm/pandoc/issues/3929](https://github.com/jgm/pandoc/issues/3929)), wodurch die Breite beim Einfärben der
Tabellenzeilen etwas zu breit wird. Wenn das stört, kann man immer noch normale \LaTeX{}-Tabellen nutzen (siehe
Tabelle \ref{tab:ieks}).

\begin{longtable}[]{rllc}
\caption{Tabelle als \LaTeX{}-Table \label{tab:ieks}} \\
\toprule
Rechtsbündig & Linksbündig & Default & Zentriert \tabularnewline
\midrule
\endhead
foo & foo & foo & foo \tabularnewline
123 & 123 & 123 & 123 \tabularnewline
bar & bar & bar & bar \tabularnewline
\bottomrule
\end{longtable}


## Querverweise

Querverweise funktionieren in Markdown leider nicht so richtig wie von \LaTeX{} gewohnt.

Hier kann aber einfach auf die entsprechenden \LaTeX{}-Pendants ausgewichen werden:

*   Definieren einer Referenz mit `\label{<id>}`{.latex} (beispielsweise in den jeweiligen Unterschriften
    unter einer Abbildung/Tabelle/Code-Schnipsel), und
*   Bezugnahme auf eine Referenz im Text mit `\ref{<id>}`{.latex}.

Vgl. Abbildung \ref{fig:foo} oder Tabelle \ref{tab:ugh} oder Listing \ref{lst:huh} ...

Wer mehr braucht, kann sogenannte Filter^[vgl. [pandoc.org/filters.html](https://pandoc.org/filters.html)
bzw. [pandoc.org/lua-filters.html](https://pandoc.org/lua-filters.html)] einsetzen, beispielsweise
[github.com/lierdakil/pandoc-crossref](https://github.com/lierdakil/pandoc-crossref).





# Stand der Technik/Forschung, vergleichbare Arbeiten

*   Darstellung relevanter Ansätze aus der Praxis bzw. Forschung
*   Einordnung und Bewertung der Konzepte und Lösungen in Bezug auf die Ziele der Arbeit

Umfang: typisch ca. 15% ... 20% der Arbeit





# Eigene Ideen, Konzepte, Methoden

*   Darstellung der eigenen Ideen und Konzepte zur Lösung der Fragestellung
*   Vergleich mit bekannten Lösungen: Worin unterscheiden sich die eigenen Ansätze von den bekannten? Wo liegen mögliche Vor- oder Nachteile?
*   Wie soll das Konzept umgesetzt werden? Beschreibung der zur Umsetzung eingesetzten Methoden

Umfang: typisch ca. 20% ... 30% der Arbeit





# Realisierung, Evaluation

*   Beschreibung der Umsetzung des Lösungskonzepts
*   Darstellung der aufgetretenen Probleme sowie deren Lösung bzw. daraus resultierende Einschränkungen des Ergebnisses (falls keine Lösung)
*   Auswertung und Interpretation der Ergebnisse
*   Vergleich mit der ursprünglichen Zielsetzung (ausführlich): Was wurde erreicht, was nicht (und warum)? (inkl. Begründung/Nachweis)

Umfang: typisch ca. 30% ... 40% der Arbeit





# Zusammenfassung

*   Fazit: Vergleich mit der ursprünglichen Zielsetzung (komprimiert/zusammengefasst)
*   Ausblick: Darstellung ungelöster Probleme und weiterer relevanter Ideen

Umfang: typisch ca. 5% ... 10% der Arbeit


## Fazit

Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


## Ausblick

Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquid ex ea commodi consequat. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.





<!-- ==============  DO NOT EDIT THE SECTION BELOW  ============== -->

# Quellen {.unnumbered}

\markboth{Quellen}{Quellen}

<!--
References are automatically generated from the BibTex file (references.bib)
... which you should create/maintain using a reference manager.
-->

::: {#refs}
:::


\appendix

<!-- ==============  DO NOT EDIT THE SECTION ABOVE  ============== -->





# Appendix 1: Some extra stuff

Platz für *wichtige* Materialien, die zu umfangreich für den eigentlichen Textteil sind.

Der Anhang gehört *nicht* zum Textteil (wird nicht zum Seitenumfang hinzugerechnet).
Der Umfang des Anhangs sollte möglichst klein sein!


## Bilder

wuppie!

## Code

fluppie?

## Tabellen

foo! bar!

# Wuppie
