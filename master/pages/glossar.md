---
document_id: "university_computer_science_de:glossar"
series_id: "university_computer_science_de:M1-L1"
series_part: 57
document_version: "0.1.0"
created: "2026-11-12"
updated: "2026-11-12"
title: "Glossar – Informatik"
author: "Stephan Kühn"
document_type: "Begleitdokument"
project_name: "Learning Courses"
course: "informatik"
language: "de"
group: "Begleitmaterial"
study_level: "Hochschulstudium (Begleitmaterial)"
study_role: "Informatikbegriffe nachschlagen"
categories: ["Bildung/Lernkurse", "Begleitmaterial/Informatik"]
keywords: ["Informatik", "Begleitmaterial", "Informatikbegriffe nachschlagen"]
website: "https://monowlith.com"
github: "https://github.com/monowlith-com/learning-courses-university-computer-science-de"
license: "CC BY-NC-SA 4.0 International"
---

# Glossar – Informatik

  Begriff                  Einordnung                                                        Wesentliche Grenze
  ------------------------ ----------------------------------------------------------------- -------------------------------------------------------------------------------
  Retrieval-Berechtigung   Autorisierter Zugriff auf passende Quellen bei RAG                Ein semantischer Treffer oder veralteter Cache erteilt keine Leseberechtigung
  KV-Cache                 Zwischenspeicher für Key-/Value-Repräsentationen früherer Token   Kontextlänge, KV-Köpfe, Präzision und Parallelität beeinflussen die Belegung
  C2PA                     Signierte, technisch prüfbare Herkunftsbehauptungen bei Medien    Signatur belegt nicht automatisch den Wahrheitsgehalt
  Artikel 50 AI Act        Rollenabhängige Transparenzpflichten für bestimmte KI-Systeme     Eng begrenzte Schonfrist zu Absatz 2 ist kein allgemeiner Aufschub

  Neuer/geschärfter Begriff   Kurzbedeutung                                                       Wichtigste Grenze
  --------------------------- ------------------------------------------------------------------- -----------------------------------------------------------------
  O-Notation                  Asymptotische obere Wachstumsgrenze                                 Nicht automatisch eine enge oder gemessene Laufzeit
  Θ-Notation                  Asymptotisch passende obere und untere Grenze                       Nur für die konkret analysierte Aufwandsfunktion
  Prüf-/Schreib-Race          Beide Teilnehmer sehen vor dem Schreiben denselben alten Zustand    Nur ein atomarer gemeinsamer Schutz verhindert den Doppeleffekt
  Externer Seiteneffekt       Zahlung, Nachricht oder Aktion außerhalb einer lokalen DB           Lokales `ROLLBACK` rollt ihn nicht automatisch zurück
  0-RTT                       Frühe Daten bei geeigneter Wiederaufnahme eines QUIC/TLS-Kontexts   Kann Replay-Risiken für fachliche Wirkungen bergen

## M7-L3 – Verteilte Systeme und Systemmodelle {#S1}

  Begriff                        Bedeutung                                        Kurzdefinition
  ------------------------------ ------------------------------------------------ ----------------------------------------------------------------------------------------------
  Verteiltes System              Mehrere unabhängig arbeitende Prozesse           Kommunikation, Teilausfälle und fehlende globale Sicht prägen Korrektheit
  Happened-before                Kausale Ereignisordnung                          Lokale Ausführung, Senden vor Empfang und Transitivität
  Lamport-Uhr                    Logische Zählerzeit                              Kausale Reihenfolge impliziert kleinere Zeitstempel; Umkehrung gilt nicht
  Vektoruhr                      Mehrkomponentiger logischer Zeitstempel          Erkennt unter dem Modell kausale Abhängigkeit bzw. Nebenläufigkeit
  Netzwerkpartition              Unterbrochene Kommunikation zwischen Gruppen     Verhindert unter Umständen sichere gemeinsame Entscheidung
  Safety / Liveness              Sicherheit / Fortschritt                         Nie etwas Verbotenes / unter Bedingungen irgendwann Fortschritt
  Timeout                        Ablauf einer Wartefrist                          Verdacht auf Störung, kein Nachweis des Serverausfalls
  Idempotenz                     Wiederholungsfeste fachliche Wirkung             Keine unerwünschten zusätzlichen Effekte bei identischer Anforderung
  Linearisierbarkeit             Starkes Konsistenzmodell                         Operationen erscheinen atomar zwischen Aufruf und Antwort mit Echtzeitordnung
  Kausale Konsistenz             Ordnung abhängiger Änderungen                    Kausale Vorgänger erscheinen vor ihren Wirkungen
  Eventual Consistency           Langfristige Konvergenz                          Bei ausbleibenden Änderungen und funktionierender Kommunikation kann Gleichstand entstehen
  Konsens                        Verteilte Einigung                               Gemeinsame Entscheidung unter definierten Fehlerannahmen
  Mehrheitsquorum                Mehrheit der stimmberechtigten Teilnehmer        Zwei Mehrheiten überschneiden sich; zusätzliche Protokollregeln nötig
  Raft                           Konsensprotokoll                                 Leader-Wahl, repliziertes Log und Sicherheitsregeln
  CAP-Theorem                    Grenze bei Netzpartitionen                       Unter den Modellannahmen nicht zugleich linearisierbar und überall verfügbar
  FLP-Ergebnis                   Unmöglichkeitsresultat                           Keine garantierte Terminierung deterministischen asynchronen Konsenses bei möglichem Ausfall
  CRDT                           Conflict-free Replicated Data Type               Datenstruktur zur konfliktarmen Konvergenz unter passenden Regeln
  Replizierte Zustandsmaschine   Gemeinsames Log und deterministische Anwendung   Gleiche Befehlsfolge erzeugt bei identischem Startzustand gleichen Zustand
  Fencing Token                  Abwehr veralteter Leiterbefugnis                 Übergeordnete Ressource verwirft Aktionen alter Leitungsepochen
  Backoff / Jitter               Wartezeit und Streuung bei Wiederholung          Begrenzt und verteilt Wiederholungsverkehr bei Störungen

## M7-L2 – Korrektheit, Berechenbarkeit und komplexe Verfahren {#S2}

  Begriff                          Bedeutung                                              Kurzdefinition
  -------------------------------- ------------------------------------------------------ --------------------------------------------------------------------------
  Spezifikation                    Präziser Verhaltensvertrag                             Definiert erwartete Ein- und Ausgaben sowie Voraussetzungen
  Vorbedingung / Nachbedingung     Precondition / Postcondition                           Vorher nötige Eigenschaft bzw. nachher garantierte Eigenschaft
  Hoare-Tripel                     `{P} C {Q}`                                            Formales Schema einer partiellen Korrektheitsaussage
  Partielle / totale Korrektheit   Richtig falls beendet / richtig und beendet            Terminierung ist zusätzlicher Nachweis
  Schleifeninvariante              Dauerhaft erhaltene Aussage                            Vor definierten Prüfpunkten jeder Iteration gültig
  Terminierungsmaß                 Wohlfundierte abnehmende Größe                         Begründet, warum eine Berechnung nicht endlos fortgesetzt wird
  Induktion                        Beweis über Basis und Schritt                          Begründet Aussagen für alle natürlichen Größen bzw. rekursive Strukturen
  Big O / Ω / Θ                    Obere / untere / enge asymptotische Schranke           Beschreiben Wachstum von Ressourcenbedarf
  Amortisierte Analyse             Durchschnitt über garantierte Operationsfolge          Kein empirisch gemessener Durchschnitt und keine Einzelzeit-Garantie
  Reduktion                        Problemumformung                                       Überträgt Lösbarkeit oder Härte bei festgelegtem Aufwand
  P / NP                           Polynomial lösbar / polynomial verifizierbar           Formale Komplexitätsklassen von Entscheidungsproblemen
  NP-vollständig                   NP und NP-schwer                                       Härte unter polynomialen Reduktionen; nicht gleich unentscheidbar
  Berechenbarkeit                  Prinzipielle algorithmische Lösbarkeit                 Unabhängig von realer Rechnergeschwindigkeit
  Halteproblem                     Allgemeine Terminierungsentscheidung                   Für beliebige Programme und Eingaben unentscheidbar
  Diagonalisierung                 Widerspruch durch Selbstbezug                          Klassische Methode zum Nachweis der Unentscheidbarkeit
  Safety / Liveness                Nie ein unerlaubter Zustand / irgendwann Fortschritt   Eigenschaften formaler Zustandsmodelle
  Model Checking                   Systematische Zustandsprüfung                          Durchsucht Ausführungen eines formal definierten Modells
  SAT / SMT                        Aussagenlogische / theoriebasierte Erfüllbarkeit       Formalwerkzeuge für bestimmte logische Formeln

## M7-L1 – Wissenschaftliche Informatik {#S3}

  Begriff                      Bedeutung                                 Kurzdefinition
  ---------------------------- ----------------------------------------- -------------------------------------------------------------------
  Wissenschaftliches Modell    Vereinfachte Systembeschreibung           Beantwortet bestimmte Fragen unter expliziten Annahmen
  Hypothese                    Prüfbare Vermutung                        Aussage, die durch geeignete Beobachtungen geprüft werden kann
  Operationalisierung          Messbare Definition                       Übersetzung eines abstrakten Begriffs in Indikatoren
  Baseline                     Vergleichsbasis                           Definierte Ausgangsvariante eines Versuchs
  Falsifizierbarkeit           Prinzip möglicher Widerlegung             Bestimmte denkbare Beobachtungen widersprechen der Hypothese
  Störgröße / Confounder       Alternativer Einfluss                     Kann eine scheinbare Ursache-Wirkung-Beziehung verzerren
  Randomisierung               Zufällige Zuweisung                       Soll systematische Verzerrungen im Versuchsplan vermindern
  Blocking                     Blockbildung                              Gruppierung vergleichbarer Versuchsbedingungen
  Korrelation / Kausalität     Zusammenhang / Ursache                    Gemeinsame Veränderung belegt nicht automatisch Ursache
  Validität                    Geltung einer Schlussfolgerung            Prüft, ob Messung und Aussage zur Forschungsfrage passen
  Verifikation / Validierung   Spezifikationsprüfung / Eignungsprüfung   Richtig gebaut versus das passende System gebaut
  Reproduzierbarkeit           Gleiches Verfahren und gleiche Daten      Konsistente rechnerische Ergebnisse unter definierten Bedingungen
  Replikation                  Neue Daten, vergleichbare Frage           Konsistente Ergebnisse einer eigenständigen Studie
  Generalisierbarkeit          Übertragbarkeit                           Ergebnis gilt in anderen Situationen oder Populationen
  Perzentil / p99              Verteilungsschwelle                       p99 bezeichnet näherungsweise die 99-%-Schwelle
  Konfidenzintervall           Statistisches Intervallschätzverfahren    Über viele Anwendungen mit definierter Überdeckungsrate
  p-Wert                       Statistik unter Nullhypothese             Keine Wahrscheinlichkeit für Wahrheit der Nullhypothese
  Artefakt                     Nachvollziehbares Forschungsprodukt       Z. B. Datensatz, Code, Messprotokoll oder Versuchsplan

## M10-L2 – Datenmodellierung und Datenbankabfragen vertieft {#S4}

  Begriff                    Bedeutung                                 Kurzdefinition
  -------------------------- ----------------------------------------- --------------------------------------------------------------------------
  Datenmodellierung          Fachliche Strukturierung                  Gegenstände, Beziehungen und Regeln als Daten beschreiben
  Entität / Attribut         Gegenstand / Eigenschaft                  Beispielsweise Video und dessen Titel
  Kardinalität               Anzahl erlaubter Beziehungen              1:1, 1:n, n:m; zusätzlich Optionalität beachten
  Primärschlüssel            Primary Key                               Eindeutige Kennung einer Tabellenzeile
  Fremdschlüssel             Foreign Key                               Verweis, dessen Zulässigkeit das DBMS prüfen kann
  Funktionale Abhängigkeit   Bestimmungsregel zwischen Attributen      `kanal_id` bestimmt beispielsweise den Kanalnamen
  1NF / 2NF / 3NF            Erste, zweite, dritte Normalform          Kriterien zur Reduktion ungünstiger Datenabhängigkeiten
  Anomalie                   Fehler durch ungünstige Datenstruktur     Einfüge-, Änderungs- oder Löschanomalie
  SQL                        Structured Query Language                 Deklarative Sprache für strukturierte Daten
  JOIN                       Tabellenverknüpfung                       Bildet Zeilenkombinationen nach einer Bedingung
  INNER / LEFT JOIN          Innere / linke äußere Verknüpfung         Nur Treffer beziehungsweise alle linken Zeilen
  Körnung                    Fachliche Ebene einer Ergebniszeile       Beispielsweise eine Zeile pro Video oder pro Tag-Zuordnung
  GROUP BY / HAVING          Gruppieren / Gruppen filtern              Aggregationen bilden und nach ihnen auswählen
  NULL                       Fehlender Datenwert                       Nicht gleich 0 oder leerer Zeichenkette; Dreiwertlogik beachten
  COALESCE                   Ersten nicht-nulligen Wert wählen         Beispielsweise fehlende Summe fachlich in 0 umwandeln
  CTE                        Common Table Expression                   Mit WITH benannte Teilabfrage innerhalb einer SQL-Anweisung
  Fensterfunktion            Window Function                           Berechnet Werte über Zeilengruppen ohne sie vollständig zusammenzufalten
  EXPLAIN                    Anzeige des Abfrageplans                  Zeigt den vom Datenbanksystem gewählten oder geplanten Ausführungsweg
  Selektivität               Wirkung eines Filters                     Anteil der Datensätze, die eine Bedingung erfüllt
  Lost Update                Verlorene Aktualisierung                  Zwei unkoordinierte Änderungen überschreiben einander
  Parametrisierte Abfrage    Werte getrennt von SQL-Syntax übergeben   Grundschutz gegen SQL-Injection
  Mandant / Tenant           Getrennte Kunden-/Nutzergruppe            Benötigt eindeutige Datenzuordnung und Rechte
  RLS                        Row-Level Security                        Datenbankseitige Zugriffskontrolle auf Zeilenebene
  Datenbankmigration         Struktur-/Datenänderung                   Geplante Versionierung und Umstellung eines Schemas
  Expand-and-Contract        Gestufte Schemamigration                  Neue und alte Strukturen vorübergehend kompatibel halten

## M10-L1 – Netzwerke und praktische IT-Sicherheit {#S5}

  Begriff             Bedeutung                                          Kurzdefinition
  ------------------- -------------------------------------------------- ------------------------------------------------------------------------------------------------
  CIDR                Classless Inter-Domain Routing                     Schreibt IP-Netze über Präfixlänge, etwa `/27`
  VLAN                Virtual Local Area Network                         Logische Trennung lokaler Netzsegmente
  NAT                 Network Address Translation                        Übersetzt IP-Adressinformationen; kein vollwertiger Sicherheitsschutz
  TCP / UDP / QUIC    Transportmechanismen                               Unterschiedliche Modelle für Verbindungs- und Datagrammkommunikation
  TLS 1.3             Transport Layer Security                           Protokoll zum Schutz des Transportkanals, seit Juli 2026 in RFC 9846 beschrieben
  DNSSEC              DNS Security Extensions                            Ermöglicht Authentizitäts-/Integritätsprüfungen von DNS-Daten, verschlüsselt die Abfrage nicht
  Least Privilege     Prinzip minimaler Rechte                           Jede Identität erhält nur die notwendigen Berechtigungen
  Default Deny        Standardmäßig verbieten                            Kommunikationswege nur nach definierter Erlaubnis öffnen
  Authentifizierung   Feststellung der Identität                         Prüft, wer beziehungsweise was sich anmeldet
  Autorisierung       Berechtigungsprüfung                               Prüft, was der angemeldete Akteur tatsächlich tun darf
  Passkey             Schlüsselbasierte Authentifizierung                Kann dienstgebunden und phishingresistent gestaltet sein
  OWASP Top 10:2025   Risikoübersicht für Webanwendungen                 Zehn Kategorien häufig relevanter Schwachstellenmuster
  Zero Trust          Zugriffsmodell ohne pauschales Netzwerkvertrauen   Ressource, Identität und Kontext einzeln prüfen
  Incident Response   Reaktion auf Sicherheitsvorfälle                   Vorfälle erkennen, eingrenzen, beheben und Betrieb wiederherstellen
  Restore-Test        Wiederherstellungsprobe                            Prüft, ob ein Backup praktisch verwendbar ist

## M8-L3 – Betriebssysteme und Nebenläufigkeit vertieft {#S6}

  Begriff                Bedeutung                                       Kurzdefinition
  ---------------------- ----------------------------------------------- ---------------------------------------------------------------------
  Prozess                Ausführungskontext eines Programms              Besitzt unter anderem einen virtuellen Adressraum und Ressourcen
  Thread                 Ausführungsfaden                                Vom Scheduler planbare Folge von Befehlen innerhalb eines Prozesses
  Nebenläufigkeit        Concurrency                                     Koordination zeitlich überlappender Tätigkeiten
  Parallelität           Parallelism                                     Tatsächlich gleichzeitige Berechnungen auf mehreren Recheneinheiten
  Scheduler              Betriebssystem-Planer                           Wählt ausführungsbereite Threads für CPU-Kerne
  Kontextwechsel         Context Switch                                  Sichert Zustand einer Ausführung und setzt eine andere fort
  EEVDF                  Earliest Eligible Virtual Deadline First        Fairer Linux-Schedulingansatz mit virtuellem Rückstand und Fristen
  Virtueller Speicher    Virtual Memory                                  Prozessbezogener Adressraum mit übersetzten Speicheradressen
  Page Fault             Seitenfehler-Ausnahme                           Meldung einer fehlenden oder unzulässigen Speicherzuordnung
  Page Cache             Zwischenspeicher für Datei-/Seiteninhalte       Vermeidet wiederholte langsame Dateizugriffe
  Swap / Pagefile        Auslagerung auf Massenspeicher                  Kann Speicherknappheit abfedern, ersetzt keinen RAM
  Race Condition         Zeitabhängiger Konkurrenzfehler                 Ergebnis hängt von unkoordinierten Zugriffen ab
  Mutex                  Mutual Exclusion                                Sperre für exklusiven Zugriff auf einen kritischen Bereich
  Semaphore              Zählendes Synchronisationsmittel                Begrenzt beispielsweise gleichzeitige Ressourcenzugriffe
  Atomic                 Unteilbar sichtbare Operation                   Für einzelne Datenänderungen; keine allgemeine Transaktion
  Deadlock               Verklemmung                                     Zyklische Warteabhängigkeit ohne Fortschritt
  Livelock               Aktive Blockade des Fortschritts                Beteiligte reagieren, erledigen aber nichts Nützliches
  Starvation             Dauerhafte Benachteiligung                      Aufgabe bekommt auf lange Sicht zu wenig Ressourcen
  Priority Inheritance   Prioritätsvererbung                             Sperrenbesitzer erhält vorübergehend wartende höhere Priorität
  IPC                    Interprocess Communication                      Datenaustausch zwischen eigenständigen Prozessen
  Amdahls Gesetz         Grenze paralleler Beschleunigung                Serielle Anteile begrenzen Gesamtspeedup
  PREEMPT_RT             Echtzeitfähige Linux-Preemption-Konfiguration   Verbessert zeitliches Verhalten in bestimmten Kernelpfaden

