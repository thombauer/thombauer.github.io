---
layout: post
title: MLOps - Skalierung, Automatisierung und Transparenz für Machine Learning Pipelines.
cover-img: /assets/img/grey_wall.jpg
tags: [data science, analytics, python, mlops]
---

MLOps ist ein Prozess der Organisationen hilft langfristigen Wert mit Machine Learning Komponenten zu schaffen und gleichzeitig die mit der Entwicklung verbundenen Risiken zu reduzieren. MLOps ist essentiell für eine erfolgreiche Data Science Strategie eines Unternehmens - es ist die Standardisierung des ML-Lifecycle-Managements, also eines mehr oder weniger geradlinigen Weges vom Businessproblem zum Machine Learning Modell in Produktion. Allerdings ist es allen voran die Skalierung dieses Liefcycles, mit der die Probleme enstehen. Traditionelle Unternehmen haben vor allem Schwierigkeiten mit vielen parallelen produktiven ML-Modellen. Zusätzliche Probleme entstehen auch mit automatisierten Entscheidungen in ehemals menschlichen Prozessen, die ML-Modelle kritischer für das gesamte Geschäftsmodell traditioneller Unternehmen machen. 

In Anlehnung an DevOps dreht sich MLOps um robuste Automatisierung, die Idee einer engen Zusammenarbeit und häufigen Kommunikation zwischen Teams und Einheiten, einen end-to-end-Lifecycle jedes Services und kontinuierliche Auslieferung in hoher Qualität. Es gibt allerdings einen entscheidenden Unterschied zwischen der Produktivsetzung von Software und der von Machine Learning Modellen. Der Code einer Softwareapplikation ist relativ stabil, die Daten der ML-Modelle hingegen verändern sich stetig. Die ML-Modelle lernen und passen sich ständig an neue Inputs an - sie bestehen aus Code UND Daten, das macht MLOps zu einer neuen Disziplin.

Wie so häufig sollte die Vision für MLOps aus dem Management kommen, wenn es erkennt, dass Machine Learning ein immer wichtigerer Teil des Geschäftes wird und viele (Kern-)Prozesse auf verlässliche ML-Modelle angewiesen sind. Diese klare Vision und strategische Roadmap muss verständlich kommuniziert werden. Die Kooperation zwischen den "Silos" der unterschiedlichen Entwicklerdisziplinen muss gefördert und die kontinuierliche Weiterentwicklung/Verbesserung muss angeregt werden. Zuletzt braucht es viel Freiraum und eine offene Feedbackkultur.

Mit einer stark steigenden Anzahl von ML-Modellen in Produktion erhöht sich der Bedarf nach einer strikten Befolgung der minimalen MLOps-Regeln. Für Data Scientists und das Management ist es essentiell zu wissen, welche ML-Modelle in Produktion gegeben wurden und welchen Einfluss sie auf das konkrete produktive Geschäft des Businesses haben. Zusätzlich sollten Stakeholder in der Lage sein, tiefer einzusteigen und alle Schritte von den Rohdaten hin zu den finalen Modelloutputs zu verstehen. MLOps ist in der Lage, diese Transparenz und Rechenschaft herzustellen.

Title Foto von: <span><a href="https://unsplash.com/@helloimnik?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Hello I'm Nik</a> auf <a href="https://unsplash.com/de/s/fotos/business-success?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span>

## MLOps: Herausforderungen und Nutzen

Die Automatisierung der Modellpipelines ausbauen, den Wert der ML-Modelle für den Business Case voll ausschöpfen, innovative und sich schnell entwickelnde Konzepte mit Hilfe moderner Tools nutzen. Das klingt fantastisch, allerdings bringt der Schritt von lokaler Modellentwicklung zu einer hochautomatisierten MLOps-Pipeline einige Herausforderungen mit sich.