Begriffe sind hier als Einstieg definiert. Ausführliche Erklärungen stehen in den jeweils passenden Lektionen.

  Begriff                     Langform / Bedeutung                                            Kurzerklärung
  --------------------------- --------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------
  Formale Sprache             Menge zulässiger Wörter über einem Alphabet                     Präzise Definition aller erlaubten Zeichenfolgen
  Alphabet                    Endliche Menge von Symbolen                                     Grundbausteine einer formalen Sprache, z. B. `{0,1}`
  Reguläre Sprache            Mit endlichem Automaten erkennbare Sprache                      Typische Grundlage klassischer regulärer Ausdrücke
  DFA                         Deterministic Finite Automaton                                  Endlicher Automat mit eindeutigem Folgezustand je Zeichen
  NFA                         Nondeterministic Finite Automaton                               Endlicher Automat mit mehreren konzeptionell möglichen Folgezuständen
  Kellerautomat (PDA)         Pushdown Automaton                                              Zustandsmodell mit Stapelspeicher, etwa für Klammerung
  CFG                         Context-Free Grammar                                            Grammatik mit nichtterminalen Symbolen und Ableitungsregeln
  Lexer                       Lexikalischer Analysator                                        Gruppiert Zeichen zu Tokens
  Token                       Lexikalische Einheit                                            Beispielsweise Bezeichner, Zahl oder Rechenoperator
  Parser                      Syntaxanalysator                                                Prüft Tokenfolge anhand der Grammatik und bildet eine Struktur
  AST                         Abstract Syntax Tree                                            Abstrakter Syntaxbaum eines Ausdrucks oder Programms
  Symboltabelle               Namens- und Eigenschaftsverzeichnis                             Unterstützt Gültigkeitsbereichs- und Typprüfungen
  IR                          Intermediate Representation                                     Zwischenrepräsentation für Analyse, Optimierung und Zielcode
  Compiler                    Übersetzer von Programmdarstellungen                            Erzeugt z. B. Bytecode, IR oder Maschinencode
  AOT                         Ahead-of-Time Compilation                                       Übersetzt Programmteile vor ihrer späteren Ausführung
  Halteproblem                Allgemeines Entscheidungsproblem der Berechenbarkeit            Für beliebige Programme und Eingaben nicht universell entscheidbar
  Aussagenlogik               Logische Aussagen mit wahr/falsch                               Verknüpft Bedingungen durch UND, ODER, NICHT und Implikation
  Prädikatenlogik             Aussagen über Objekte                                           Formuliert Eigenschaften und Beziehungen mit Variablen und Quantoren
  Quantoren                   ∀ für alle, ∃ es existiert                                      Beschreiben die Geltung von Aussagen über Mengen von Objekten
  De-Morgan-Gesetze           Logische Umformungsregeln                                       Verknüpfen Negation mit UND bzw. ODER
  Menge                       Sammlung unterscheidbarer Elemente                              Zugehörigkeit zählt, nicht Reihenfolge oder Mehrfachvorkommen
  Schnittmenge                $A\cap B$                                                       Elemente, die sowohl in A als auch in B liegen
  Kartesisches Produkt        $A\times B$                                                     Menge aller geordneten Paare aus zwei Mengen
  Funktion                    Eindeutige Zuordnung für jeden zulässigen Eingang               Ordnet jeder Eingabe genau eine Ausgabe zu
  Relation                    Teilmenge eines kartesischen Produkts                           Beschreibt, welche geordneten Paare miteinander in Beziehung stehen
  Äquivalenzrelation          Reflexive, symmetrische und transitive Relation                 Teilt die Ausgangsmenge in Äquivalenzklassen
  Partielle Ordnung           Reflexive, antisymmetrische, transitive Relation                Ordnet Elemente, ohne alle Paare vergleichen zu müssen
  Induktion                   Mathematische Beweistechnik                                     Anfangsfall plus Übergang zu einem Nachfolger
  Graph                       Knoten und Kanten                                               Stellt Verbindungen, Netzwerke und Abhängigkeiten dar
  DAG                         Directed Acyclic Graph                                          Gerichteter Graph ohne gerichtete Zyklen
  BFS                         Breadth-First Search, Breitensuche                              Durchläuft Graphen schrittweise nach Kantenentfernung
  DFS                         Depth-First Search, Tiefensuche                                 Verfolgt Wege in einem Graphen und kehrt zu Alternativen zurück
  Adjazenzliste               Nachbarschaftsdarstellung eines Graphen                         Speichert zu jedem Knoten seine Nachbarn
  Kombinatorik                Zählen endlicher Möglichkeiten                                  Erklärt Permutationen, Kombinationen und Auswahlzahlen
  Modulo                      Rest der ganzzahligen Division                                  Gruppiert Zahlen nach Restklassen, z. B. beim Sharding
  Invariante                  Erhaltungsbedingung im Ablauf                                   Eigenschaft, die über definierte Zustandsübergänge wahr bleiben soll
  Algorithmus                 Eindeutig beschriebene schrittweise Vorgehensweise              Löst eine festgelegte Klasse von Aufgaben unter benannten Voraussetzungen
  Abstraktion                 Bewusst vereinfachtes Modell                                    Blendet für eine Fragestellung unwichtige Eigenschaften aus
  Berechenbarkeit             Entscheidbarkeit/Lösbarkeit durch algorithmische Verfahren      Nicht jedes formale Problem ist für alle Eingaben algorithmisch entscheidbar
  Informatik                  Wissenschaft der Darstellung und Verarbeitung von Information   Behandelt Modelle, Algorithmen, Systeme und ihre Grenzen
  ISA                         Instruction Set Architecture                                    Für Software sichtbarer Befehlssatz-/Register-Vertrag einer Prozessorfamilie
  ALU                         Arithmetic Logic Unit                                           Rechen- und Logikschaltung innerhalb eines Prozessors
  JIT                         Just-in-Time Compilation                                        Übersetzt Code während der Ausführung in Maschinenbefehle
  Virtueller Speicher         Virtual Memory                                                  Virtueller Adressraum und Abbildung auf physische Speicher; nicht mit Swap gleichzusetzen
  API                         Application Programming Interface                               Definierte Programmschnittstelle
  CPU                         Central Processing Unit                                         Allgemeiner Hauptprozessor
  GPU                         Graphics Processing Unit                                        Besonders für viele parallele Rechenoperationen geeigneter Prozessor
  RAM                         Random Access Memory                                            Flüchtiger Arbeitsspeicher
  SSD                         Solid State Drive                                               Dauerhafter Flash-Massenspeicher
  DNS                         Domain Name System                                              Auflösung von Domainnamen in Netzwerkadressen u. a.
  TCP                         Transmission Control Protocol                                   Zuverlässiger Transportprotokollmechanismus in IP-Netzen
  IP                          Internet Protocol                                               Adressierung und Weiterleitung von Netzwerkpaketen
  TLS                         Transport Layer Security                                        Kryptografisch abgesicherte Transportverbindung
  HTTP                        Hypertext Transfer Protocol                                     Protokoll für Webkommunikation
  VPS                         Virtual Private Server                                          Virtueller gemieteter Server
  VM                          Virtual Machine                                                 Virtuelle Maschine mit eigenem Gastbetriebssystem
  VPC                         Virtual Private Cloud                                           Logisch isolierter Cloud-Netzwerkbereich
  IAM                         Identity and Access Management                                  Identitäts- und Berechtigungsverwaltung
  CDN                         Content Delivery Network                                        Verteilte Auslieferung von Inhalten
  CI/CD                       Continuous Integration / Continuous Delivery oder Deployment    Automatisiertes Integrieren und Bereitstellen von Software
  IaaS                        Infrastructure as a Service                                     Gemietete Infrastrukturressourcen
  PaaS                        Platform as a Service                                           Verwaltete Plattform für eigene Anwendungen
  SaaS                        Software as a Service                                           Nutzung fertiger Software als Online-Dienst
  SQL                         Structured Query Language                                       Abfrage- und Verarbeitungssprache relationaler Daten
  NoSQL                       Not Only SQL (übliche Lesart)                                   Sammelbegriff für mehrere nichtklassisch-relationale Datenbankmodelle
  ACID                        Atomicity, Consistency, Isolation, Durability                   Grundlegende Transaktionseigenschaften
  RPO                         Recovery Point Objective                                        Ziel für maximal akzeptablen Datenverlustzeitraum
  RTO                         Recovery Time Objective                                         Ziel für maximal akzeptable Wiederanlaufzeit
  SLA                         Service Level Agreement                                         Vertragliche Dienstgüte-Zusage
  SLO                         Service Level Objective                                         Internes oder dokumentiertes Dienstgüte-Ziel
  IaC                         Infrastructure as Code                                          Infrastruktur in überprüfbarer maschinenlesbarer Beschreibung
  MFA                         Multi-Factor Authentication                                     Anmeldung mit mehreren unabhängigen Faktoren
  REST                        Representational State Transfer                                 Architekturstil für vernetzte Anwendungen
  NAT                         Network Address Translation                                     Umsetzung von Netzwerkadressen
  CAP                         Consistency, Availability, Partition tolerance                  Aussage über Zielkonflikte unter Netzpartitionen in bestimmten verteilten Systemmodellen
  ROS 2                       Robot Operating System 2                                        Middleware- und Werkzeugökosystem für Robotik
  Array                       Feld mit über Positionsnummern erreichbaren Einträgen           Direkter Indexzugriff typischerweise $O(1)$
  Verkettete Liste            Linked List                                                     Folge von Knoten, die auf weitere Knoten verweisen
  Hash-Tabelle                Hash Table                                                      Datenstruktur für schnellen schlüsselbasierten Zugriff bei geeigneter Verteilung
  Binäre Suche                Binary Search                                                   Halbierung des Suchbereichs in geordneter, direkt zugreifbarer Struktur
  Baum / Suchbaum             Tree / Search Tree                                              Hierarchische Datenstruktur; balancierte Suchbäume oft $O(\log n)$
  Graph                       Graph                                                           Knoten und Kanten zur Darstellung von Beziehungen
  BFS                         Breadth-First Search                                            Breitensuche, durchläuft Graphen schichtweise
  DFS                         Depth-First Search                                              Tiefensuche, untersucht Pfade zunächst in die Tiefe
  LIFO                        Last In, First Out                                              Zuletzt eingelegt, zuerst entnommen – Stack
  FIFO                        First In, First Out                                             Zuerst eingelegt, zuerst entnommen – Queue
  Stack                       Stapel                                                          Datenstruktur nach LIFO-Prinzip
  Queue                       Warteschlange                                                   Datenstruktur nach FIFO-Prinzip
  Rekursion                   Recursion                                                       Beschreibung eines Problems durch kleinere Instanzen desselben Problems
  Memoisierung                Memoization                                                     Zwischenspeicherung bereits berechneter Teilergebnisse
  Dynamische Programmierung   Dynamic Programming                                             Wiederverwendung überlappender Teilproblemlösungen
  Greedy                      Gieriges Verfahren                                              Lokale Entscheidungen, deren globale Optimalität separat geprüft werden muss
  Big O / O-Notation          asymptotische obere Schranke                                    Beschreibt eine Wachstumsgrenze für Rechen-/Speicheraufwand
  NP-schwer                   NP-hard                                                         Klasse mindestens so schwieriger Probleme wie die schwersten Probleme in NP; nicht gleichbedeutend mit unberechenbar

  Begriff                     Bedeutung                                              Einordnung
  --------------------------- ------------------------------------------------------ -------------------------------------------------------------------------------------
  Modul                       Softwarebaustein mit klar abgegrenzter Zuständigkeit   Macht Änderungen und Tests überschaubarer
  Kohäsion                    Innerer Zusammenhalt eines Moduls                      Wie eng Aufgaben eines Moduls fachlich zusammengehören
  Kopplung                    Abhängigkeiten zwischen Softwarebausteinen             Geringere unnötige Kopplung erleichtert Änderungen
  Kapselung                   Encapsulation                                          Abschirmung interner Zustände hinter definierten Operationen
  Schichtenarchitektur        Layered Architecture                                   Trennung zum Beispiel von Darstellung, Fachlogik und Datenzugriff
  Contract                    Schnittstellenvertrag                                  Festgelegte Ein-/Ausgaben und Fehler einer Schnittstelle
  JSON                        JavaScript Object Notation                             Textformat für strukturierte Daten
  XML                         Extensible Markup Language                             Erweiterbare Auszeichnungssprache für strukturierte Daten
  CSV                         Comma-Separated Values                                 Zeilenbasiertes Tabellenformat
  Zustandsautomat             State Machine                                          Modell erlaubter Zustände und Übergänge
  Event-Driven Architecture   Ereignisgesteuerte Architektur                         Verarbeitung reagiert auf gemeldete Ereignisse
  Unit-Test                   Komponententest                                        Prüft eine kleine, abgegrenzte Funktionseinheit
  Integrationstest            Integration Test                                       Prüft Zusammenspiel mehrerer Komponenten
  E2E                         End to End                                             Durchgängige Prüfung eines vollständigen Nutzerablaufs
  Regressionstest             Regression Test                                        Prüft, ob Änderungen bestehendes Verhalten beschädigen
  Git                         Verteiltes Versionsverwaltungssystem                   Verwaltet nachvollziehbare Dateiversionen
  Commit                      Versionsverwaltungs-Eintrag                            Speichert nachvollziehbaren Änderungsstand
  Branch                      Entwicklungszweig                                      Erlaubt isolierte Änderungsvarianten
  CI                          Continuous Integration                                 Häufiges Zusammenführen und automatisiertes Prüfen von Änderungen
  CD (Delivery)               Continuous Delivery                                    Geprüfte Software ist zur Veröffentlichung bereit
  CD (Deployment)             Continuous Deployment                                  Automatische Produktivbereitstellung bestandener Änderungen
  Build                       Softwarebau                                            Erzeugt aus Quellcode ein nutzbares Programm-/Paketartefakt
  Monolith                    Zusammenhängend bereitgestellte Anwendung              Kann intern sauber in Module gegliedert sein
  Microservices               Eigenständig bereitstellbare Dienste                   Erlauben unabhängigen Betrieb, erhöhen aber Verteilungskomplexität
  Technische Schulden         Technical Debt                                         Heute eingesparte Arbeit kann spätere Änderungen verteuern
  Authentifizierung           Authentication                                         Prüft, wer ein Nutzer ist
  Autorisierung               Authorization                                          Prüft, was ein Nutzer tun darf
  Least Privilege             Prinzip der geringsten Rechte                          Vergibt nur notwendige Berechtigungen
  OWASP                       Open Worldwide Application Security Project            Sicherheitsprojekt mit Entwicklungshilfen und Prüfleitfäden
  DBMS                        Datenbankmanagementsystem                              Software, die eine Datenbank verwaltet, Abfragen ausführt und Regeln kontrolliert
  Datenbank-Schema            Schema                                                 Definition von Tabellen, Datentypen, Beziehungen und Integritätsregeln
  Primärschlüssel             Primary Key                                            Eindeutige Kennung eines Datensatzes innerhalb einer Tabelle
  Fremdschlüssel              Foreign Key                                            Verweis auf eine passende eindeutige Kennung einer verknüpften Tabelle
  Referenzielle Integrität    Referential Integrity                                  Sicherstellung gültiger Verweise zwischen Tabellen
  JOIN                        Verknüpfung relationaler Tabellen                      Kombiniert Zeilen anhand passender Beziehungen
  Normalisierung              Normalization                                          Modellierung zur Verringerung unnötiger Datenwiederholungen und Änderungsprobleme
  Denormalisierung            Denormalization                                        Absichtliche Speicherung abgeleiteter oder redundanter Werte für bestimmte Zugriffe
  Index                       Datenbankindex                                         Zusatzstruktur zur Beschleunigung geeigneter Such- oder Sortieranfragen
  Query Planner               Abfrageplaner                                          Wählt einen Ausführungsweg für eine Datenbankabfrage
  Transaktion                 Transaction                                            Zusammengehörige Änderungen, die als Einheit gesteuert werden
  COMMIT / ROLLBACK           Bestätigen / Zurücknehmen                              Abschließen oder Rückgängigmachen einer Transaktion
  MVCC                        Multi-Version Concurrency Control                      Versionsbasierte Kontrolle nebenläufiger Datenbankzugriffe
  WAL                         Write-Ahead Log                                        Vorabprotokoll, das zur Wiederherstellung und Transaktionssicherung beitragen kann
  Dokumentendatenbank         Document Database                                      Speichert Dokumente mit flexiblen Feldern und Unterstrukturen
  Schlüssel–Wert-Speicher     Key–Value Store                                        Datenhaltung mit direkter Zuordnung von Schlüsseln zu Werten
  SQLite                      Eingebettetes relationales Datenbanksystem             Meist lokale Datenbankdatei ohne separaten DBMS-Server
  PostgreSQL                  Relationales Client-Server-DBMS                        Eigenständiger Datenbankserver mit umfangreichen Integritäts- und Abfragefunktionen

  Begriff                      Bedeutung                          Einordnung
  ---------------------------- ---------------------------------- ----------------------------------------------------------------------
  IPv4                         Internet Protocol Version 4        32-Bit-IP-Adressfamilie
  IPv6                         Internet Protocol Version 6        128-Bit-IP-Adressfamilie
  DNS-Resolver                 DNS-Auflösungsdienst               Ermittelt Adressinformationen zu Namen
  A / AAAA                     DNS Resource Record Types          A für IPv4-, AAAA für IPv6-Adressen
  Router                       Netzwerkvermittler                 Leitet Pakete in Richtung anderer Netze
  NAT                          Network Address Translation        Übersetzt Netzwerkadressen und häufig Ports
  Port                         Logischer Kommunikationsendpunkt   Hilft, Verbindungen einem Dienst zuzuordnen
  UDP                          User Datagram Protocol             Transport von Datagrammen ohne eingebaute Zustellgarantie
  QUIC                         Transportprotokoll auf UDP-Basis   Grundlage von HTTP/3, mit verschlüsselten Verbindungen und Streams
  HTTP                         Hypertext Transfer Protocol        Protokoll für Web-Anfragen und -Antworten
  HTTPS                        HTTP über TLS                      HTTP-Verbindung mit kryptografischem Transportschutz
  TLS-Handshake                Aushandlung einer TLS-Verbindung   Vereinbart Sicherheitsparameter und Sitzungsschlüssel
  RFC                          Request for Comments               Technische Dokumentenreihe, unter anderem für Internetstandards
  OSI                          Open Systems Interconnection       Konzeptionelles Netzwerk-Schichtenmodell
  CA                           Certificate Authority              Zertifizierungsstelle für digitale Zertifikate
  Zertifikat                   Digitales Zertifikat               Ordnet einen öffentlichen Schlüssel einer geprüften Identität zu
  Hashfunktion                 Kryptografische Prüffunktion       Berechnet einen nicht einfach umkehrbaren Fingerabdruck
  Salt                         Zufälliger Zusatzwert              Trennt Passwort-Hashberechnungen verschiedener Benutzer
  Argon2id                     Passwort-Hashverfahren             Geeignet für aufwendige, gesalzene Passwort-Hashberechnung
  Symmetrische Kryptografie    Shared-Key-Kryptografie            Beide Partner verwenden denselben geheimen Schlüssel
  Asymmetrische Kryptografie   Public-Key-Kryptografie            Öffentlicher und privater Schlüssel für unterschiedliche Verfahren
  Firewall                     Netzwerk-Zugriffskontrolle         Filtert erlaubten und unerlaubten Netzwerkverkehr
  Bedrohungsmodell             Threat Model                       Betrachtung von Schutzgütern, Angriffen und möglichen Gegenmaßnahmen
  Deny by Default              Standardmäßig verweigern           Zugriff wird nur bei ausdrücklicher Erlaubnis gewährt
  Session                      Sitzung                            Zuordnung mehrerer Anfragen zu einem Nutzer bzw. Vorgang
  Zugangstoken                 Access Token                       Berechtigungsnachweis für bestimmte Zugriffe

Das Glossar erklärt Fachbegriffe über alle Kurskapitel hinweg. Die genaue Bedeutung richtet sich nach dem Kontext der jeweiligen Lektion.

## Künstliche Intelligenz und Robotik (Module M5 und M6) {#S7}

- **KI (Künstliche Intelligenz):** Oberbegriff für Verfahren, die Aufgaben bearbeiten, die als intelligent gelten, beispielsweise Mustererkennung, Sprachverarbeitung oder Planung.
- **ML (Machine Learning, maschinelles Lernen):** Verfahren, die aus Daten bzw. Erfahrungen Muster oder Regeln ableiten statt jede Regel einzeln zu programmieren.
- **Deep Learning (tiefes Lernen):** maschinelles Lernen mit mehrschichtigen neuronalen Netzen.
- **Neuronales Netz:** mathematisches System gewichteter Verbindungen, dessen Parameter durch Lernen angepasst werden.
- **Parameter / Gewicht:** anpassbare Zahl in einem Modell, die seine Berechnung beeinflusst.
- **Backpropagation (Fehlerrückpropagation):** Berechnung des Einflusses einzelner Parameter auf einen Fehlerwert, um Gewichte effizient anzupassen.
- **Transformer:** seit 2017 einflussreiche neuronale Architektur mit Attention-Mechanismen zur Verarbeitung von Sequenzen.
- **Attention (Aufmerksamkeit):** Mechanismus, der berechnet, welche Teile einer Eingabe für andere Teile bei einer Verarbeitung relevant sind.
- **LLM (Large Language Model):** großes Sprachmodell, das sprachliche Muster aus umfangreichen Trainingsdaten gelernt hat; viele heutige Modelle erzeugen Text Token für Token.
- **Token:** Verarbeitungseinheit eines Sprachmodells; kann Wort, Wortteil, Zeichen oder Sonderzeichen repräsentieren.
- **Embedding:** numerischer Vektor, der bestimmte Eigenschaften von Text, Bild oder anderen Daten darstellt.
- **Inferenz:** Ausführung eines bereits trainierten Modells zur Erzeugung einer Ausgabe oder Vorhersage.
- **Fine-Tuning:** nachgelagerte Anpassung eines vortrainierten Modells mit zusätzlichen Trainingsdaten.
- **RAG (Retrieval-Augmented Generation):** Einbinden extern gefundener Informationen in die Erzeugung einer Modellantwort.
- **RLHF (Reinforcement Learning from Human Feedback):** Training anhand menschlicher Präferenzurteile als Belohnungssignal.
- **Agent:** Softwaresystem, das ein Modell für die Auswahl oder Durchführung mehrerer Arbeitsschritte und Werkzeugaufrufe verwenden kann.
- **ROS 2 (Robot Operating System 2):** Middleware-Ökosystem zur Kommunikation und Strukturierung von Robotiksoftware, kein vollständiges klassisches Betriebssystem.
- **SLAM (Simultaneous Localization and Mapping):** gleichzeitige Positionsbestimmung und Erstellung einer Umgebungskarte.
- **Edge Computing:** Verarbeitung nahe am Gerät statt zwingend in einer entfernten Cloud.

## Ergänzungen aus M1-L7 – weiterführende Grundlagen {#S8}

  Begriff                Langform / Bedeutung                          Kurzerklärung
  ---------------------- --------------------------------------------- -------------------------------------------------------------------------------------
  Nebenläufigkeit        Concurrency                                   Mehrere Aufgaben können in überlappenden Zeiträumen Fortschritte machen
  Parallelität           Parallelism                                   Mehrere Berechnungen finden tatsächlich gleichzeitig statt
  Thread                 Ausführungsstrang innerhalb eines Prozesses   Kann Speicher und Ressourcen mit anderen Threads desselben Prozesses teilen
  Asynchronität          Asynchronous execution                        Auf langwierige Operationen reagieren, ohne zwingend bis zum Ergebnis zu blockieren
  Race Condition         Wettlaufsituation                             Ergebnis hängt von der Reihenfolge konkurrierender Zugriffe ab
  Mutex                  Mutual Exclusion                              Sperre für gegenseitigen Ausschluss beim Zugriff auf gemeinsam genutzte Daten
  Atomare Operation      Atomic Operation                              Gegenüber konkurrierenden Zugriffen unteilbar wirkender Schritt
  Deadlock               Verklemmung                                   Aufgaben warten zyklisch aufeinander und kommen nicht weiter
  Starvation             Verhungern einer Aufgabe                      Eine Aufgabe bekommt über längere Zeit keine benötigte Ressource
  Livelock               Lebendverklemmung                             Aufgaben reagieren ständig aufeinander, ohne Fortschritt zu erzielen
  Formale Sprache        Formal Language                               Menge von Zeichenfolgen, die bestimmten Regeln entsprechen
  Grammatik              Grammar                                       Regeln für den Aufbau gültiger Ausdrücke
  Parser                 Syntaxanalysator                              Ordnet Token einer grammatischen Struktur zu
  Token (Compiler)       Sprachliche Einheit                           Erkannter Bezeichner, Operator, Literal oder ähnlicher Baustein
  Regex                  Regular Expression                            Musterbeschreibung zur Erkennung und Verarbeitung von Zeichenfolgen
  Verteiltes System      Distributed System                            Mehrere eigenständige Rechner/Prozesse arbeiten über Nachrichten zusammen
  Idempotenz             Idempotence                                   Wiederholte Ausführung hat keine unerwünschte zusätzliche Wirkung
  Logische Uhr           Logical Clock                                 Verfahren zur Beschreibung einer Ereignisreihenfolge ohne perfekte Echtzeituhr
  Eventual Consistency   Letztendliche Konsistenz                      Kopien können unter bestimmten Voraussetzungen zeitverzögert übereinstimmen
  Konsensverfahren       Consensus Algorithm                           Verfahren für gemeinsame Entscheidungen mehrerer Knoten unter definierten Annahmen
  HCI                    Human-Computer Interaction                    Mensch-Computer-Interaktion, untersucht Gestaltung und Nutzung digitaler Systeme
  WCAG                   Web Content Accessibility Guidelines          Leitlinien zur Zugänglichkeit von Webinhalten
  W3C                    World Wide Web Consortium                     Standardisierungsgremium für Webtechnologien
  DSGVO                  Datenschutz-Grundverordnung                   EU-Rechtsrahmen für die Verarbeitung personenbezogener Daten
  Privacy by Design      Datenschutz durch Technikgestaltung           Datenschutz schon bei Planung und Entwurf berücksichtigen
  ML                     Machine Learning                              Verfahren des maschinellen Lernens aus Daten oder Rückmeldungen
  Overfitting            Überanpassung                                 Modell passt zu Trainingsbeispielen, verallgemeinert aber schlecht

## Ergänzungen aus M2-L1 – Server, Hosting und Erreichbarkeit {#S9}

  Begriff                Langform / Bedeutung                              Kurzerklärung
  ---------------------- ------------------------------------------------- ------------------------------------------------------------------------------------------------------------------
  Server (Rolle)         Netzwerkdienst                                    Programm, das Anfragen anderer Programme annimmt und beantwortet
  Client                 Anfragendes Programm                              Browser oder andere Software, die einen Dienst nutzt
  Loopback / localhost   Eigener Rechner als Netzwerkziel                  Zugriff auf einen Dienst desselben Computers, häufig über `127.0.0.1`
  Hintergrunddienst      Service / Daemon                                  Programm, das ohne sichtbares Fenster dauerhaft oder bei Bedarf läuft
  Shared Hosting         Geteilte Hostingplattform                         Anbieter betreibt gemeinsam verwendete Serverumgebung mit vorgegebenen Funktionen
  VPS                    Virtual Private Server                            Virtueller Rechner mit weitgehend eigener Betriebssystemumgebung
  Dedizierter Server     Dedicated Server                                  Einem Kunden zugeordneter physischer Server
  Managed Hosting        Vom Anbieter mitbetreuter Dienst                  Vertragsmodell mit zusätzlichen Betriebsaufgaben des Providers
  Webserver              HTTP-Serverprogramm                               Nimmt Webanfragen an und liefert Inhalte oder leitet sie weiter
  Reverse Proxy          Serverseitiger Vermittler                         Nimmt öffentliche Anfragen entgegen und reicht sie an interne Dienste weiter
  Registrar              Domainregistrierungsanbieter                      Registriert Domainnamen für Kunden über das Domainvergabesystem
  DNS-Hosting            Verwaltung autoritativer DNS-Einträge             Legt fest, welche DNS-Antworten zu einer Domain bereitgestellt werden
  CNAME                  Canonical Name (DNS-Eintrag)                      Verweist im DNS auf einen anderen Namen statt unmittelbar auf eine IP-Adresse
  NAT / CGNAT            Network Address Translation / Carrier-Grade NAT   Lokale beziehungsweise providerseitige Adressübersetzung; CGNAT kann direkte eingehende IPv4-Zugriffe erschweren
  Portweiterleitung      Port Forwarding                                   Weiterleitung eingehender Verbindungen an ein internes Ziel
  TLS-Terminierung       Beendigung einer TLS-Verbindung                   Beispielsweise Entschlüsselung am Reverse Proxy vor interner Weitergabe
  Let's Encrypt          Zertifizierungsstelle                             Stellt nach erfolgreicher Kontrolle von Namen automatisierbar Zertifikate aus
  ACME                   Automatic Certificate Management Environment      Standardprotokoll zur automatisierten Zertifikatsverwaltung
  HTTP-01 / DNS-01       ACME-Prüfverfahren                                Nachweis der Kontrolle einer Domain über einen Webpfad bzw. DNS-Eintrag
  Monitoring             Betriebsüberwachung                               Beobachtung von Erreichbarkeit, Fehlern und Ressourcennutzung
  Log                    Ereignisprotokoll                                 Gespeicherte technische Ereignisse zur Analyse und Diagnose

## Ergänzungen aus M2-L2 – Webanwendungen und APIs {#S10}

  Begriff              Langform / Bedeutung                             Kurzerklärung
  -------------------- ------------------------------------------------ ---------------------------------------------------------------------------------------------------------
  Statische Website    Vorgefertigte Webdateien                         Webserver liefert Dateien ohne individuell berechnete HTML-Ausgabe aus
  Dynamische Website   Serverseitig erzeugte Ausgabe                    Seite wird mithilfe von Anwendungslogik und Daten zusammengestellt
  SPA                  Single-Page Application                          Oberfläche aktualisiert Bereiche nach dem ersten Seitenaufruf dynamisch
  Frontend             Benutzeroberfläche                               Sicht- und bedienbarer Anwendungsteil, im Web meist im Browser
  Backend              Anwendungslogik im Hintergrund                   Prüft Vorgänge und Berechtigungen, verarbeitet Daten und spricht Dienste an
  API                  Application Programming Interface                Vertrag für die Nutzung von Programmfunktionen durch andere Programme
  Endpunkt             API Endpoint                                     Definierte Adresse und Operation einer Webschnittstelle
  JSON                 JavaScript Object Notation                       Textbasiertes Format für strukturierte Daten
  REST                 Representational State Transfer                  Architekturstil unter anderem mit Ressourcen, einheitlicher Schnittstelle und zustandslosen Anfragen
  Idempotenz           Gleiche beabsichtigte Wirkung bei Wiederholung   Schutz vor unerwarteten Mehrfachwirkungen
  Webhook              Ereignisbenachrichtigung per HTTP                Dienst A benachrichtigt Dienst B aktiv über Ereignisse
  Hintergrundjob       Background Job                                   Aufgabe, die unabhängig von einer offenen Browseranfrage läuft
  Queue                Warteschlange                                    Hält Aufträge zur späteren Verarbeitung bereit
  Worker               Arbeitsprozess                                   Holt und bearbeitet Aufgaben aus einer Queue
  Scheduler            Zeitplaner                                       Startet Vorgänge nach zeitlichen Regeln
  WebSocket            WebSocket-Protokoll                              Länger bestehende, bidirektionale Browser-Server-Verbindung
  SSE                  Server-Sent Events                               Kontinuierliche Nachrichten vom Server an den Browser über HTTP
  Polling              Regelmäßige Statusabfrage                        Client erkundigt sich wiederholt nach einem Ergebnis
  Session-Cookie       Sitzungskennung im Browser-Cookie                Verknüpft Anfragen mit einer Anmeldesitzung
  RBAC                 Role-Based Access Control                        Zugriffsberechtigungen werden über Rollen organisiert
  Multi-Tenancy        Mandantenfähigkeit                               Mehrere getrennte Kundenorganisationen nutzen einen Dienst
  Stateful             Zustandsbehaftet                                 Komponente verwaltet für spätere Schritte erforderlichen Zustand
  Stateless            Zustandslos                                      Verarbeitung einzelner Anfragen hängt nicht von exklusiv lokal gespeichertem früherem Anfragekontext ab
  BOLA                 Broken Object Level Authorization                Sicherheitslücke durch fehlende objektbezogene Zugriffsprüfung
  Backpressure         Rückstaukontrolle                                Langsame Empfänger oder Worker sollen nicht unbegrenzt mit Daten überlastet werden

## Ergänzungen aus M2-L3 – Hosting- und Cloud-Bereitstellungsmodelle {#S11}

  Begriff                 Langform / Bedeutung                                        Kurzerklärung
  ----------------------- ----------------------------------------------------------- ------------------------------------------------------------------------------------------
  On-Premises             Betrieb am eigenen Standort                                 Eigene Hardware und überwiegend eigener Betrieb
  Colocation / Housing    Unterbringung eigener Server in fremdem Rechenzentrum       Anbieter liefert Standortdienste, Kunde betreut meist den Server
  Shared Hosting          Gemeinsam genutztes Webhosting                              Mehrere Kunden nutzen eine verwaltete Webserverumgebung
  Managed Hosting         Verwaltetes Hosting                                         Vertraglich vereinbarte Betriebsaufgaben werden zusätzlich vom Anbieter übernommen
  Unmanaged Hosting       Hosting ohne umfangreiche Administration                    Kunde verwaltet das Gastbetriebssystem und die Anwendung meist selbst
  Dedizierter Server      Physical Dedicated Server                                   Gemieteter physischer Rechner, typischerweise exklusiv für einen Kunden
  Public Cloud            Öffentlich angebotene Cloudinfrastruktur                    Für viele Organisationen als Dienst verfügbar; Daten müssen nicht öffentlich sein
  Private Cloud           Exklusive Cloudinfrastruktur einer Organisation             Cloudbetrieb für eine Organisation, lokal oder extern betrieben
  Hybrid Cloud            Kombination verbundener unterschiedlicher Cloudumgebungen   Verknüpft etwa Private und Public Cloud für gemeinsame Nutzung
  Community Cloud         Gemeinsame Cloud für eine definierte Organisationsgruppe    Organisatorisch geteilte Infrastruktur mit ähnlichen Anforderungen
  Multicloud              Nutzung mehrerer Cloudanbieter                              Kein klassisches NIST-Bereitstellungsmodell
  NIST                    National Institute of Standards and Technology              US-amerikanisches Institut, Quelle der klassischen Clouddefinition
  CaaS                    Containers as a Service                                     Verwaltete Ausführungsumgebung für Container
  FaaS                    Function as a Service                                       Ereignisgesteuerte Ausführung bereitgestellter Funktionen
  Serverless              Verdeckte Serververwaltung durch die Plattform              Server existieren, aber Kunden betreiben sie nicht selbst
  Managed Database        Verwaltete Datenbank                                        Anbieter übernimmt Teile des Datenbankbetriebs, nicht automatisch die Datenverantwortung
  Shared Responsibility   Gemeinsames Verantwortungsmodell                            Aufgaben verteilen sich je nach Dienstmodell zwischen Anbieter und Kunde
  Vendor Lock-in          Anbieterabhängigkeit                                        Plattformwechsel wird durch proprietäre Technik oder Prozesse aufwendig
  Cold Start              Start einer zuvor nicht bereiten Ausführungsumgebung        Kann bei ereignisgesteuerten Funktionen zusätzliche Latenz verursachen
  Ressourcenpool          Resource Pooling                                            Infrastruktur wird mehreren Kunden bedarfsweise zugeordnet
  Elastizität             Elasticity                                                  Kapazität kann auf wechselnde Nachfrage angepasst werden