### Herausforderungen von MLOps:
1. Es bestehen sehr viele Abhängigkeiten: Daten verändern sich ständig, Bedürfnisse im Business entwickeln sich. Ergebnisse brauchen ständige Schlaufen mit dem Business, um sicherzustellen, dass die Vorhersagen zu den Erwartungen passen und die in der Konzeptphase (und mittlerweile schon längst angepassten) gesetzten Ziele erreichen.
2. Es ist eine Vielzahl von Rollen involviert: Kommunikation und gemeinsames Verständnis komplexer Probleme sind herausfordernd. Nicht alle Beteiligten nutzen die gleichen Tools oder haben die gleichen Verständnishintergründe. MLOps ist ständig in Bewegung und noch stärker als Data Science eine Aufgabe an kritischen Schnittstellen mit vielen Beteiligten aus unterschiedlichen Disziplinen.
3. Data Scientists sind meist keine Software Engineers: oft fehlt Expertise im Schreiben von Applikationen. Mit der Zeit werden Data Scientists besser im Bereich Deployment oder im Betrieb der Modelle, aber diese Rollen neben Daten- und Modellentwicklung voll auszufüllen ist herausfordernd. Vor allem neben den sich ständig entwickelnden Methoden im Bereich Machine Learning auch noch Data Engineering und Software Engineering im Blick zu behalten ist nur in gewissem Umfang möglich.

Es gibt aber viel mehr Gründe sich mit MLOps auseinanderzusetzen, als sich von den Herausforderungen abschrecken zu lassen. Ab einer gewissen Menge von Machine Learning Modellen im Unternehmen und den meist begrenzten personellen Ressourcen führt kein Weg an einer gewissen MLOps-Maturität vorbei. 

### Vorteile durch MLOps:
1. Skalierung des Designs, der Entwicklung und des Deployments von ML-Modellen hin zu einem effizienten Prozess - eine Voraussetzung um eine Vielzahl von ML-Modellen parallel zu betreiben.
2. Automatisierung möglichst vieler Teilschritte im Prozess. 
3. Stabilität der ML-Modelle, auch bei Weiterentwicklungen und notwendigen Anpassungen an der Infrastruktur.
4. Niedrigere Betriebsaufwände, geringe Aufwände für Anpassungen und viele weitere Effizienzsteigerungen.
5. Definition eines festen Prozesses um Business Value mithilfe von ML-Modellen zu generieren.
6. Risiken mitigieren und Transparenz schaffen. Schon heute wichtig, mit zukünftigen regulatorischen Einschränkungen immer bedeutsamer.

![rolle](/assets/img/roles.jpg)
<span>Foto von <a href="https://unsplash.com/@dmjdenise?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Denise Jans</a> auf <a href="https://unsplash.com/de/s/fotos/roles?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span>

## MLOps: Rollen im ML-lifecycle
Die Hauptunterscheidung, die hier zu treffen ist, ist die zwischen Businessrollen und technischen Rollen. Klar ist, alle Rollen haben eigene Verantwortlichkeiten, Aufgaben und Kompetenzen. Funktionieren wird das System aber nur, wenn die Schnittstellen aufgebaut, gepflegt und der professionelle Austausch institutionalisiert werden. Gemeinsame Abnahmen der zentralen Schritte bauen ein stabiles, lernendes Team bestehend aus eigentlich höchst unterschiedlichen Rollenbildern.

### Business-Rollen
1. Business-Stakeholder: treffen Budgetentscheidungen und transportieren die Vision des Business. Formulieren klar definierte Ziele der KI-Anwendung, beschreiben die Problemstellung und evaluieren/validieren entwickelte ML-Modelle. Übernehmen Verantwortung im Monitoring der produktiven ML-Modelle.

2. Fachexperte: konkretes Domainwissen und Unterstützung in der initialen Datenanalyse. Unterstützung beim Feature Engineering und in der Modellevaluation, ebenso beim Monitoring produktiver ML-Modelle. Accuracy/Precision/Recall reichen als Metriken nicht aus! Feedback der Business-Experten wird gebraucht, mit diesem Feedback werden die Modelle optimiert und Veränderungen in der Modellperformance werden mit ihnen gespiegelt.