## Ergänzungen aus M2-L4 – Virtualisierung und Container {#S12}

  Begriff              Langform / Bedeutung                              Kurzerklärung
  -------------------- ------------------------------------------------- -----------------------------------------------------------------------------
  Virtualisierung      Abstraktion physischer Rechnerressourcen          Ermöglicht mehrere logisch getrennte Umgebungen auf derselben Hardware
  Hypervisor           Virtualisierungssoftware bzw. -schicht            Stellt und verwaltet virtuelle Maschinen auf physischen Ressourcen
  Gastbetriebssystem   Guest Operating System                            Eigenes Betriebssystem innerhalb einer virtuellen Maschine
  Host                 Tragende Ausführungsumgebung                      Physischer Rechner bzw. System, das VMs oder Container bereitstellt
  vCPU                 virtual Central Processing Unit                   Virtuelle Prozessoreinheit; nicht zwingend exklusiver physischer Kern
  Virtueller Switch    Virtual Switch                                    Softwarebasierte Netzvermittlung zwischen virtuellen Schnittstellen
  KVM                  Kernel-based Virtual Machine                      Virtualisierungstechnik im Linux-Kernel
  Kernel               Betriebssystemkern                                Verantwortlich unter anderem für Prozesse, Speicher und Gerätezugriffe
  Container            Isolierter Anwendungsprozess bzw. Prozessgruppe   Läuft mit definiertem Dateisystem, Netzkontext und Ressourcenbeschränkungen
  Namespace            Linux-Namensraum                                  Isoliert Sicht auf Prozesse, Netzwerk, Benutzerkennungen u. a.
  cgroups              Control Groups                                    Linux-Mechanismus zur Organisation und Beschränkung von Ressourcen
  Container-Image      Paketierte Laufzeitvorlage                        Enthält Code, Bibliotheken, Dateien und Startinformationen
  Registry             Image-Registrierungsdienst                        Speichert und verteilt Container-Images
  Image-Layer          Schicht eines Container-Images                    Wiederverwendbare Menge von Dateisystemänderungen
  Image-Digest         Inhaltsbezogener Identifikator                    Bindet ein Image an eine bestimmte Paketfassung
  OCI                  Open Container Initiative                         Offene Standards zu Container-Images, Laufzeit und Verteilung
  Docker Engine        Docker-Laufzeit- und Verwaltungssoftware          Erstellt und betreibt Container auf einem Host
  Docker Compose       Werkzeug zur Mehrcontainerverwaltung              Beschreibt mehrere Dienste, Netze und Volumes gemeinsam
  Volume               Dauerhafter eingebundener Speicherbereich         Speichert Daten außerhalb der kurzlebigen Containerschicht
  Bind Mount           Einbindung eines Hostpfads                        Verbindet Container mit Dateien und Verzeichnissen des Hosts
  Kubernetes / K8s     Containerplattform zur Zustandsverwaltung         Verwaltet Anwendungsinstanzen über einen oder mehrere Knoten
  Control Plane        Steuerungsebene                                   Verwaltet den gewünschten Zustand eines Kubernetes-Clusters
  Node                 Clusterknoten                                     Physischer oder virtueller Rechner, der Pods ausführt
  Pod                  Kleinste Kubernetes-Bereitstellungseinheit        Umfasst einen oder mehrere eng gekoppelte Container
  Deployment           Kubernetes-Ressource für Anwendungsinstanzen      Definiert und verwaltet etwa Replikate und Aktualisierungen
  Kubernetes Service   Stabile Netzabstraktion                           Macht wechselnde Pod-Instanzen über eine definierte Adresse erreichbar
  Orchestrierung       Koordinierter Betrieb vieler Instanzen            Automatisiert Platzierung, Ersatz, Updates und Skalierung
  Soll-Zustand         Desired State                                     Deklarative Beschreibung, wie viele und welche Instanzen laufen sollen
  Rootless Mode        Betrieb ohne privilegierten Root-Daemon           Reduziert bestimmte Risiken bei der Containerverwaltung

## Ergänzungen aus M2-L5 – Cloud-Netzwerke und Skalierung {#S13}

  Begriff                  Langform / Bedeutung                   Kurzerklärung
  ------------------------ -------------------------------------- --------------------------------------------------------------------------------------
  Region                   Geografische Cloud-Standortgruppe      Anbieterdefinierter Standortbereich mit Ressourcen und Zonen
  AZ                       Availability Zone                      Betriebs- und Fehlerdomäne innerhalb einer Cloudregion (Anbieterdetails variieren)
  VPC                      Virtual Private Cloud                  Logisch abgegrenztes virtuelles Cloud-Netzwerk mit Routen und Regeln
  Subnet                   Teilnetz                               Abgegrenzter IP-Adressbereich eines Netzwerks
  Gateway                  Netzwerkknoten für Übergänge           Verbindet ein Netz mit anderen Netzwerken
  Load Balancer            Lastverteiler                          Verteilt Anfragen auf mehrere erreichbare Instanzen
  Health Check             Erreichbarkeits-/Funktionsprüfung      Prüft, ob ein Zielserver Anfragen bearbeiten kann
  Connection Draining      Auslaufenlassen aktiver Verbindungen   Nimmt eine Instanz für neue Anfragen heraus, ohne laufende sofort abzubrechen
  CDN                      Content Delivery Network               Geografisch verteiltes Auslieferungsnetz für geeignete Inhalte
  Origin-Server            Ursprungsserver                        Originalquelle der ausgelieferten Inhalte
  Cache                    Zwischenspeicher                       Hält wiederverwendbare Inhalte oder Ergebnisse vor
  Cache-Hit / Cache-Miss   Treffer / fehlender Eintrag            Inhalt liegt im Cache vor bzw. muss neu abgerufen werden
  Cache-Invalidation       Cache-Entwertung                       Veraltete Einträge gezielt ungültig machen
  Scale Up                 Vertikale Skalierung                   Vorhandene Instanz mit mehr Ressourcen ausstatten
  Scale Out                Horizontale Skalierung                 Zusätzliche Instanzen derselben Aufgabe starten
  Stateless                Zustandslos                            Benötigt keinen ausschließlich lokal gespeicherten Zustand aus früheren Anfragen
  Sticky Session           Sitzung an Instanz binden              Versucht, denselben Nutzer jeweils auf denselben Server zu leiten
  Session-Store            Gemeinsamer Sitzungsspeicher           Speichert serverseitige Sitzungsinformationen außerhalb eines einzelnen Webprozesses
  Autoscaling              Automatische Skalierung                Passt Ressourcen/Instanzen nach Regeln oder Messwerten an
  HPA                      Horizontal Pod Autoscaler              Kubernetes-Steuerung zur Anpassung der Anzahl laufender Pods
  Rate Limit               Ratenbegrenzung                        Beschränkt Anfragen oder Aktionen pro Zeitabschnitt
  Queue                    Warteschlange                          Puffert Aufträge bis zu ihrer Verarbeitung
  Worker                   Auftragsbearbeiter                     Hintergrundprozess, der Aufgaben verarbeitet
  Backpressure             Rückdruck / Überlaststeuerung          Begrenzt Zufluss, wenn nachgelagerte Verarbeitung nicht nachkommt
  Idempotenz               Wirkungssicherheit bei Wiederholung    Mehrfache Ausführung führt nicht zu mehrfacher unerwünschter Wirkung
  Throughput               Durchsatz                              Zahl verarbeiteter Aufgaben pro Zeiteinheit
  Latency                  Latenz                                 Dauer bis zu einem einzelnen Ergebnis oder einer Antwort
  Observability            Beobachtbarkeit                        Systemzustand durch Metriken, Logs und Traces nachvollziehen

## Ergänzungen aus M3-L1 – Eine Datenbank auf einem Server {#S14}

  Begriff                    Langform / Bedeutung                   Kurzerklärung
  -------------------------- -------------------------------------- -------------------------------------------------------------------------------------------------
  Datenseite / Datenblock    Page / Block                           Physische Einheit, in der ein Datenbanksystem mehrere Datensätze oder Indexeinträge organisiert
  Sequential Scan            Sequentieller Tabellenlauf             Untersucht Tabellenzeilen ohne selektiven Indexzugriff
  B-Tree                     Balanced Tree, balancierter Suchbaum   Häufige Indexstruktur für Such-, Bereichs- und Sortieranfragen
  Selektivität               Selectivity                            Anteil der Datensätze, die eine Suchbedingung erfüllen
  Abfrageplaner              Query Planner / Optimizer              Wählt anhand von Statistiken und Kostenabschätzungen einen Ausführungsweg
  EXPLAIN                    PostgreSQL-Analysewerkzeug             Zeigt den geplanten Datenbank-Abfrageweg
  EXPLAIN ANALYZE            PostgreSQL-Ausführungsanalyse          Führt die Anfrage aus und berichtet Messwerte; Schreibanfragen können Daten ändern
  Buffer Pool                Datenbank-Seitenpuffer                 Hält häufig benötigte Datenblöcke im RAM
  Cache-Hit / Cache-Miss     Puffer-Treffer / fehlender Eintrag     Benötigter Datenblock liegt im Speicher oder muss nachgeladen werden
  I/O                        Input/Output                           Ein-/Ausgabe, etwa Lesen und Schreiben von Speicherblöcken
  Write-Ahead Log (WAL)      Vorabprotokoll für Änderungen          Unterstützt Transaktionshaltbarkeit und Wiederherstellung nach bestimmten Abstürzen
  Connection Pool            Verbindungspool                        Wiederverwendbarer Vorrat begrenzter Datenbankverbindungen
  MVCC                       Multi-Version Concurrency Control      Reguliert gleichzeitige Transaktionen über verschiedene sichtbare Datenversionen
  Snapshot                   Konsistenter Daten-Sichtstand          Datenversion, die ein Lesevorgang nach den Isolationsregeln beobachten darf
  VACUUM                     PostgreSQL-Bereinigung                 Entfernt beziehungsweise verwaltet nicht mehr benötigte Datenversionen und Speicherplätze
  Hotspot                    Stark umkämpfter Datenbereich          Zeile oder Ressource, auf die viele Vorgänge zugreifen und sich behindern
  SQL-Injection              Einschleusen von SQL über Eingaben     Angriff, bei dem unkontrollierte Eingaben als Datenbankbefehle interpretiert werden
  Parameterisierte Anfrage   Parameterized Query                    Trennt Abfragestruktur von eingegebenen Werten
  Datenbank-Latenz           Query Latency                          Antwortzeit einer einzelnen Datenbankanfrage
  Datenbank-Durchsatz        Query Throughput                       Verarbeitete Datenbankanfragen pro Zeiteinheit

## Ergänzungen aus M3-L2 – Replikation und Hochverfügbarkeit {#S15}

  Begriff                  Langform / Bedeutung                  Kurzerklärung
  ------------------------ ------------------------------------- -------------------------------------------------------------------------------------
  Replikation              Replication                           Überträgt Daten oder Änderungen von einer Datenbank zu weiteren Knoten
  Primary / Primärserver   Schreibführende Instanz               Übernimmt im einfachen Primär-/Standby-Modell die Änderungen
  Standby                  Nachführender Datenbankknoten         Kann bei geeigneter Konfiguration übernehmen oder lesend genutzt werden
  Physische Replikation    Physical Replication                  Nachführung einer PostgreSQL-Instanz über WAL-/Speicheränderungen
  Logische Replikation     Logical Replication                   Übertragung von Änderungen ausgewählter Datenobjekte nach logischem Modell
  Streaming Replication    Laufende WAL-Übertragung              Änderungen werden inkrementell an einen Standby weitergegeben
  Log Shipping             Versand archivierter WAL-Dateien      Überträgt Protokollabschnitte an andere Datenbankknoten
  HA / Hochverfügbarkeit   High Availability                     Ziel, Betriebsunterbrechungen bei bestimmten Ausfällen gering zu halten
  Synchrone Replikation    Synchronous Replication               Commit wartet auf eine definierte Bestätigung ausgewählter Standbys
  Asynchrone Replikation   Asynchronous Replication              Primärserver wartet beim Commit nicht auf die Replikatbestätigung
  Replication Lag          Replikationsverzug                    Rückstand beim Empfangen oder Anwenden von Änderungen
  Read Replica             Lesereplikat                          Zusätzlicher Knoten für geeignete Leseabfragen
  Read-Your-Writes         Konsistenz nach eigenem Schreiben     Eigene bestätigte Änderungen beim nächsten Lesen wiederfinden
  Failover                 Ungeplanter Rollenwechsel             Ersatz übernimmt, nachdem der Primärserver ausfällt
  Switchover               Geplanter Rollenwechsel               Vorbereitete Umschaltung etwa für Wartungsarbeiten
  Promotion                Beförderung zum Primary               Ein Standby erhält die führende Schreibrolle
  Split-Brain              Gespaltene Führungsrolle              Zwei Systeme nehmen unkoordiniert widersprüchliche Schreibvorgänge an
  Fencing                  Technische Isolierung                 Verhindert, dass ein alter Primary weiterhin schreibend eingreift
  STONITH                  Shoot The Other Node In The Head      Technik zum gezielten Abschalten/Zurücksetzen eines problematischen Knotens
  Quorum                   Erforderliche Stimmenzahl             Mindestanzahl von Bestätigungen für eine Entscheidung
  RPO                      Recovery Point Objective              Ziel für maximal akzeptable Datenverlust-Zeitspanne
  RTO                      Recovery Time Objective               Ziel für maximal akzeptierte Wiederanlaufdauer
  Failure Domain           Fehlerdomäne                          Infrastrukturteil mit potenziell gemeinsamer Ausfallursache
  Replication Slot         PostgreSQL-Replikationsreservierung   Kann benötigte WAL-Dateien zurückhalten, verursacht ohne Kontrolle Speicher-Risiken

## Ergänzungen aus M3-L3 – Partitionierung und Sharding {#S16}

  Begriff                       Langform / Bedeutung                 Kurzerklärung
  ----------------------------- ------------------------------------ ---------------------------------------------------------------------------------------
  Tabellenpartitionierung       Table Partitioning                   Gliedert eine logische Tabelle in physische Teilstücke, auch innerhalb einer Instanz
  Horizontale Partitionierung   Horizontal Partitioning              Verteilt Tabellenzeilen auf getrennte Teilmengen
  Vertikale Partitionierung     Vertical Partitioning                Trennt Tabellenspalten oder Datenbereiche
  Sharding                      Verteilung von Teilbeständen         Ordnet Daten mehreren unabhängig verwalteten Datenbankeinheiten/Knoten zu
  Shard                         Teilbestand                          Unabhängig verwaltete Teilmenge einer verteilten Datenbank
  Shard Key                     Verteilungsschlüssel                 Bestimmt, auf welchem Shard ein Datensatz liegen soll
  Range Sharding                Bereichsverteilung                   Verteilt Daten anhand zusammenhängender Schlüsselbereiche
  Hash Sharding                 Hashbasierte Verteilung              Nutzt eine Hashfunktion zur Streuung von Datensätzen
  Lookup Sharding               Verzeichnisbasierte Verteilung       Ein Verzeichnis weist Schlüssel einem Shard zu
  Partition Pruning             Auslassen irrelevanter Partitionen   Der Abfrageplan überspringt Teilbereiche, die keine passenden Zeilen enthalten können
  Shard-Router                  Anfragenverteiler                    Leitet Anfragen anhand von Schlüssel oder Metadaten an passende Knoten
  Co-Location                   Zusammenlegung verwandter Daten      Häufig gemeinsam benötigte Datensätze liegen auf demselben Shard
  Cross-Shard-JOIN              Verteilte Tabellenverknüpfung        JOIN muss Daten von mehr als einem Shard berücksichtigen
  Fan-out / Scatter-Gather      Verteilen und Einsammeln             Anfrage geht an mehrere Shards; Ergebnisse werden zusammengeführt
  Rebalancing                   Neuverteilung                        Verlagert Shards/Teilbereiche bei veränderter Last oder zusätzlichen Knoten
  Hotspot (Sharding)            Überlasteter Teilbestand             Ein Shard erzeugt unverhältnismäßig viel Last
  2PC                           Two-Phase Commit                     Zweiphasiges Verfahren zur koordinierten Bestätigung einer verteilten Transaktion
  Citus                         PostgreSQL-Erweiterung               Stellt zusätzliche Funktionen für verteilte Tabellen und Shards bereit

## Ergänzungen aus M3-L4 – Distributed SQL, NoSQL und Konsistenz {#S17}

  Begriff                Langform / Bedeutung                                              Kurzerklärung
  ---------------------- ----------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------
  RDBMS                  Relational Database Management System                             Relationales Datenbankmanagementsystem mit Tabellen, Schlüsseln und Transaktionen
  NoSQL                  Sammelbezeichnung für nicht primär relationale Datenbanksysteme   Umfasst verschiedene Datenmodelle und Konsistenzmechanismen
  Dokumentendatenbank    Document Database                                                 Speichert zusammengehörige Daten in Dokumenten
  Key-Value-Store        Schlüssel-Wert-Speicher                                           Ordnet eindeutigen Schlüsseln Werte zu
  Distributed SQL        Verteilte SQL-Datenbankarchitektur                                Bietet SQL über mehreren abgestimmten Datenbankknoten
  Konsensalgorithmus     Consensus Algorithm                                               Einigt mehrere Knoten auf bestimmte Zustandsänderungen
  Raft                   Konsensprotokoll                                                  Verwaltet ein repliziertes, geordnetes Änderungsprotokoll über gewählte Führung und Mehrheiten
  Quorum                 Beschlussfähige Teilmenge                                         Erforderliche Zahl beteiligter Knoten für eine Entscheidung
  RAC                    Real Application Clusters                                         Oracle-Architektur mit mehreren Datenbankinstanzen und gemeinsamem Speicher
  Shared Everything      Gemeinsam genutzte Ressourcen                                     Clusterinstanzen greifen auf gemeinsame Daten und Storage zu
  Shared Nothing         Unabhängige Ressourcen                                            Knoten/Shards haben eigene Datenhaltungsressourcen
  Shard Director         Shard-Verbindungsrouter                                           Oracle-Komponente zum Anfragenrouting nach Datenort
  YSQL                   Yugabyte SQL                                                      PostgreSQL-nahe SQL-Schnittstelle von YugabyteDB
  Tablet                 Datenbereich einer verteilten Datenbank                           Kleinere verwaltete Dateneinheit, etwa bei YugabyteDB
  Serializable           Serialisierbar                                                    Transaktionen ergeben ein Resultat wie bei einem zulässigen seriellen Ablauf
  Linearisierbarkeit     Linearizability                                                   Operationen erscheinen entsprechend realer Reihenfolge wie atomare Einzelschritte
  Eventual Consistency   Schließlich eintretende Konsistenz                                Replikate nähern sich bei ausbleibenden neuen Änderungen und funktionierender Kommunikation einander an
  Causal Consistency     Kausale Konsistenz                                                Abhängige Operationen werden in kausal passender Reihenfolge sichtbar
  Read Your Writes       Eigene Änderungen sehen                                           Folgezugriffe eines Nutzers erkennen zuvor bestätigte eigene Änderungen
  Monotonic Reads        Nicht zurückfallende Lesesicht                                    Eine Folge von Lesezugriffen fällt nicht auf ältere bereits überholte Stände zurück
  CAP                    Consistency, Availability, Partition Tolerance                    Grundsätzlicher Zielkonflikt bei Netzpartitionen zwischen strenger Konsistenz und starker Verfügbarkeit
  Netzpartition          Network Partition                                                 Zeitweiser Kommunikationsausfall zwischen Teilen eines verteilten Systems
  PACELC                 Partition, Availability, Consistency; Else Latency, Consistency   Ergänzende Betrachtung von Latenz/Konsistenz auch ohne Partition
  Lost Update            Verlorene Änderung                                                Ein späterer Schreibzugriff überschreibt unbeabsichtigt eine parallele Änderung
  Write Skew             Schreibanomalie über mehrere Datensätze                           Zwei für sich gültige Änderungen verletzen gemeinsam eine fachliche Regel
  Lock                   Sperre                                                            Koordiniert gleichzeitig konkurrierende Datenzugriffe
  Retry                  Wiederholungsversuch                                              Erneuter Versuch eines fehlgeschlagenen oder unklar bestätigten Vorgangs
  Idempotenz             Wiederholbare Wirkung ohne Doppeleffekt                           Derselbe Vorgang darf erneut eintreffen, ohne fachlich doppelt zu wirken
  At-least-once          Mindestens einmal                                                 Zustellmodell, bei dem Nachrichten mehrfach eintreffen können
  Transactional Outbox   Transaktionaler Postausgang                                       Geschäftsdaten und Versandauftrag werden gemeinsam in einer lokalen Transaktion gespeichert
  Dual Write             Doppelter Schreibvorgang                                          Fachliche Änderung und Ereignisversand erfolgen getrennt und können auseinanderfallen
  2PC                    Two-Phase Commit                                                  Koordinierte Vorbereitung und Entscheidung bei verteilten Transaktionen
  Saga                   Kette lokaler Transaktionen                                       Koordiniert verteilte Geschäftsabläufe einschließlich möglicher Kompensationen
  Kompensation           Compensating Transaction                                          Geschäftsseitige Ausgleichsaktion nach bereits bestätigten Teilvorgängen
  Inbox-Muster           Verarbeitungsprotokoll für eingehende Nachrichten                 Speichert Kennungen bearbeiteter Ereignisse gegen Doppeleffekte