### Technische Rollen
1. Data Engineer: Verantwortlich für Datenqualität vor und in Design-/Entwicklungs- und Deploymentphase. Sammlung und Bereitstellung von Daten und höchstmöglicher Qualität und Konsistenz. Data Engineers sorgen dafür, dass Daten optimiert in Machine Learning Modellen genutzt werden können. Sie arbeiten eng mit Business-Experten zusammen, erschliessen die richtigen Daten für ML-Projekte und bereiten deren Nutzung vor. MLOps kann massive Effizienzgewinne für diese zentrale Rolle bringen: Transparenz für Modellperformance in Produktion und Kontrolle über Modellspezifische Data Pipelines, um schnell auf unvorhergesehene Probleme reagieren zu können.

2. Data Scientist: vorab Datenanalyse und Feature Engineering, dann zental für die Modellentwicklung und das statistische Monitoring des produktiven Modells. Schwierigkeiten zeigen sich in vielen Organisationen vor allem in Form von Silodaten, Siloprozessen und Silotools. Das macht es schwierig die Arbeit der Data Scientists zu skalieren. Oft stehen Kommunikationsfähigkeiten in den Studiengängen nicht im Vordergrund, durch MLOps wird das aufgebaut. Zentral ist nun Austausch mit Business Experten, formalisierter Austausch mit anderen Experten, geteilte Verantwortung durch Model Ownership und regelmässiger Austausch mit anderen Data Scientists. Transparenz wird in jeder Weise zentral. Essentiell ist die Fähigekeit, in die Daten einzutauchen und diese schnell zu analysieren und anzupassen. Prinzipien, wie schnelle und sichere Modellentwicklung, anhand fester Standards Vertrauen zu Engineers und DevOps schaffen, verbreiten sich schnell. Effizient arbeiten, Standards skalieren, an möglichst wenigen Stellen das Rad neu erfinden.

3. Software Engineer: Verantwortlich für die Deployment-Pipeline und die Einhaltung der best practices von Softwareentwicklung. Sie arbeiten mit Data Scientists und Data Engineers zusammen, um ML-Modelle in grösserem Zusammenhang funktional zu halten. ML-Modelle sind keine stand-alone-Applikationen. Code, train/test und Deployment müssen in ci/cd pipelines passen. Wichtig ist hier, dass Data-Rollen und Software Engineers die gleiche Sprache sprechen.

4. Machine Learning Engineer: vielfältige Rolle mit Anknüpfungspunkten über den gesamten ML-Lifecycle. Traditionelle Data Architects sind verantwortlich für eine umfassende Datenarchitektur, ML-Engineers/Architekten müssen zusätzlich den Zusammenhang zu den Modellen verstehen. Eine sehr kritische Position im ML-Lifecycle, vor allem was Skalierbarkeit und Flexibilität betrifft. Sie haben die Expertise neue Technologie einzuführen, die die Performance der ML-Modelle deutlich verbessern kann. Wichtig ist hier ein zentraler Blick auf die Ressourcenallokation und auf Engpässe entlang der pipeline. Daraus folgern ML-Architekten strategische Inputs.

5. Backend Engineer: Cloud Infrastruktur für das Modelldeployment

All diese Rollen können wichtig sein, müssen sich aber je nach Aufbau der Organisation und des Teams nicht im MLOps-Team wiederfinden. Bestimmte Rollen können Aufgaben nicht vorhandener Rollen übernehmen, bestimmte Fragen stellen sich in einer konkreten Organisation vielleicht auch nicht (bspw. Cloud).

![phase](/assets/img/phase.jpg)
<span>Foto von <a href="https://unsplash.com/@jannerboy62?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Nick Fewings</a> auf <a href="https://unsplash.com/de/s/fotos/sequence?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span>

## MLOps: Komponenten und Phasen

Wir haben es einfach gesagt bei MLOps mit Praktiken zu tun, um ML-Modelle für die Produktion zu designen, zu deployen und zu warten. Kontinuierlich, verlässlich und effizient. MLOps hebt dabei die Trennung zwischen Entwicklung und Betrieb auf, der vor allem die Weiterentwicklung verlangsamen kann. Neben MLOps kennen wir noch weitere Konzepte rund um Machine Learning: ModelOps - Fokus ist das Machine Learning Modell, DataOps - Fokus sind die Daten, Qualität und Analyticspraktiken sowie AIOps - Fokus Nutzung von Analytics/Big Data/ML, um Probleme mit IT automatisiert zu lösen.
 