## Ergänzungen aus M3-L6 – Datenhaltbarkeit und Wiederherstellung {#S18}

  Begriff                    Langform / Bedeutung                         Kurzerklärung
  -------------------------- -------------------------------------------- ------------------------------------------------------------------------------------------
  Backup                     Unabhängige Datensicherung                   Aufbewahrter Bestand für eine spätere Wiederherstellung
  Logisches Backup           Logical Backup                               Exportiert Daten und Struktur in wiederimportierbarer Form
  Physisches Backup          Physical Backup                              Sichert Datenbankdateien beziehungsweise den physischen Clusterzustand
  Basisbackup                Base Backup                                  Ausgangsstand für Wiederherstellung und gegebenenfalls WAL-Wiedereinspielung
  Vollbackup                 Full Backup                                  Enthält vollständigen benötigten Ausgangsdatenbestand
  Inkrementelles Backup      Incremental Backup                           Sichert bestimmte Änderungen seit einem früheren Sicherungsstand
  Differenzielles Backup     Differential Backup                          Sichert Änderungen seit einer definierten Vollsicherung
  Speicher-Snapshot          Storage Snapshot                             Zustandsbild eines Speichers zu einem Zeitpunkt; nicht mit MVCC-Lesesnapshot verwechseln
  Crash-konsistent           Crash-consistent                             Datensicht vergleichbar mit abruptem Systemabbruch; Datenbank-Recovery kann nötig sein
  Anwendungskonsistent       Application-consistent                       Sicherung berücksichtigt die Konsistenzanforderungen der beteiligten Anwendung
  PITR                       Point-in-Time Recovery                       Datenbankwiederherstellung bis zu einem gewählten früheren Zeitpunkt
  WAL-Archiv                 Write-Ahead Log Archive                      Aufbewahrte Änderungsprotokolle für geeignete physische Wiederherstellung
  Offsite-Backup             Räumlich/technisch getrennte Kopie           Schutz vor gemeinsamen Ausfällen am Hauptstandort
  Immutable Backup           Unveränderliche Sicherung                    Während einer Schutzfrist nicht ohne Weiteres lösch- oder überschreibbar
  Offline-Backup             Getrennte Datensicherung                     Nicht dauerhaft mit dem laufenden System verbunden
  Restore                    Wiederherstellung                            Daten oder Systeme aus gesicherten Beständen wieder nutzbar machen
  Restore-Test               Wiederherstellungstest                       Prüft die tatsächliche Wiederverwendbarkeit einer Sicherung
  Backup-Retention           Aufbewahrungsdauer                           Regel zur Historie und Löschung alter Sicherungen
  Backup-Manifest            Sicherungsdateiverzeichnis/Prüfinformation   Dokumentiert zugehörige Backup-Dateien und ermöglicht Integritätsprüfung
  3-2-1-Regel                Backup-Merkhilfe                             Drei Kopien, zwei Medien/Systemtypen, eine getrennte Kopie
  Job / Hintergrundauftrag   Background Job                               Abgegrenzte, ggf. später bearbeitete Arbeit mit Kennung und Status
  Queue / Job Queue          Warteschlange                                Puffer für noch nicht ausgeführte Aufgaben
  Worker                     Arbeiterprozess                              Prozess, der einen Auftrag entgegennimmt und ausführt
  Scheduler                  Planer                                       Entscheidet über Ausführungszeitpunkt oder Ressourcenzuteilung
  Message Broker             Nachrichtenbroker                            Vermittelt Nachrichten zwischen sendenden und empfangenden Programmen
  Producer / Consumer        Produzent / Konsument                        Nachrichtensender und Nachrichtenempfänger
  Pub/Sub                    Publish/Subscribe                            Ereignisverteilung an mehrere unabhängige Abonnenten
  Event Bus                  Ereignisbus                                  Vermittelt Ereignisse anhand von Typen oder Regeln
  Event Streaming            Ereignisstromverarbeitung                    Kontinuierliche Verarbeitung von Nachrichten- oder Ereignisfolgen
  DAG                        Directed Acyclic Graph                       Gerichteter azyklischer Graph für Abhängigkeiten von Arbeitsschritten
  Concurrency                Nebenläufigkeit                              Mehrere Aufgaben machen überlappend Fortschritt
  Parallelism                Parallelität                                 Mehrere Rechenschritte finden tatsächlich gleichzeitig statt
  Batch Processing           Stapelverarbeitung                           Gesammelte Aufträge oder Daten in Paketen verarbeiten
  Streaming                  Stromverarbeitung                            Fortlaufend eintreffende Daten verarbeiten
  Hard Real-Time             Harte Echtzeit                               Verbindliche Reaktionsfrist, deren Verfehlen unzulässig ist
  ACK                        Acknowledgement                              Empfangs- oder Bearbeitungsbestätigung in Nachrichtensystemen
  Retry / Backoff            Wiederholung / wachsende Wartezeit           Fehlerbehandlung mit begrenzten erneuten Versuchen
  DLQ                        Dead-Letter Queue                            Auffangwarteschlange für wiederholt nicht verarbeitbare Nachrichten
  Backpressure               Rückdruck                                    Schutz vor Überlast durch Begrenzen weiterer Zufuhr
  SQS                        Simple Queue Service                         Verwalteter Warteschlangendienst von Amazon Web Services
  GPU-Worker                 Worker mit Grafikprozessor                   Führt dafür geeignete parallele Rechen- oder KI-Aufgaben aus
  Modellinferenz             Inference                                    Ausführung eines bereits trainierten Modells auf neuen Eingaben

## Ergänzungen aus M4-L2 – Bereitstellung und Zuverlässigkeit {#S19}

  Begriff                        Langform / Bedeutung                        Kurzerklärung
  ------------------------------ ------------------------------------------- ------------------------------------------------------------------------------------------
  Deployment                     Bereitstellung                              Installation und Aktivierung einer bestimmten Softwareversion in einer Umgebung
  Artefakt / Build-Artefakt      Erzeugtes Softwarepaket                     Geprüftes, identifizierbares Ergebnis eines Build-Prozesses
  Staging                        Vorproduktionsumgebung                      Prüfstand vor der produktiven Freigabe einer Software
  Infrastructure as Code / IaC   Infrastruktur als Code                      Versionierbare Definition und automatisierte Verwaltung von Infrastruktur
  State (IaC)                    Zustandsinformation der Infrastruktur       Ordnet verwaltete Ressourcen ihren Konfigurationen zu; ist schutzbedürftig
  Observability                  Beobachtbarkeit                             Zusammenhänge im System anhand ausgegebener Signale verstehen
  Monitoring                     Systemüberwachung                           Beobachtung definierter Kenngrößen und Zustände
  Log                            Ereignisprotokoll                           Zeitlich zugeordneter Eintrag über ein Ereignis
  Metrik                         Quantitative Messgröße                      Zeitreihe etwa für Antwortzeit, Fehlerquote oder Ressourcennutzung
  Trace                          Ablaufspur                                  Zusammenhang mehrerer Verarbeitungsschritte einer Anfrage
  Span                           Einzelschritt eines Traces                  Zeitlicher Abschnitt einer nachvollziehbaren Operation
  OpenTelemetry                  Offener Telemetrie-Standard und Werkzeuge   Erfasst und exportiert Logs, Metriken und Traces; kein eigenständiges Monitoring-Backend
  Alerting                       Alarmierung                                 Benachrichtigung bei relevanten Betriebsereignissen
  Liveness Probe                 Lebensprüfung                               Prüft, ob ein Neustart eines blockierten Prozesses sinnvoll sein kann
  Readiness Probe                Bereitschaftsprüfung                        Prüft, ob eine Instanz aktuell Nutzerverkehr empfangen sollte
  Startup Probe                  Startprüfung                                Schützt lange anlaufende Dienste vor voreiligen Neustarts
  Rolling Update                 Schrittweise Aktualisierung                 Neue Instanzen ersetzen alte nach und nach
  Blue-Green Deployment          Umschaltung zwischen zwei Umgebungen        Neue Version wird vor der öffentlichen Umschaltung separat geprüft
  Canary Release                 Gestaffelte Freigabe                        Zunächst erhält nur ein Teil der Nutzer die neue Version
  Feature Flag                   Funktionsschalter                           Aktiviert eine Programmfunktion ohne neue Softwareveröffentlichung
  Rollback                       Rücknahme auf eine frühere Version          Macht eine Softwareänderung rückgängig, nicht zwingend ihre Datenfolgen
  Datenbankmigration             Schema- oder Datenumstellung                Passt gespeicherte Strukturen an neue Softwareversionen an
  Expand and Contract            Erst erweitern, später abbauen              Muster für kompatible schrittweise Datenbankänderungen
  SLI                            Service Level Indicator                     Messgröße für die Qualität eines Dienstes
  SLO                            Service Level Objective                     Festgelegtes Ziel für einen SLI
  Error Budget                   Fehlerbudget                                Im SLO berücksichtigte rechnerische Abweichungstoleranz
  SRE                            Site Reliability Engineering                Technische Methoden und organisatorische Praxis für zuverlässigen Betrieb
  Single Point of Failure        Einzelner Ausfallpunkt                      Dessen Ausfall kann den ganzen Dienst beeinträchtigen
  Availability Zone              Verfügbarkeitszone                          Infrastruktur-Ausfallbereich innerhalb einer Cloud-Region

## Ergänzungen aus M4-L3 – Sicherheit, Datenschutz und Verantwortung {#S20}

  Begriff                    Langform / Bedeutung                                               Kurzerklärung
  -------------------------- ------------------------------------------------------------------ --------------------------------------------------------------------------------------------------------------------
  Vertraulichkeit            Confidentiality                                                    Schutz vor unberechtigter Einsicht in Informationen
  Integrität                 Integrity                                                          Schutz vor unbemerkter oder unerlaubter Veränderung von Daten
  Bedrohungsmodell           Threat Modeling                                                    Systematische Betrachtung von Schutzgütern, Angreifern und Schwachstellen
  Authentifizierung          Authentication                                                     Nachweis einer Identität
  Autorisierung              Authorization                                                      Prüfung der erlaubten Aktion auf einer Ressource
  IAM                        Identity and Access Management                                     Verwaltung von Identitäten und Zugriffsberechtigungen
  Least Privilege            Prinzip der geringsten Rechte                                      Vergibt nur die wirklich benötigten Berechtigungen
  RBAC                       Role-Based Access Control                                          Rollenbasierte Zugriffssteuerung
  ABAC                       Attribute-Based Access Control                                     Zugriffsentscheidung anhand von Merkmalen und Regeln
  MFA                        Multi-Factor Authentication                                        Anmeldung mit mehreren unabhängigen Faktoren
  FIDO2 / WebAuthn           Standards für starke Webauthentifizierung                          Grundlage vieler Passkey-Verfahren
  Passkey                    Schlüsselbasierte Anmeldung                                        Authentifizierung mit kryptografischem Schlüssel statt wiederverwendbarem Webseitenpasswort
  Passwort-Hash              Einweg-Prüfwert eines Passworts                                    Muss mit geeigneten langsamen Passwort-Hash-Verfahren erzeugt werden
  Salt                       Zufälliger Zusatzwert                                              Verhindert, dass identische Passwörter automatisch identische Prüfwerte liefern
  Argon2id                   Speicheraufwendige Passwort-Hash-Funktion                          Erschwert massenhaftes Erraten gestohlener Passwortprüfwerte
  Session                    Sitzung                                                            Wiedererkennbarer, zeitlich begrenzter Nutzerkontext
  CSRF                       Cross-Site Request Forgery                                         Unerwünschte Aktionen über fremde Webinhalte im Kontext einer Anmeldung
  Secret                     Vertraulicher Zugangswert                                          Etwa API-Schlüssel, Datenbankpasswort oder privater Schlüssel
  Secret Manager             Werkzeug zur Verwaltung von Geheimnissen                           Begrenzt und protokolliert Zugriff auf vertrauliche Werte
  Schlüsselrotation          Austausch eines Geheimnisses/Schlüssels                            Begrenzung der Folgen und Lebenszeit von Zugangswerten
  Encryption at Rest         Verschlüsselung ruhender Daten                                     Schutz bestimmter gespeicherter Daten gegen unberechtigten Zugriff
  Rate Limit                 Aufrufbegrenzung                                                   Begrenzt, wie häufig eine Schnittstelle verwendet werden darf
  SSRF                       Server-Side Request Forgery                                        Missbrauch von serverseitigen Netzwerkaufrufen zu ungewollten Zielen
  DSGVO / GDPR               Datenschutz-Grundverordnung / General Data Protection Regulation   Europäische Regeln zur Verarbeitung personenbezogener Daten
  Verantwortlicher           Data Controller                                                    Legt Zwecke und wesentliche Mittel einer Verarbeitung fest
  Auftragsverarbeiter        Data Processor                                                     Verarbeitet Daten im Auftrag und nach den maßgeblichen Weisungen
  AVV                        Auftragsverarbeitungsvertrag                                       Vertragliche Grundlage bei Auftragsverarbeitung nach Art. 28 DSGVO
  Privacy by Design          Datenschutz durch Technikgestaltung                                Datenschutz schon im Systementwurf berücksichtigen
  Privacy by Default         Datenschutzfreundliche Voreinstellungen                            Standardmäßig nur erforderliche Daten verarbeiten
  Pseudonymisierung          Ersetzung direkter Merkmale                                        Erschwert Zuordnung, ohne Personenbezug sicher auszuschließen
  EWR                        Europäischer Wirtschaftsraum                                       EU-Staaten sowie Island, Liechtenstein und Norwegen
  Angemessenheitsbeschluss   Adequacy Decision                                                  EU-Kommissionsentscheidung über angemessenes Drittland-Datenschutzniveau
  SCC                        Standard Contractual Clauses                                       EU-Standardvertragsklauseln für bestimmte Datentransfers
  Datenschutzverletzung      Personal Data Breach                                               Sicherheitsverletzung mit Verlust, Veränderung, Offenlegung oder unberechtigtem Zugriff auf personenbezogene Daten

## Ergänzungen aus M4-L4 – Kosten verstehen {#S21}

  Begriff           Langform / Bedeutung                        Kurzerklärung
  ----------------- ------------------------------------------- -----------------------------------------------------------------------------------------------------
  Fixkosten         Laufende Grundkosten                        Kosten, die innerhalb der betrachteten Periode auch ohne einzelne neue Aufträge anfallen
  Variable Kosten   Nutzungsabhängige Kosten                    Steigen mit der genutzten Leistung oder Datenmenge
  Grenzkosten       Zusätzliche Kosten einer weiteren Einheit   Was eine weitere erfolgreich erbrachte Leistung zusätzlich kostet
  Egress            Ausgehender Datenverkehr                    Datenübertragung aus einem Cloud-Dienst oder definierten Netzwerkbereich
  GB-Monat          Gigabyte mal Aufbewahrungsdauer             Maßeinheit für gespeicherte Daten über einen Zeitraum
  GB-Sekunde        Gigabyte mal Ausführungszeit                Häufige Modellgröße bei speicher- und zeitabhängiger Funktionsabrechnung
  Cloud-Budget      Geplantes Ausgabenziel                      Rechengröße für Warnungen oder, falls gesondert unterstützt, technische Ausgabenbegrenzung
  Spend Cap         Technische Ausgabenbegrenzung               Kann bei unterstützten Diensten weitere Nutzung blockieren; kein universelles Merkmal jedes Budgets
  Kostenalarm       Budgetwarnung                               Informiert über eine Schwelle, begrenzt die Ausgaben nicht automatisch
  TCO               Total Cost of Ownership                     Gesamtkosten über einen Nutzungszeitraum einschließlich Betrieb und Zusatzaufwand
  FinOps            Financial Operations                        Kosten und geschäftlichen Nutzen von Technologie gemeinsam analysieren
  Unit Economics    Kosten pro sinnvoller Leistungseinheit      Beispielsweise pro erfolgreicher Analyse oder nutzbarem KI-Ergebnis
  Kostentreiber     Dominante Ausgabenursache                   Beispielsweise GPU-Laufzeit, große Dateien oder Datenbankkapazität
  Auslastung        Verhältnis von Nutzung zu Kapazität         Beeinflusst die Kosten pro erledigtem Auftrag
  Vendor Lock-in    Anbieterabhängigkeit                        Aufwand und Risiken beim Wechsel von proprietären Plattformdiensten

## Ergänzungen aus M4-L5 – Eigene Software- und Cloud-Angebote {#S22}

  Begriff               Langform / Bedeutung                           Kurzerklärung
  --------------------- ---------------------------------------------- -------------------------------------------------------------------------------------------------------------------------------------
  SaaS-Produkt          Software as a Service                          Als Dienst genutzte Anwendung mit laufender Betreiberverantwortung
  API-as-a-Service      Programmierschnittstelle als Dienst            Maschinenlesbare Funktion für externe Kundenprogramme
  Managed Automations   Betreute Automatisierung                       Wiederkehrende Abläufe einschließlich Einrichtung und Betrieb übernehmen
  Mandant / Tenant      Einzelner Kundenbereich                        Logische Zuordnung von Nutzern, Daten, Berechtigungen und Kosten
  Mandantenisolierung   Tenant Isolation                               Schutz vor unberechtigtem Zugriff zwischen Kundenbereichen
  Onboarding            Einführung eines neuen Kunden                  Technisches Anlegen von Konto, Berechtigungen und gegebenenfalls Abrechnung
  MVP                   Minimum Viable Product                         Kleinste brauchbare Fassung, die den zentralen Nutzen überprüfbar macht
  Freemium              Kostenlose Basis, bezahlte Erweiterung         Geschäftsmodell mit begrenztem Gratiszugang und kostenpflichtigen Funktionen
  Metered Billing       Nutzungsabhängige Abrechnung                   Abrechnung anhand gemessener Aufrufe, Aufträge oder Verbrauchseinheiten
  Guthabenmodell        Prepaid Credits                                Vorab bezahltes, später verbrauchtes Nutzungsbudget
  AGPLv3                GNU Affero General Public License, Version 3   Open-Source-Lizenz mit besonderen Bedingungen bei Netzwerkinteraktion modifizierter Programme
  OSS                   One Stop Shop (EU-Umsatzsteuer)                Vereinfachtes Verfahren für bestimmte grenzüberschreitende Umsatzsteuerfälle; im Kontext nicht mit Open Source Software verwechseln
  B2B / B2C             Business to Business / Business to Consumer    Angebot an Unternehmen / Privatkunden
  Kundennutzen          Value Proposition                              Für die Zielgruppe erkennbarer praktischer Vorteil eines Angebots
  Kündigungsrate        Churn Rate                                     Anteil der Kunden, die innerhalb eines Zeitraums abspringen
  Stückkosten           Unit Economics                                 Kosten und Erlöse einer sinnvoll definierten Leistungseinheit

## Ergänzungen aus M5-L1 – Geschichte der künstlichen Intelligenz {#S23}

  Begriff             Langform / Bedeutung                                    Kurzerklärung
  ------------------- ------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------
  KI / AI             Künstliche Intelligenz / Artificial Intelligence        Forschungs- und Anwendungsfeld für Systeme mit Fähigkeiten wie Mustererkennung, Problemlösen und Sprachverarbeitung
  Symbolische KI      Regel- und symbolbasierte KI                            Stellt Wissen und Schlussregeln explizit dar und verarbeitet sie mit Logik oder Suche
  ML                  Machine Learning / maschinelles Lernen                  Verfahren, die Muster und Entscheidungsfunktionen aus Beispieldaten ableiten
  Deep Learning       Tiefes Lernen                                           Maschinelles Lernen mit meist mehrschichtigen neuronalen Netzen
  Generative KI       Inhaltserzeugende Modelle                               Erzeugen Text, Bilder, Audio oder andere neue Ausgaben auf Basis gelernter Muster
  LLM                 Large Language Model / großes Sprachmodell              Auf umfangreichen Sprach-/Tokendaten trainiertes Modell zur Verarbeitung und Erzeugung von Sprache
  Perzeptron          Frühes lernfähiges Neuronenmodell                       Verknüpft Eingabemerkmale mit anpassbaren Gewichten und bildet eine Entscheidung
  XOR                 Exclusive OR / exklusives Oder                          Logische Verknüpfung, die bei genau einem wahren Eingang wahr ist; klassisches Beispiel für Grenzen einfacher linearer Modelle
  Expertensystem      Regelbasiertes Fachsystem                               Verbindet eine explizite Wissensbasis mit einer Schlussfolgerungsmaschine
  Inferenzmaschine    Rule / Inference Engine                                 Wertet Regeln und Fakten aus, um Folgerungen abzuleiten
  KI-Winter           Rückgang von Förderung und Erwartungen                  Historische Phasen enttäuschter Versprechen, ohne kompletten Stillstand der Forschung
  Backpropagation     Rückwärtsweitergabe von Ableitungsinformationen         Methode zur Berechnung des Beitrags von Modellparametern zum Trainingsfehler
  GPU                 Graphics Processing Unit                                Paralleler Rechenprozessor, häufig zum Trainieren und Ausführen neuronaler Netze genutzt
  AlexNet             Tiefe Bildklassifikationsarchitektur (2012)             Bekannter Meilenstein für große Bilddatensätze und GPU-gestütztes Deep Learning
  Transformer         Aufmerksamkeitsbasierte Netzarchitektur (2017)          Grundlage vieler moderner Sprach- und Multimodalmodelle
  Attention           Aufmerksamkeitsgewichtung                               Mathematische Gewichtung von Beziehungen zwischen Elementen einer Eingabesequenz
  Token               Modellabhängige Texteinheit                             Beispielsweise Wortteil oder Satzzeichenfolge; wird numerisch verarbeitet
  Pretraining         Vortraining                                             Umfangreiche anfängliche Lernphase, oft vor einer Anpassung an spezielle Aufgaben
  Few-Shot Learning   Lernen / Adaptieren mit wenigen Beispielen im Kontext   Ein Modell erkennt ein Aufgabenschema aus wenigen Eingabebeispielen, ohne notwendigerweise seine Gewichte zu ändern

## Ergänzungen aus M5-L2 – Was ist ein neuronales Netz? {#S24}

  Begriff              Langform / Bedeutung                 Kurzerklärung
  -------------------- ------------------------------------ -------------------------------------------------------------------------------------------
  Künstliches Neuron   Mathematische Recheneinheit          Berechnet gewichtete Eingangssumme, Bias und gegebenenfalls Aktivierungsfunktion
  Feature              Eingabemerkmal                       Numerischer Wert, der einem Modell als Eingabe oder interne Repräsentation dient
  Gewicht / Weight     Trainierbarer Modellparameter        Bestimmt den Beitrag eines Eingangs zu einer Neuronenrechnung
  Bias                 Trainierbarer Versatz                Verändert den Grundwert einer Recheneinheit unabhängig von aktuellen Eingaben
  ReLU                 Rectified Linear Unit                Aktivierungsfunktion max(0, z); negative Werte werden null
  Hidden Layer         Verborgene Schicht                   Interne Verarbeitungsstufe zwischen Modelleingabe und Modellausgabe
  Forward Pass         Vorwärtsdurchlauf                    Berechnung einer Ausgabe mit den aktuellen Modellparametern
  Loss Function        Verlustfunktion                      Misst den Fehler zwischen Ausgabe und Lernziel nach einer festgelegten Vorschrift
  Gradient             Änderungsraten der Verlustfunktion   Ableitungen des Fehlers nach sämtlichen trainierbaren Parametern
  Gradient Descent     Gradientenabstieg                    Ändert Modellparameter in Richtung eines lokal geringeren Fehlers
  Backpropagation      Rückwärtsberechnung von Gradienten   Berechnet Ableitungen effizient über die Kettenregel durch ein Netz
  Lernrate             Learning Rate                        Faktor für die Schrittweite bei Gewichtsänderungen
  SGD                  Stochastic Gradient Descent          Gradientenverfahren mit stochastisch gewählten Beispielen oder Mini-Batches
  Batch / Mini-Batch   Datenpaket für einen Rechenschritt   Kleine Gruppe von Trainingsbeispielen zur gemeinsamen Gradientenberechnung
  Epoch                Epoche                               Ein vollständiger Durchlauf über die vorgesehene Trainingsmenge
  Hyperparameter       Vorgabe des Lernverfahrens           Etwa Lernrate, Batchgröße oder Zahl der Schichten, nicht direkt wie Gewichte trainiert
  Generalisierung      Übertragbarkeit auf neue Fälle       Fähigkeit, auch bislang unbekannte Beispiele sinnvoll zu bearbeiten
  Overfitting          Überanpassung                        Geringer Trainingsfehler bei schwächerer Leistung auf neuen Daten
  Underfitting         Unteranpassung                       Modell erfasst selbst die grundlegenden Trainingsmuster unzureichend
  Data Leakage         Datenleckage in der Evaluation       Unzulässige Information aus Prüf- oder Zukunftsdaten beeinflusst die Entwicklung
  Dropout              Trainingsregularisierung             Blendet vorübergehend Aktivierungen aus, um Überanpassung zu begrenzen
  CNN                  Convolutional Neural Network         Netz mit Faltungsschichten und geteilten Filtergewichten, etwa für Bilddaten
  RNN                  Recurrent Neural Network             Netz mit internem Zustand für schrittweise Verarbeitung von Folgen
  LSTM                 Long Short-Term Memory               Rekurrente Netzarchitektur mit speziellen Mechanismen für Zustands- und Informationsfluss
  VRAM                 Video Random Access Memory           Speicher auf einer Grafikkarte, relevant für Modellparameter und Zwischenwerte

## Ergänzungen aus M5-L3 – Wie Maschinen lernen {#S25}

  Begriff                       Langform / Bedeutung                           Kurzerklärung
  ----------------------------- ---------------------------------------------- -------------------------------------------------------------------------------------------
  Supervised Learning           Überwachtes Lernen                             Lernt aus Eingaben mit bekannten Zielwerten beziehungsweise Labels
  Unsupervised Learning         Unüberwachtes Lernen                           Sucht in Daten ohne vorgegebene Zielbeschriftungen nach Strukturen
  Self-Supervised Learning      Selbstüberwachtes Lernen                       Erzeugt Vorhersageziele aus den vorhandenen Daten selbst
  Reinforcement Learning (RL)   Bestärkendes Lernen                            Erlernt eine Handlungsstrategie anhand von Belohnungen aus einer Umgebung
  Transfer Learning             Übertragen gelernter Fähigkeiten               Verwendet bereits trainierte Parameter oder Repräsentationen für eine neue Aufgabe
  Fine-Tuning                   Feinabstimmung                                 Trainiert ein bestehendes Modell für einen engeren Zweck weiter
  Label                         Zielbeschriftung / Zielwert                    Gewünschte Ausgabe für ein Lernbeispiel bei überwachtem Lernen
  Klassifikation                Kategorievorhersage                            Ordnet ein neues Beispiel einer oder mehreren Kategorien zu
  Regression (ML)               Vorhersage kontinuierlicher Zielwerte          Schätzt beispielsweise Preis, Temperatur oder Verbrauch
  Clustering                    Gruppenbildung                                 Sucht Datenpunkte mit ähnlichen Merkmalen und ordnet sie Gruppen zu
  k-Means                       Cluster-Verfahren                              Ordnet Punkte wiederholt k Gruppenzentren zu und aktualisiert die Zentren
  Masked Language Modeling      Vorhersage verdeckter Texteinheiten            Selbstüberwachtes Lernziel mit ausgeblendeten Tokens
  Policy                        Handlungsstrategie                             Regel oder Modell, das für Beobachtungen Aktionen auswählt
  Reward / Return               Belohnung / kumulative Belohnung               Bewertet Handlungsschritte bzw. deren Gesamtfolge im bestärkenden Lernen
  Reward Hacking                Optimierung am Ziel vorbei                     Ein Agent verbessert einen Belohnungswert, ohne das eigentliche Ziel sinnvoll zu erfüllen
  Embedding                     Zahlenvektor einer Darstellung                 Modellabhängige numerische Repräsentation von Text, Bild oder anderem Inhalt
  One-Hot Encoding              Kodierung mit einer aktiven Stelle             Vektor mit je einem Platz pro möglicher Kategorie
  Precision                     Präzision                                      Anteil tatsächlich positiver Fälle unter allen positiv vorhergesagten
  Recall                        Trefferquote                                   Anteil erkannter positiver Fälle unter allen tatsächlich positiven
  Accuracy                      Gesamtgenauigkeit                              Anteil richtiger Vorhersagen unter allen Beispielen; bei seltenen Klassen oft irreführend
  F1-Wert                       Harmonisches Mittel aus Precision und Recall   Kombinierter Klassifikationswert für Präzision und Trefferquote
  Konfusionsmatrix              Verwechslungsmatrix                            Zeigt richtige und falsche positive beziehungsweise negative Entscheidungen
  Benchmark                     Standardisierter Vergleichstest                Erfasst definierte Modellleistungen unter bestimmten Testbedingungen
  Distribution Shift            Verteilungsverschiebung                        Neue Daten unterscheiden sich statistisch von Trainings- oder Testdaten
  Training-Serving-Skew         Unterschied zwischen Training und Betrieb      Tatsächliche Eingaben werden anders erfasst oder verarbeitet als Trainingsdaten
  Data Poisoning                Manipulation von Trainingsdaten                Angreifer versuchen Modellverhalten durch präparierte Daten zu beeinflussen

## Ergänzungen aus M6-L1 – Von Sprachverarbeitung zu Transformer und LLM {#S26}

  Begriff                            Langform / Bedeutung                                            Kurzerklärung
  ---------------------------------- --------------------------------------------------------------- -------------------------------------------------------------------------------------------------
  NLP                                Natural Language Processing                                     Informatikverfahren zur Verarbeitung natürlicher Sprache
  n-Gramm                            Folge aus n Einheiten                                           Klassische statistische Modellierung benachbarter Wörter oder Tokens
  Bigramm / Trigramm                 Wort-/Tokenfolge der Länge 2 oder 3                             Eingeschränkter Kontext klassischer n-Gramm-Modelle
  Smoothing                          Glättung von Wahrscheinlichkeiten                               Verhindert unter anderem Nullwahrscheinlichkeiten für ungesehene Fälle
  Subword-Tokenisierung              Zerlegung in Wortbestandteile                                   Verwendet Wortteile statt nur ganze Wörter als Token-Einheiten
  BPE                                Byte Pair Encoding                                              Verfahren zum schrittweisen Zusammenfassen häufiger Zeichen- oder Bytefolgen
  SentencePiece                      Modell- und Implementierungsfamilie für Subword-Tokenisierung   Kann Tokenisierer direkt auf Rohtext trainieren
  RNN                                Recurrent Neural Network                                        Rekurrentes Netz, das Zustand von einem Sequenzschritt zum nächsten trägt
  BPTT                               Backpropagation Through Time                                    Rückwärtsberechnung von Gradienten durch zeitlich entfaltete rekurrente Netze
  LSTM                               Long Short-Term Memory                                          Rekurrente Architektur mit Gates zur Steuerung des Informationsflusses
  Seq2Seq                            Sequence-to-Sequence                                            Architektur zur Umwandlung einer Sequenz in eine weitere Sequenz
  Encoder                            Eingabeverarbeitung und Repräsentation                          Verwandelt Eingabe in interne Zustände; je nach Architektur mit bidirektionaler Aufmerksamkeit
  Decoder                            Ausgabegenerierender Netzteil                                   Erzeugt Ausgaben schrittweise; je nach Architektur mit Encoderzugriff
  Attention                          Aufmerksamkeitsgewichtung                                       Gewichtet die Beiträge anderer Positionen zu einer Vektordarstellung
  Self-Attention                     Attention innerhalb derselben Sequenz                           Query, Key und Value stammen aus Repräsentationen derselben Folge
  Cross-Attention                    Attention über zwei Folgen/Quellen                              Beispielsweise Decoder-Queries auf Encoder-Keys und -Values
  Query / Key / Value (Q/K/V)        Anfrage- / Schlüssel- / Inhaltsvektoren                         Trainierte Projektionen zum Vergleichen und Mischen von Informationen
  Skalarprodukt                      Dot Product                                                     Multipliziert Vektorkomponenten paarweise und summiert sie
  Softmax                            Normierung von Vergleichswerten                                 Wandelt Scores in nichtnegative Gewichte um, deren Summe 1 ist
  Scaled Dot-Product Attention       Skalierte Skalarprodukt-Aufmerksamkeit                          Bildet Softmax-Gewichte aus $Q\cdot K^{\mathrm T}$ geteilt durch $\sqrt{d_k}$ und mischt Values
  Multi-Head Attention               Mehrköpfige Attention                                           Mehrere separat projizierte Attention-Rechnungen werden zusammengeführt
  Positional Encoding                Positionskodierung                                              Ergänzt Tokenrepräsentationen um Reihenfolgeinformationen
  Feedforward-Schicht                Vorwärtsgerichtetes Teilnetz                                    Bearbeitet die Darstellungen nach Attention positionsweise weiter
  Residual Connection                Restverbindung/Residualpfad                                     Addiert eine Eingabe über einen Teilblock hinweg hinzu
  Layer Normalization                Schichtnormalisierung                                           Normalisiert Werte zur Stabilisierung des Trainings
  Causal Mask                        Kausale Attention-Maske                                         Verhindert Zugriff auf zukünftige Zielpositionen beim autoregressiven Modell
  Autoregressiv                      Nächster Schritt aus bisherigen Schritten                       Generiert Token für Token unter Nutzung der bisherigen Folge
  Encoder-only                       Reiner Encoder-Transformer                                      Häufig für Repräsentation, Klassifikation und Informationsextraktion
  Decoder-only                       Reiner Decoder-Transformer                                      Häufig für kausale Textgenerierung, etwa GPT-Modelle
  Encoder-Decoder                    Kombinierte Transformer-Architektur                             Verarbeitet Eingabe mit Encoder und generiert mit Decoder Ausgabe
  BERT                               Bidirectional Encoder Representations from Transformers         Bekanntes bidirektionales Encoder-Modell mit selbstüberwachtem Vortraining
  GPT                                Generative Pre-trained Transformer                              Familie autoregressiver vortrainierter Sprachmodelle
  T5                                 Text-to-Text Transfer Transformer                               Encoder-Decoder-Ansatz, der Sprachaufgaben als Text-zu-Text formt
  VRAM                               Video Random Access Memory                                      Grafikspeicher für Modellgewichte und temporäre Rechenwerte
  RAG                                Retrieval-Augmented Generation                                  Ergänzt Generierung um extern abgerufene Dokumentabschnitte
  Chat-Template                      Gesprächsvorlage für ein Modell                                 Kodiert Rollen und Nachrichten in einer vom Modell erwarteten Eingabeform
  Token-IDs                          Numerische Tokenkennungen                                       Ordnen einem Tokenizer-Vokabular diskrete Einheiten zu
  Kontextfenster                     Context Window                                                  Maximal berücksichtigbarer Tokenkontext bei einer Modellverarbeitung
  Inferenz                           Inference                                                       Ausführen eines bereits trainierten Modells ohne gewöhnliche Gewichtsänderung
  Prefill                            Vorberechnungsphase der Inferenz                                Verarbeitet die bereitgestellte Eingabefolge vor der autoregressiven Ausgabe
  Decoding (LLM)                     Schrittweise Textgenerierung                                    Erzeugung weiterer Tokens abhängig von der bisherigen Folge
  Logit                              Nichtnormierter Modell-Ausgabewert                              Score für eine mögliche nächste Tokeneinheit vor Softmax und Sampling
  Greedy Decoding                    Gierige Tokenauswahl                                            Wählt in jedem Schritt den Kandidaten mit der höchsten Auswahlwahrscheinlichkeit
  Sampling                           Gewichtete Zufallsauswahl                                       Zieht das nächste Token aus einer Wahrscheinlichkeitsverteilung
  Temperatur (LLM)                   Temperature                                                     Skaliert Logits und verändert die Konzentration der Auswahlwahrscheinlichkeiten
  Top-p / Nucleus Sampling           Auswahl nach kumulierter Wahrscheinlichkeit                     Berücksichtigt den kleinsten Kandidatensatz, der mindestens die Schwelle p abdeckt
  Top-k                              Auswahl aus k Kandidaten                                        Beschränkt die Tokenwahl auf die k wahrscheinlichsten Fortsetzungen
  KV-Cache                           Key-Value-Cache                                                 Zwischenspeichert Attention-Zustände früherer Positionen für effizienteres Decoding
  Prefix Caching                     Präfix-Zwischenspeicherung                                      Erlaubt unter geeigneten Bedingungen die Wiederverwendung bereits berechneter Eingabepräfixe
  TTFT                               Time to First Token                                             Zeit bis zum ersten ausgegebenen Token einer Anfrage
  Quantisierung (LLM)                Verringerte Zahlendarstellungspräzision                         Spart unter anderem Speicher für Modellgewichte, kann Qualität und Geschwindigkeit beeinflussen
  Halluzination (LLM)                Sachlich unbelegte oder falsche Modellgenerierung               Plausibel wirkende, aber nicht verlässlich aus Fakten begründete Ausgabe
  Streaming (LLM)                    Schritthafte Übermittlung                                       Zeigt die bereits erzeugte Ausgabe, bevor der gesamte Text fertig ist
  Basismodell (Base Model)           Vortrainiertes Sprachmodell                                     Hat allgemeine Textmuster gelernt, muss aber nicht zuverlässig Anweisungen befolgen
  Assistenzmodell / Instruct Model   Nachtrainiertes dialog- und aufgabenorientiertes Sprachmodell   Wurde auf erwünschte Anweisungsbefolgung und Antwortverhalten angepasst
  Post-Training                      Nachtraining nach allgemeinem Vortraining                       Umfasst je nach Verfahren SFT, Präferenzoptimierung und weitere Lernziele
  Fine-Tuning                        Feinabstimmung eines vortrainierten Modells                     Weitere Gewichts- oder Adapteranpassung auf zusätzliche Daten
  SFT                                Supervised Fine-Tuning                                          Überwachte Feinabstimmung mit Beispielen erwünschter Ausgaben
  Instruction Tuning                 Anweisungsorientiertes Nachtraining                             Häufig als SFT auf Anweisungs-Antwort-Daten durchgeführt
  Präferenzdaten                     Vergleichsdaten für erwünschte Antworten                        Kennzeichnen bevorzugte und abgelehnte Modellantworten
  RLHF                               Reinforcement Learning from Human Feedback                      Bestärkendes Lernen, bei dem menschliche Präferenzen das Trainingsziel beeinflussen
  Reward Model                       Belohnungsmodell                                                Schätzt eine Bewertung anhand menschlicher oder anderer Präferenzdaten
  PPO                                Proximal Policy Optimization                                    Optimierungsfamilie für bestärkendes Lernen, unter anderem in klassischen RLHF-Varianten
  KL-Divergenz                       Kullback-Leibler-Divergenz                                      Beschreibt eine gerichtete Abweichung zwischen Wahrscheinlichkeitsverteilungen
  Reward Hacking                     Ausnutzen von Schwächen einer Belohnungskennzahl                Hohe Messwerte können ohne tatsächlichen Nutzgewinn erzielt werden
  DPO                                Direct Preference Optimization                                  Optimiert Präferenzpaare ohne separaten Reward-Model/RL-Schritt im Grundverfahren
  PEFT                               Parameter-Efficient Fine-Tuning                                 Trainiert nur einen kleinen Teil zusätzlicher oder ausgewählter Parameter
  LoRA                               Low-Rank Adaptation                                             Trainiert kleinere Korrekturmatrizen bei eingefrorenen Basismatrizen
  QLoRA                              Quantized Low-Rank Adaptation                                   Kombiniert quantisierte eingefrorene Basisgewichte mit LoRA-Adaptern
  Data Contamination                 Kontamination von Testdaten                                     Testaufgaben sind bereits aus Trainingsdaten bekannt oder sehr ähnlich
  LLM-as-a-Judge                     Sprachmodell als Bewertungsinstanz                              Automatische Bewertung anderer Antworten, selbst fehler- und biasanfällig
  Red Teaming                        Gezielte Untersuchung möglicher Schwachstellen                  Prüft Fehlverhalten, Missbrauchsmöglichkeiten und Sicherheitsgrenzen
  Guardrails                         Zusätzliche Sicherheits- und Kontrollmechanismen                Beispielsweise Zugriffsprüfung, Schema-, Ressourcen- und Freigaberegeln
  Model Card                         Modellkarte                                                     Dokumentiert Einsatzzweck, Testmethoden, bekannte Grenzen und Risiken
  Catastrophic Forgetting            Katastrophales Vergessen                                        Zusatztraining kann bisherige Modellfähigkeiten beeinträchtigen