### Designphase:
Die kritischste Phase im MLOps-Lifecycle. Technisch braucht es zunächst einen Plan, welche Tools/Infrastruktur und Ressourcen ein Produkt um eine Machine-Learning-Applikation herum braucht und wo Risiken liegen. Danach braucht es die richtigen Daten für die Business Probleme. In hoher Qualität, möglichst real-time. Die gewünschte Infrastruktur muss dann bereit sein, die Daten müssen analysiert und verstanden sein. Daten für die Produktion müssen automatisiert gesammelt und versioniert werden. Datenqualität steht deutlich im Fokus: schlechte Daten haben grossen Einfluss auf die Vorhersagequalität eines ML-Modells. Wichtig sind vier Dimensionen: wie gut bilden die Daten die Realität ab, wie vollständig sind die Daten, wie konsistent sind sie und sind sie gut verfügbar.

Fachlich ist es wichtig mit offenen Karten zu spielen und den (zusätzlichen) Business Value durch das ML-Modell zu schätzen und als Benchmark festzuschreiben. Darauf folgt das Erheben der Business Anforderungen: Anforderungen der Nutzer, gesetzliche Regulationen, Budget für die Entwicklung und die zur Verfügung stehenden Ressourcen bei den Entwicklern. Idealerweise folgt die detaillierte Definition von Key Metrics: Accuracy, Business Impact, monetärer Nutzen. 

### Developmentphase:
Die Vorbereitung der Daten für das Modeltraining unter Einbezug von fachlichen Experten soll vor allem verlässliche Daten bereitstellen und diskriminierende Features für das zu entwickelnde Modell verfügbar machen. Gute Features sind hier wichtig für ein genaues Modell, sie sorgen für stabile Modelle. Allerdings können sie auch höhere Kosten verursachen, denn das Engineering ist aufwändig. Ausserdem brauchen sie oft auch mehr Betriebsaufwand. Der Aufbau eines zentralen Feature Store bringt erst ab einer gewissen Menge an ML-Modellen und einer gewissen Teamgrösse von Entwicklern einen Nutzen.

Mit der Entwicklung des ML-Modells im Detail wollen wir uns hier nicht beschäftigen - entscheidend ist, dass dieses Development Testing und Verifikation nach DevOps-Prinzipien und -Standards umfassen muss, die selbstverständlich auch für den Code des ML-Modells gelten. Mit der Model Evaluation schauen Data Scientist und Business stakeholder, ob die Anforderungen des Business aus der Design-Phase erfüllt sind.
Im konkreten Prozess des Model Development und Model Training durch den Data Scientist sind alle Schritte des Trainings und Tunings, des Vergleiches konkurrierender Modelle enthalten - immer basierend auf automatischen logs. 

Mit Experiment Tracking in der Developmentphase durchlaufen die Modelle verschiedene Konfigurationen von Daten oder Algorithmen (das kann eine Vielzahl von Kombinationen ergeben) und liefern dabei Metadaten, die für die spätere Modellevaluation und -reproduktion wichtig sind. Das Tracking hilft,  Resultate zu vergleichen, zu reproduzieren, die kollaborative Arbeitsweisen zu unterstützen und Resultate an stakeholder zu kommunizieren. Der vereinfachte Prozesse sieht so aus: Hypothese formulieren, Experimente designen, Tracking aufsetzen, ML-Modelle trainieren, Selektion des passenden Modells, Reporting über das selektierte Modell.

### Deploymentphase:
In der Deployment- oder Operationsphase gibt es wie in den beiden anderen Phase von MLOps eine Abfolge von Schritten. Im Pre-Deployment schauen die Engineers, dass die ML-Modelle lokal und auf der cloud gleiche Resultate werfen. Beim Deployment selbst werden CI/CD-Pipelines eingesetzt, um die Aufwände vor allem beim Redeployment zu reduzieren. Alles verläuft stark standardisiert und automatisiert: Testing, statistisches Monitoring, technisches Monitoring. 

Nach dem Deployment ergeben sich so eine enge Kontrollen der Modellergebnisse, geringe downtimes und die jederzeit mögliche Aussage, ob der Wert für das Business durch das ML-Modell konstant erzielt wird. Ein Fokus liegt auch auf dem Retraining der Modelle. Je nach Geschäftsumfeld und gesellschaftlichen, politischen und ökonomischen Prozessen können sich die Inputdaten nach Deployment des Modells verändern und bald unterschiedlich von den Trainingsdaten sein. Eine Möglichkeit diesem Drift zu begegnen, ist das Aufsetzen eines automatisierten Retrainings. Wie oft Retrainings notwendig sind, hängt von verschiedenen Faktoren ab: Umfeld der Daten, Kosten und Anforderungen an die Präzision des Modells.

![risk](/assets/img/risk.jpg)
<span>Foto von <a href="https://unsplash.com/@cristofer?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Cristofer Maximilian</a> auf <a href="https://unsplash.com/de/s/fotos/risk?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a></span>
 
## Risikomitigation und Erklärbarkeit
Neben all den technischen Vorteile und Prozesseffizienzen hat MLOps noch weitere Vorteile die einen Einstieg und schnell wachsende Maturität in der eigenen Organisation beinah unvermeidbar machen. Die Nutzung von MLOps als Risikomitigation und für transparente und verantwortungsvolle KI.

Kontinuierliches Performance Monitoring und schnelle Anpassungen an den Modellen sind essentiell. Das muss sicher und verlässlich passieren, für jeden Anwendungsfall müssen die Risiken im Vorhinein evaluiert werden. ML-Modelle unterscheiden sich oft deutlich dahingehend, welches Risiko von Ihnen ausgeht. Ein monatlich genutzer Recommender-Algorithmus ist wesentlicher weniger riskant im Betrieb als ein automatisiertes Entscheidungssystem mit real-time-pipeline. Die Evaluation kann mit der untenstehenden Matrix erfolgen, initial am Beginn einer Entwicklung und periodisch für unvorhergesehene Probleme.
1. Risiko, dass das Modell für einen bestimmten Zeitraum ausfällt
2. Risiko, dass das Modell für bestimmte Fälle falsche Prognosen liefert
3. Risiko, dass die Fairness oder Accuracy eines Modells über die Zeit abnimmt
4. Risiko, dass das Wissen, dass Modell zu warten verlorengeht
 
Die Performance eines ML Modells zeigt sich erst in Produktion, da es entscheidend ist, dass die realen Daten eine gute Entsprechung der Trainingsdaten des spezifischen Modells darstellen. Wenn sich an den produktiven Daten etwas ändern, sinkt die Vorhersageperformance gewöhnlich schnell ab. Ein weiteres Risiko entsteht durch die Art der Entwicklung und die Einbindung von open-source software. Die Versionen im Trainingsprozess müssen zu jenen in Produktion passen. Der Deploymentprozess ist nicht das Ende der Modellentwicklung, es ist erst der Beginn von Monitoring der Performance und Verhalten des Modells. Monitoring aller Verwendungszwecke der Modelle ist ein ebenfalls wichtiger Risikofaktor. Alle potentiellen Risiken können einen vernichtenden Einfluss auf die Businessfunktionalität einer Organisation haben, wenn etwas schief läuft.