## M6-L4 – Wissen, Werkzeuge und Agenten sowie Studienstruktur {#S27}

  Begriff                   Erklärung                                                    Bedeutung
  ------------------------- ------------------------------------------------------------ -------------------------------------------------------------------------
  RAG-Pipeline              Retrieval-Augmented Generation mit Abruf und Generierung     Externe Informationen als Kontext, ohne die Modellgewichte zu verändern
  Chunking                  Aufteilen von Dokumenten in kleinere Textabschnitte          Erlaubt gezielten Abruf relevanter Passagen
  Embedding                 Numerische Darstellung eines Textes oder anderen Inhalts     Grundlage vieler semantischer Suchsysteme
  Vektorsuche               Ähnlichkeitssuche in einem Vektorraum                        Findet semantisch nahe Darstellungen, nicht automatisch wahre Aussagen
  Hybridsuche               Verbindung von Volltext- und Vektorsuche                     Kombiniert exakte Begriffe und semantische Nähe
  Reranking                 Erneute Sortierung von Suchtreffern                          Kann die Passung der gefundenen Kandidaten verbessern
  Tool Calling              Strukturierte Anforderung eines Werkzeugaufrufs              Modell schlägt Aufruf vor, Anwendung prüft und führt aus
  Agentischer Workflow      Mehrstufiger Ablauf mit modellgesteuerter Schrittauswahl     Verknüpft Modell, Werkzeuge, Zustand und Abbruchregeln
  Orchestrator              Koordinierende Anwendungssoftware                            Verwaltet Suche, Modellaufrufe, Berechtigungen und Rückmeldungen
  Prompt Injection          Einschleusen von Anweisungen in Eingaben oder fremde Daten   Sicherheitsgefahr, insbesondere bei Dokumenten und Werkzeugresultaten
  Excessive Agency          Zu weitgehende Werkzeugrechte oder Autonomie                 Vergrößert die Folgen fehlerhafter oder manipulierter Modellaktionen
  Bachelor-Wahlthema        Freiwilliger Vertiefungsbaustein auf Bachelor-Niveau         Eigenständige Wahllektionen in M8–M10
  Master-Wahlthema          Freiwilliger Vertiefungsbaustein auf Master-Niveau           Schwerpunkt auf formalen Modellen, Abwägungen und Forschungsmethoden
  Master-Kernbereich F      Vorgemerkter späterer Informatik-Vertiefungsabschnitt        Noch kein ausgearbeiteter oder akkreditierter Masterstudiengang

## M6-L5 – Multimodale KI: Bild, Video und Audio {#S28}

  Begriff                        Erklärung                                                                Bedeutung
  ------------------------------ ------------------------------------------------------------------------ ---------------------------------------------------------------------------------
  Modalität                      Datenform wie Text, Bild, Video oder Audio                               Multimodale Systeme verarbeiten mehrere Datenformen
  Bildpatch                      Kleines, rechteckiges Teilstück eines Bildes                             Häufige Eingabeeinheit für Bild-Transformer
  Vision-Language-Modell (VLM)   Modell zur gemeinsamen Verarbeitung von visuellen Inhalten und Sprache   Bildfragen, Bildbeschreibungen, Dokumentanalyse
  CLIP                           Contrastive Language–Image Pre-training                                  Bild- und Textdarstellungen werden über passende Paare ausgerichtet
  Gemeinsamer Embedding-Raum     Vergleichbarer numerischer Merkmalsraum für mehrere Datenarten           Ermöglicht bildübergreifende Suche und Ähnlichkeitsvergleiche
  Diffusionsmodell               Generatives Modell mit schrittweiser Entrauschung                        Bild-, Video- und auch Audioerzeugung
  Latenter Raum                  Gelernter numerischer Merkmalsraum                                       Kann die aufwendige Generierung kompakter organisieren
  Autoencoder                    Encoder mit passendem Decoder für Rekonstruktion                         Oft zur Bildkompression in generativen Systemen
  VAE                            Variational Autoencoder                                                  Probabilistische Autoencoder-Familie, in manchen latenten Bildverfahren genutzt
  Conditioning                   Steuerung einer Generierung durch zusätzliche Eingaben                   Beispielsweise Text, Skizzen oder Referenzbilder
  Inpainting                     Neugenerierung eines ausgewählten Bildbereichs                           Kontrollierte Bildbearbeitung
  Outpainting                    Erweiterung eines Bildes über bisherige Ränder hinaus                    Szenenerweiterung
  Frame                          Einzelbild einer Videofolge                                              Zeitliche Konsistenz entsteht aus Beziehungen zwischen Frames
  Zeitliche Konsistenz           Erhaltung sinnvoller Beziehungen über die Zeit                           Wichtig für Figurenidentität, Bewegung und Szenenlogik
  Sample / Abtastrate            Digitaler Messwert / Messwerte pro Sekunde                               Grundlage digitaler Audiosignale
  Spektrogramm                   Darstellung von Frequenzanteilen über die Zeit                           Häufige Zwischendarstellung für Audio-KI
  ASR                            Automatic Speech Recognition                                             Umwandlung gesprochener Sprache in Text
  TTS                            Text-to-Speech                                                           Umwandlung von Text in gesprochene Sprache
  Vocoder                        Erzeugt Audio-Wellenformen aus akustischen Merkmalen                     Teil bestimmter Sprachsynthesearchitekturen
  Prosodie                       Betonung, Rhythmus, Melodie und Pausen von Sprache                       Wichtig für Natürlichkeit synthetischer Stimmen
  C2PA / Content Credentials     Standards und technische Herkunftshinweise für Medien                    Unterstützen prüfbare Provenienz, beweisen nicht Inhaltwahrheit
  Muxing                         Zusammenführen mehrerer Medienspuren in einen Container                  Teil der Video-/Audio-Produktionspipeline

## M6-L6 – KI-Infrastruktur und verteilte Berechnung {#S29}

  Begriff                  Erklärung                                                                               Bedeutung
  ------------------------ --------------------------------------------------------------------------------------- ---------------------------------------------------------------------
  Inferenz                 Anwendung eines bereits trainierten Modells ohne gewöhnliche Änderung seiner Gewichte   Grundlage für Chat, Bildanalyse und viele KI-Dienste
  Trainings-Checkpoint     Gesicherter Trainingszustand mit je nach Verfahren Gewichten und weiteren Zuständen     Wiederaufnahme nach Fehlern oder Unterbrechungen
  Speicherbandbreite       Übertragbare Datenmenge je Zeiteinheit zwischen Speicher und Recheneinheiten            Kann Modellgeschwindigkeit begrenzen
  Memory-bound             Vorwiegend durch Datentransport/Speicherzugriff begrenzte Berechnung                    Mehr Recheneinheiten allein helfen wenig
  Compute-bound            Vorwiegend durch eigentliche Rechenoperationen begrenzte Berechnung                     Andere Beschleunigungsstrategien als bei Speicherengpässen
  Quantisierung            Reduzierte numerische Präzision bei der Speicherung/Verarbeitung von Modellwerten       Kann Speicher sparen, je nach Verfahren Qualität beeinflussen
  TPOT                     Time per Output Token                                                                   Mittlere Zeit je weiterem generiertem Token
  Continuous Batching      Dynamisches Zusammenfassen aktiver Modellanfragen                                       Bessere Nutzung des Inferenzservers bei passender Last
  PagedAttention           Blockorientierte Verwaltung von Attention-KV-Cache-Speicher                             Dient effizienterer Cache-Verwaltung bei passenden Engines
  Task-Parallelität        Unabhängige Rechenaufträge auf mehrere Worker verteilen                                 Einfacher Ausbau der parallelen Auftragsbearbeitung
  Datenparallelität (KI)   Vollständige Modellkopien bearbeiten unterschiedliche Trainingsdaten                    Gradienten werden synchronisiert; Modell muss pro Kopie passen
  DDP                      Distributed Data Parallel                                                               PyTorch-Verfahren zur synchronisierten Datenparallelität
  Modellparallelität       Parameter oder Rechenschritte eines Modells auf Geräte verteilen                        Hilft bei großen Modellen; erfordert Kommunikation
  Tensorparallelität       Aufteilung von Tensoroperationen über mehrere Geräte                                    Teilergebnisse können Synchronisation benötigen
  Pipelineparallelität     Verteilung aufeinanderfolgender Modellschichten auf mehrere Geräte                      Zwischenergebnisse werden weitergereicht
  FSDP                     Fully Sharded Data Parallelism                                                          Aufgeteilte Modell- und Trainingszustände bei verteilter Berechnung
  AllReduce                Zusammenführen und Verteilen aggregierter Werte zwischen Teilnehmern                    Beispielsweise Gradientenabgleich
  NCCL                     NVIDIA Collective Communications Library                                                Kommunikationsbibliothek für unterstützte NVIDIA-GPU-Gruppen
  Expert Parallelism       Verteilung von Experten in Mixture-of-Experts-Modellen                                  Erfordert geeignete Routing- und Lastplanung
  Device Plugin            Erweiterung einer Clustersteuerung zur Nutzung spezieller Hardware                      Kubernetes kann damit GPUs planen
  Serving-Replikat         Eigene laufende Instanz eines Modells/Servingsystems                                    Bearbeitet unabhängig Anfragen, benötigt eigene Ressourcen

## M6-L7 – Robotik: Vom Sprachmodell zur handelnden Maschine {#S30}

  Begriff                    Erklärung                                                           Bedeutung
  -------------------------- ------------------------------------------------------------------- -----------------------------------------------------------------
  Roboter                    Programmierbares physisches System mit Sensoren und Aktoren         Nimmt Umgebung auf und wirkt mechanisch auf sie ein
  Aktor                      Bauteil, das Bewegung oder Wirkung erzeugt                          Motor, Greifer oder Ventil
  Encoder                    Sensor zur Messung von Drehwinkel/-bewegung                         Rückmeldung für Motor- und Positionsregelung
  IMU                        Inertial Measurement Unit                                           Misst unter anderem Beschleunigung und Drehbewegung
  LiDAR                      Light Detection and Ranging                                         Optische Entfernungsmessung zur Umgebungswahrnehmung
  Regelkreis                 Rückgekoppelte Steuerung aus Sollwert, Istwert und Regler           Korrigiert Abweichungen während der Bewegung
  PID-Regler                 Proportional-Integral-Differenzial-Regler                           Klassisches Regelungsverfahren mit mehreren Korrekturanteilen
  Echtzeit                   Zeitliche Fristen als Teil der korrekten Systemfunktion             Wichtig für vorhersagbare Steuerung und Reaktion
  Pose                       Position und Orientierung eines Objekts oder Roboters               Grundlage für Lokalisierung und Greifplanung
  Sensordatenfusion          Verbindung mehrerer Messquellen zu einer Zustandsschätzung          Reduziert bestimmte Messunsicherheiten
  SLAM                       Simultaneous Localization and Mapping                               Gleichzeitige Eigenortung und Kartenerstellung
  Odometriedrift             Auflaufen von Positionsfehlern aus Bewegungsmessungen               Macht ergänzende Ortungsverfahren notwendig
  Pfadplanung                Suche nach einer befahrbaren/verfolgbaren Route                     Grundlage mobiler Navigation
  Kinematik                  Geometrische Beziehungen zwischen Gelenken und Körperlagen          Rechnet Gelenkwinkel und Zielposen um
  Endeffektor                Werkzeug am Ende eines Robotermanipulators                          Beispielsweise ein Greifer
  ROS 2                      Robot Operating System 2                                            Softwareframework für Robotikkomponenten und ihre Kommunikation
  Node / Knoten              Einzelne ROS-2-Komponente                                           Sensor, Planung oder Steuerung als logische Einheit
  Topic                      Kontinuierlicher Nachrichtenstrom in ROS 2                          Sensordaten und Status als Publish/Subscribe
  Service                    Kurze Anfrage-/Antwortoperation in ROS 2                            Statusabfrage oder Einzelberechnung
  Action                     Länger laufender Auftrag mit Rückmeldungen und Ergebnis             Beispielsweise Navigation zu einem Ziel
  QoS                        Quality of Service                                                  Konfigurierbare Übertragungseigenschaften von Nachrichten
  Nav2                       Navigation2                                                         ROS-2-basierter Baukasten für mobile Navigation
  MoveIt 2                   Framework für robotische Manipulation                               Kinematik, Bewegungsplanung und Kollisionsprüfung
  ros2_control               ROS-2-Hardware-/Controllerframework                                 Bindet Regler und Antriebe aneinander an
  Behavior Tree              Verhaltensbaum für aufeinander abgestimmte Teilaufgaben             Strukturiert Navigations- und Fehlerabläufe
  Edge Computing (Robotik)   Rechenleistung direkt an der Maschine                               Erlaubt kurze und netzunabhängige Verarbeitung
  VLA                        Vision-Language-Action                                              Forschungsansatz für Modelle aus Bild, Sprache und Aktionen
  Funktionale Sicherheit     Sicherheitsfunktionen und Fehlerbehandlung nach Risikobetrachtung   Unabhängig von der Qualität einer LLM-Antwort zu betrachten
  OTA-Update                 Over-the-Air-Update                                                 Fernaktualisierung von Geräte-Software
  Telemetrie                 Übertragene Betriebs- und Zustandsmessungen                         Monitoring und Wartung von Robotern und Flotten

## M9-L1 – Benutzeroberflächen, Barrierefreiheit und Softwareergonomie {#S31}

  Begriff                   Erklärung                                                                   Bedeutung
  ------------------------- --------------------------------------------------------------------------- ----------------------------------------------------------------------
  UI                        User Interface, Benutzeroberfläche                                          Bedienelemente zur Interaktion mit einem System
  UX                        User Experience, Nutzungserlebnis                                           Umfasst Erwartungen und tatsächliche Erfahrung der Nutzung
  HCI                       Human–Computer Interaction                                                  Forschungsgebiet der Mensch-Computer-Interaktion
  Usability                 Gebrauchstauglichkeit                                                       Wirksame, effiziente und zufriedenstellende Nutzung in einem Kontext
  Accessibility             Barrierefreiheit                                                            Zugänglichkeit für Menschen mit unterschiedlichen Voraussetzungen
  Informationsarchitektur   Systematischer Aufbau von Inhalten und Navigation                           Erleichtert Auffinden und Einordnen
  Mentales Modell           Vorstellung von der Funktionsweise eines Systems                            Bestimmt Erwartungen und Bedienverhalten
  Affordanz                 Wahrnehmbare Handlungsmöglichkeit eines Elements                            Hilft, Interaktionen zu erkennen
  Progressive Disclosure    Schrittweise Offenlegung komplexerer Funktionen                             Reduziert anfängliche Informationslast
  Designsystem              Gemeinsame Regeln und Komponenten der Gestaltung                            Unterstützt Konsistenz und Pflege
  WCAG                      Web Content Accessibility Guidelines                                        W3C-Richtlinien mit überprüfbaren Erfolgskriterien
  W3C                       World Wide Web Consortium                                                   Standardisierungsgremium für Webtechnologien
  ARIA                      Accessible Rich Internet Applications                                       Semantische Rollen und Zustände für unterstützende Technik
  Screenreader              Software, die strukturierte Inhalte akustisch oder per Braille vermittelt   Erfordert zugängliche Namen, Rollen und Zustände
  Tastaturfokus             Aktuell mit Tastatur angesprochenes Element                                 Muss sichtbar und sinnvoll erreichbar sein
  Kontrastverhältnis        Verhältnis der relativen Helligkeiten zweier Farben                         Hilft, Lesbarkeit zu beurteilen
  Responsive Design         Layoutanpassung an Geräte und Darstellungsflächen                           Funktioniert auf mobilen und großen Bildschirmen
  Usability-Test            Beobachtete Bearbeitung konkreter Aufgaben                                  Ermittelt Erfolge, Probleme und Nutzungserfahrungen
  Heuristische Evaluation   Fachliche Prüfung anhand von Gestaltungsregeln                              Ergänzt, ersetzt aber keine Nutzertests
  EAA                       European Accessibility Act                                                  EU-Rechtsrahmen für bestimmte barrierefreie Produkte/Dienste
  BFSG                      Barrierefreiheitsstärkungsgesetz                                            Deutscher Rechtsrahmen zur Umsetzung relevanter EAA-Anforderungen
  Prozentpunkte             Absolute Differenz zweier Prozentwerte                                      90 % − 60 % = 30 Prozentpunkte