Im Bereich MLOps für verantwortliche KI findet sich die Schnittpunkte zu KI-Ethik, weswegen es wichtig ist, auch diese Einsatzzwecke zu reflektieren. Es ist wichtig, die Verwendung der Modelle im Blick zu behalten: werden die Modelle nur für die Zwecke benutzt, für die sie erstellt wurden, verhalten sich die Modelle in Produktion, wie erwartet werden kann? Vor dem Deployment müssen data bias und model bias untersucht und wenn möglich mitigiert werden. Die verwendeten ML-Modelle sollten Menschen erklärt werden können, idealerweise nicht nur anderen Entwicklern, sondern auch nicht-technischen Kollegen und Fachexperten. Wichtig ist daneben Rechenschaft darüber geben zu können, welche Teams einer Organisation Daten auf welche Weise in welchen Modellen nutzen und das beinhaltet im Vorfeld verlässliche Daten aus verlässlichen Quellen bereitzustellen. Es folgt die Schaffung eines zentralisierten Verständnisses, welche Modelle in welchen Businessprozessen genutzt werden - essentiell für einen trace back bei Fehlfunktionen. Um klare Entscheidungswege zu haben (trotz der wichtigen crowd- und Teamstrukturen und der kollaborativen Arbeitsweise ohne Hierarchie) muss ein Verantwortlicher für die Verwendung der Modellvorhersagen definiert werden: das führt zu einer Verschiebung der Verantwortung für Prozessresultate von vielen beitragenden einzelnen Menschen zu einem Executive, der das ML-Modell fachlich verantwortet.

![wrap](/assets/img/wrap_01.jpg)
Foto von <a href="https://unsplash.com/@marius?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Marius Masalar</a> auf <a href="https://unsplash.com/de/s/fotos/wrapped?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

## Zusammenfassung und Best Practices

Nach all den vielen Informationen, die dennoch nur den momentanen Stand zusammenfassen und diesen auch nur an der Oberfläche behandeln, möchte ich mit ein paar best practices abschliessen. Entscheidend ist der Fokus auf bessere Datenqualität statt auf bessere Modelle, vor allem wenn man sich entscheiden muss, wo das Geld investiert werden kann. Ein klares Ziel ist entscheidend, starte immer mit einer Businessfrage und einem Proof of Concept. Wichtig, gerade wenn man die Infrastruktur von klein auf schrittweise immer weiter vergrössert: sie muss für schwankende Spitzen (paralleles Training von vielen ML-Modellen) bereit sein. Unbedingt immer automatisierte Tests über den gesamten Lifecycle schreiben, das reduziert die Probleme bei Redeployments erheblich. Auf bestmögliche Codequalität und Reproduzierbarkeit (Versionierung Data & Code) achten und zuletzt unbedingt alles automatisiert loggen und monitoren. Metadata rules!

Warum ging es lange gut, ML-Modelle zu entwickeln und zu deployen - ohne definierte und zentralisierte Prozesse? Das liegt schlicht daran, dass die ML-Modelle in Produktion nicht zahlreich genug waren. Die Schnittstellen waren noch manuell wartbar und alle Schritte waren für einzelne Entwickler nachvollziehbar. Das ändert sich nun in vielen traditionellen Organisationen.

Zusammenfassend lässt sich sagen, dass die Integration von MLOps in den Entwicklungsprozess von ML-Modellen das Potential hat, die Arbeitsweise vor allem traditioneller Unternehmen im Umfeld ihrer genutzten ML-Modelle zu revolutionieren. Durch die Automatisierung und Standardisierung der Pipeline können Unternehmen ihre Modelle effektiv und effizient auf den Markt bringen. Da die Technologie immer weiter voranschreitet, ist es wichtig, auf dem neuesten Stand zu bleiben und neue Lösungen zu nutzen. Sehen wir MLOps als grosse Chance und bleiben neugierig, wohin es uns führen wird.

Die Basis für diesen Blogeintrag bilden vor allem zwei Forschungspublikationen [Mark Treveil](https://oreilly.de/produkt/mlops-kernkonzepte-im-ueberblick/) und [Sculley et.al.](https://research.google/pubs/pub43146/) und darauf aufbauen einige Kurse auf DataCamp. Ergänzt habe ich das Ganze mit Insights aus meiner praktischen Beschäftigung mit dem Themenkomplex MLOps in den letzten Monaten. Einen guten Einstieg bietet auch [MLOps.org](https://ml-ops.org).

***Thank you, and have a beautiful day!***
***Like to connect? I'm on [linkedin](https://www.linkedin.com/in/thombauer/) ;)***