## M9-L2 – Datenanalyse, Visualisierung und statistisches Denken {#S32}

  Begriff                     Erklärung                                                         Bedeutung
  --------------------------- ----------------------------------------------------------------- ---------------------------------------------------------------------
  Beobachtungseinheit         Was eine Datenzeile repräsentiert                                 Person, Auftrag, Datei oder Messereignis nicht verwechseln
  Datenbereinigung            Nachvollziehbare Behandlung von Datenproblemen                    Einheiten, Dubletten und fehlende Werte prüfen
  NULL / fehlender Wert       Keine vorliegende Angabe                                          Nicht mit dem Zahlenwert Null gleichsetzen
  Deskriptive Statistik       Beschreibung beobachteter Daten                                   Lage, Häufigkeit und Streuung
  Arithmetischer Mittelwert   Summe der Werte geteilt durch Anzahl                              Empfindlich gegenüber großen Extremwerten
  Median                      Zentraler Wert einer sortierten Folge                             Robuster gegenüber einzelnen Ausreißern
  Modus                       Häufigster beobachteter Wert                                      Auch für Kategorien sinnvoll
  Quartil                     Trennpunkt in einer sortierten Werteverteilung                    Quantilkonvention angeben
  IQR                         Interquartilsabstand                                              Differenz zwischen oberem und unterem Quartil
  Varianz                     Mittlerer quadrierter Abstand vom Mittelwert                      Populations-/Stichprobenformeln unterscheiden
  Standardabweichung          Quadratwurzel der Varianz                                         Streuung in der ursprünglichen Einheit
  Gewichtetes Mittel          Mittelwert mit unterschiedlichen Fallgewichten                    Gruppenstärken korrekt berücksichtigen
  Grundgesamtheit             Alle für die Frage relevanten Einheiten                           Zielmenge statistischer Aussagen
  Stichprobe                  Untersuchte Teilmenge der Grundgesamtheit                         Auswahl bestimmt die Aussagekraft
  Auswahlbias                 Systematische Verzerrung der Auswahl                              Mehr Daten allein heilen Bias nicht
  Stichprobenfehler           Schwankungen durch Auswahl einer Teilmenge                        Vom Mess- und Nichtstichprobenfehler unterscheiden
  Standardfehler              Streuung einer Schätzgröße über gedachte Stichproben              Grundlage von Unsicherheitsintervallen
  Konfidenzintervall          Schätzintervall nach Verfahren mit definierter Überdeckungsrate   Kein Wahrscheinlichkeitsurteil über den bereits fixierten Parameter
  Basisrate                   Häufigkeit eines Ereignisses in der Ausgangsmenge                 Wichtig für die Bewertung seltener Warnungen
  Korrelation                 Statistischer Zusammenhang zweier Größen                          Ist kein Kausalitätsnachweis
  Kausalität                  Ursache-Wirkungs-Beziehung                                        Erfordert geeignete Studiendesigns
  Simpsons Paradoxon          Richtungsumkehr von Gruppenvergleichen bei Aggregation            Gruppenzusammensetzung prüfen
  Zeitreihe                   Messwerte in zeitlicher Reihenfolge                               Trends, Saisonalität und Messfenster beachten
  Histogramm                  Verteilung numerischer Werte in Intervallen                       Klassenbreiten beeinflussen die Darstellung
  Streudiagramm               Darstellung von Paaren zweier Messgrößen                          Zusammenhänge und Ausreißer erkennen
  p-Wert                      Modellbezogene Überraschung der Daten unter einer Nullhypothese   Kein Wahrheitswahrscheinlichkeitsmaß
  A/B-Test                    Geplanter Vergleich zweier Varianten                              Zuweisung, Zielgröße und Laufzeit vorab festlegen
  Data Leakage                Unzulässiger Informationsfluss in Training und Evaluation         Verhindert glaubwürdige Modellprüfungen
  Data Drift                  Veränderung der Eingabeverteilung über Zeit                       Qualität und Monitoring können betroffen sein
  Concept Drift               Änderung des Zusammenhangs zwischen Eingaben und Ziel             Modell kann bei gleichen Metriken veralten

## M9-L3 – Eingebettete Systeme, Sensoren und Mikrocontroller {#S33}

  Begriff           Langform / Bedeutung                                   Kurzerklärung
  ----------------- ------------------------------------------------------ ---------------------------------------------------------------------
  Embedded System   Eingebettetes System                                   Rechner mit spezifischer Aufgabe in einem technischen Gerät
  MCU               Microcontroller Unit                                   Chip mit Prozessor, Speicher und Geräteschnittstellen
  SoC               System on a Chip                                       Mehrere Rechner- und Peripheriekomponenten in einem Chip
  GPIO              General-Purpose Input/Output                           Konfigurierbarer digitaler Ein-/Ausgang
  ADC               Analog-to-Digital Converter                            Wandelt analoge Spannungen in digitale Werte
  Quantisierung     Abbildung kontinuierlicher Werte auf digitale Stufen   Auflösung ist keine garantierte Genauigkeit
  PWM               Pulse Width Modulation                                 Steuert Tastgrad digitaler Pulse
  Tastgrad          Duty Cycle                                             Anteil der Einschaltzeit an einer PWM-Periode
  UART              Universal Asynchronous Receiver-Transmitter            Serielle asynchrone Übertragung
  I²C               Inter-Integrated Circuit                               Zweidraht-Bus mit adressierten Teilnehmern
  SPI               Serial Peripheral Interface                            Serielle Peripherieschnittstelle mit Takt und Datenleitungen
  CAN               Controller Area Network                                Nachrichtenorientierter Feldbus für Maschinen und Fahrzeuge
  Interrupt         Hardware-/Software-Unterbrechungsanforderung           Ruft einen passenden Handler zur Ereignisbehandlung auf
  NVIC              Nested Vectored Interrupt Controller                   Interruptsteuerung in vielen Arm-Cortex-M-Prozessoren
  DMA               Direct Memory Access                                   Datentransfer durch Hardware ohne CPU-Kopie jedes Bytes
  RTOS              Real-Time Operating System                             Betriebssystem für zeitkritische eingebettete Aufgaben
  Deadline          Echtzeitfrist                                          Bis wann ein Ergebnis verfügbar sein muss
  Jitter            Schwankung der Verzögerung                             Zeitliche Unregelmäßigkeit wiederholter Ereignisse
  Watchdog          Ablaufüberwachung                                      Kann ausgefallene Programmausführung erkennen und Neustart anstoßen
  Brownout          Unterspannungsereignis                                 Versorgungsspannung fällt unter zulässigen Betriebspunkt
  OTA               Over-the-Air-Update                                    Übertragung neuer Firmware über eine Verbindung
  IoT               Internet of Things                                     Vernetzte Geräte mit Sensoren oder Aktoren
  Sensorfusion      Kombinierte Auswertung mehrerer Sensoren               Verbessert unter geeigneten Annahmen die Zustandsschätzung
  IMU               Inertial Measurement Unit                              Sensorpaket für Beschleunigung und Drehbewegung

## Fachbegriffe aus M7-L4 – Architektur, Datenschutz und Risiko {#S34}

  Begriff                                    Kurzdefinition                                                                             Wichtige Grenze
  ------------------------------------------ ------------------------------------------------------------------------------------------ --------------------------------------------------------------
  Architekturentscheidung / ADR              Dokumentierte Wahl mit Kontext, Alternativen und Konsequenzen                              Kein Ersatz für spätere Neubewertung
  Qualitätsanforderung                       Messbares oder anderweitig prüfbares Gütekriterium eines Systems                           „Schnell“ allein ist nicht messbar
  Trust Boundary / Vertrauensgrenze          Übergang zwischen Bereichen mit unterschiedlichen Sicherheitsannahmen                      Interne Netzlage begründet nicht automatisch Vertrauen
  STRIDE                                     Klassifikation technischer Bedrohungen in sechs Gruppen                                    Nicht vollständig für Datenschutz- und Organisationsrisiken
  Threat Modeling / Bedrohungsmodellierung   Systematische Untersuchung von Werten, Bedrohungen und möglichen Schutzmaßnahmen           Keine Garantie, alle Angriffe vorherzusehen
  Least Privilege                            Nur erforderliche Zugriffsrechte vergeben                                                  Erfordert Pflege bei wechselnden Aufgaben
  Zero Trust                                 Keine implizite Vertrauensgewährung allein aufgrund von Standort oder Netzzone             Kein einzelnes Produkt und keine Allzweckgarantie
  Row-Level Security (RLS)                   Datenbankrichtlinien, die den Zugriff auf einzelne Tabellenzeilen einschränken             Besitzer und privilegierte Rollen können ausgenommen sein
  RPO                                        Recovery Point Objective – angestrebter maximal tolerierter Datenverlust als Zeitfenster   Nicht mit Wiederherstellungsdauer verwechseln
  RTO                                        Recovery Time Objective – angestrebte Zeit bis zum Wiederanlauf                            Ein Ziel ist ohne Restore-Test noch keine bewiesene Zusage
  Datenminimierung                           Daten nur im für den Zweck nötigen Umfang verarbeiten                                      Rechtsgrundlage und Zweckbindung bleiben gesondert zu prüfen
  Sensitivitätsanalyse                       Prüfen, wie eine Entscheidung bei veränderten Annahmen ausfällt                            Bereinigt keine falsch gewählten Kriterien
  Pareto-Dominanz                            Alternative ist in allen Kriterien mindestens gleich gut und in einem besser               Ohne klare Kriterien gibt es keinen sinnvollen Vergleich
  Defense in Depth                           Mehrere voneinander unabhängige Sicherheitsmaßnahmen kombinieren                           Eine Schicht darf Fehler anderer nicht verdecken

## Fachbegriffe aus M7-L5 – wissenschaftliche Bewertung von KI-Systemen {#S35}

  Begriff            Kurzdefinition                                                        Aussagegrenze
  ------------------ --------------------------------------------------------------------- -----------------------------------------------------
  Evaluation         Systematische Bewertung anhand definierter Ziele und Daten            Eine Kennzahl bildet nicht alle Eigenschaften ab
  Benchmark          Standardisierte Vergleichsaufgaben mit Auswertung                     Nicht automatisch repräsentativ für jeden Einsatz
  Population         Menge aller Fälle, für die eine Aussage gelten soll                   Nicht mit beobachteter Stichprobe identisch
  Ground Truth       Als Referenz verwendetes Label oder Ergebnis                          Kann selbst ungenau oder strittig sein
  Konfusionsmatrix   Tabelle richtig/falsch positiver und negativer Fälle                  Nur bezogen auf festgelegte positive Klasse
  Accuracy           Anteil aller richtig klassifizierten Fälle                            Kann bei seltenen Zielklassen täuschen
  Precision          TP geteilt durch alle positiv vorhergesagten Fälle                    Nicht gleich Recall
  Recall             Anteil erkannter tatsächlich positiver Fälle                          Nicht gleich Precision
  F1-Score           Harmonisches Mittel aus Precision und Recall                          Bezieht TN und Fehlkosten nicht direkt ein
  Basisrate          Häufigkeit einer Klasse in der Zielpopulation                         Beeinflusst die Interpretierbarkeit der Precision
  Kalibrierung       Übereinstimmung geschätzter Wahrscheinlichkeiten mit Häufigkeiten     Sprachliches Selbstvertrauen ist keine Kalibrierung
  Generalisierung    Leistung auf passenden, ungesehenen Fällen                            Muss für Zielverteilung geprüft werden
  Data Leakage       Unzulässiger Informationsfluss zwischen Daten und Auswertung          Künstlich gute Testresultate möglich
  Concept Drift      Veränderung der Beziehung zwischen Eingangsdaten und Ziel             Nicht dasselbe wie nur veränderte Klassenhäufigkeit
  OOD                Out-of-Distribution – deutlich untypische Eingaben                    Erfolg auf Testdaten garantiert OOD-Leistung nicht
  Slice-Analyse      Gesonderte Fehlerprüfung fachlich relevanter Untergruppen             Kleine Gruppen erhöhen die Unsicherheit
  LLM-as-a-Judge     Sprachmodell beurteilt generierte Ergebnisse                          Urteilsbias, Referenz und Rubrik prüfen
  RAG-Evaluation     Getrennte Prüfung von Dokumentensuche, Belegen und Antwort            Gute Suche bedeutet nicht zwingend richtige Antwort
  Model Card         Standardisierte Dokumentation von Modellzweck, Leistung und Grenzen   Keine Zertifizierung oder universelle Garantie
  AI RMF             NIST-Rahmenwerk zum KI-Risikomanagement                               Freiwillige Leitlinie, kein Modellgütesiegel

## Fachbegriffe aus M7-L6 – Systemübergreifende Synthese und Forschungsmethoden {#S36}

  Begriff                        Kurzdefinition                                                                    Wichtige Grenze
  ------------------------------ --------------------------------------------------------------------------------- --------------------------------------------------------------
  Systemübergreifende Synthese   Verknüpfung von Erkenntnissen über mehrere technische Teilbereiche                Gute Einzelergebnisse garantieren kein gutes Gesamtsystem
  Design Science                 Forschung durch Gestaltung und Evaluation zweckgerichteter Artefakte              Gewöhnliche Programmierung ist nicht automatisch Forschung
  Forschungsfrage                Genau abgegrenzte, methodisch untersuchbare Fragestellung                         „Besser“ ohne Kriterium ist nicht prüfbar
  Hypothese                      Überprüfbare Annahme mit möglichen Widerlegungsbefunden                           Keine bereits bewiesene Tatsache
  Deduktiver Beweis              Logische Ableitung aus Axiomen und Voraussetzungen                                Gilt innerhalb des zugrunde gelegten Modells
  Empirische Messung             Beobachtung tatsächlicher Systemabläufe                                           Abhängig von Messmethode, Stichprobe und Kontext
  Versuchsdesign / DoE           Regeln für vergleichbare, auswertbare Untersuchungen                              Unkontrollierte Störgrößen können Unterschiede vortäuschen
  Confounder / Störgröße         Einfluss, der systematisch mit der untersuchten Veränderung variiert              Kann kausale Schlussfolgerungen verzerren
  Randomisierung                 Zufallszuordnung oder zufällige Reihenfolge im Versuchsplan                       Ersetzt keine geeignete Stichprobe
  Blockbildung                   Vergleich innerhalb möglichst ähnlicher Versuchsgruppen                           Falsch gewählte Gruppen können Unterschiede verdecken
  End-to-End                     Betrachtung der vollständigen Wirkungskette bis zum Nutzerergebnis                Komponentenwerte sind nicht automatisch Gesamtwerte
  Tail Latency                   Langsame Randbereiche einer Laufzeitverteilung                                    Mittelwert verdeckt problematische Ausreißer
  SLI                            Service Level Indicator: gemessene Qualitätskenngröße eines Dienstes              Nur sinnvoll mit genauer Messdefinition
  SLO                            Service Level Objective: vereinbarter Zielwert für einen SLI                      Ziel ist kein Nachweis realer Erfüllung
  Pareto-Dominanz                Eine Variante ist in keinem Kriterium schlechter und in mindestens einem besser   Kriterien und harten Grenzen zuerst bestimmen
  Entscheidungsmatrix            Transparente Abwägung mehrerer Kriterien und Gewichtungen                         Subjektive Punkte sind keine objektiven Tatsachen
  Sensitivitätsanalyse           Untersucht Entscheidungen unter veränderten Annahmen                              Rettet keine fehlerhafte Forschungsfrage
  TCO                            Total Cost of Ownership: Gesamtkosten über betrachtete Zeit                       Ein monatlicher Cloudpreis ist kein vollständiger TCO
  Reproduzierbarkeit             Nach National Academies: konsistente Rechnung mit denselben Daten und Methoden    Begriff wird fachgebietsspezifisch unterschiedlich verwendet
  Replikation                    Neue Untersuchung derselben Frage mit eigenen Daten                               Gleiches Ergebnis nicht für jede Population garantiert
  Generalisierbarkeit            Übertragbarkeit von Erkenntnissen auf andere Kontexte                             Muss zusätzlich begründet werden
  Forschungsartefakt             Nachprüfbarer Bestandteil einer Untersuchung (Code, Daten, Verfahren)             Veröffentlichbarkeit kann durch Rechte begrenzt sein
  FAIR                           Findable, Accessible, Interoperable, Reusable                                     Zugänglich ist nicht zwangsläufig öffentlich
  ADR                            Architecture Decision Record: dokumentierter Architekturentscheid                 Dokumentation ersetzt keine Neubewertung bei Änderungen

## M8-L4 – Algorithmen und Datenstrukturen vertieft {#S37}

| Begriff | Bedeutung | Wichtig |
| --- | --- | --- |
| AVL-Baum | Binärer Suchbaum mit Höhenunterschied höchstens eins je Knoten | Rotation erhält Schlüsselordnung |
| Balancefaktor | Höhe des linken minus Höhe des rechten Teilbaums | In einem AVL-Baum nur -1, 0 oder 1 |
| Rot-Schwarz-Baum | Suchbaum mit Farb- und Schwarzhöheninvarianten | Logarithmische Höhenschranke |
| Schwarzhöhe | Anzahl schwarzer Knoten auf einem Pfad gemäß festgelegter Zählweise | Auf allen Pfaden desselben Ausgangsknotens gleich |
| Rotation | Lokale Umstrukturierung eines Suchbaums | Inorder-Reihenfolge bleibt erhalten |
| Min-Heap | Vollständiger Binärbaum mit Elternschlüssel höchstens so groß wie Kindschlüssel | Minimum an der Wurzel, keine vollständige Sortierung |
| Prioritätswarteschlange | Abstrakter Datentyp für Auswahl nach Priorität | Kann mit Heap implementiert werden |

Weiterführend: [M8-L4](../M8-L4.md).
