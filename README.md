# **Spectral Clustering – eine empirische Untersuchung** 

## Freie wissenschaftliche Arbeit zur Erlangung des akademischen Grades "Bachelor of Science"

Studiengang: Wirtschaftsinformatik

**an der Wirtschaftswissenschaftlichen Fakultät der Universität Augsburg**

Lehrstuhl für Statistik

Eingereicht bei: Prof. Dr. Yarema Okhrin

Betreuerin:      Christine Distler (M. Sc.)

Vorgelegt von:

Adresse:         
>
>
>

Augsburg, im März 2023

### Zusammenfassung
In dieser Arbeit wird das Spectral Clustering behandelt, das auf der Graphentheorie und Spektraltheorie basiert. Es wurden viele Varianten des Spectral Clusterings entwickelt, die sich in der Wahl der Parameter unterscheiden. In der vorliegenden Arbeit wird empirisch untersucht, wie sich verschiedene Parameter auf die Performance des Spectral Clusterings auswirken. Es zeigt sich, dass die Performance empfindlich auf die Parameterwahl reagiert. Es ist sinnvoll, eine Clusteranalyse mit verschiedenen Parameterkombinationen durchzuführen, um die besten Ergebnisse zu finden.

### Einleitung
Die Clusteranalyse (auch Clustering genannt) ist ein wichtiges Verfahren in der Data Science. Das Ziel ist es, Gruppen in einem Datensatz zu bilden, sodass Objekte in einer Gruppe möglichst ähnlich sind und sich verschiedene Gruppen voneinander so weit wie möglich unterscheiden. (Rousseeuw, 1987; Arthur und Vassilvitskii, 2007; Zhang et al., 2020). Beispiele für „Objekte“, die man clustern möchte sind Pflanzen, Kunden in einem Onlineshop, Patienten im Krankenhaus, Immobilien oder Teile in Bildern. Das kann Vorteile in vielen Bereichen bringen. Z.B. wenn man versucht Kunden in Gruppen auf- zuteilen, kann man Gruppen angepasste Angebote anbieten, was einen ökonomischen Vorteil für den Handel hat.  
Es gibt verschiedene Cluster-Verfahren. Zu denen zählen partitionsbasiertes, hierarchisches, dichtebasiertes, gitterbasiertes und Verfahren die auf Graphentheorie basieren (Zhang et al., 2020, S. 1). In dieser Arbeit behandle ich das Spectral Clustering. Diese Clusteranalyse basiert auf die Graphentheorie. Ein Graph ist eine mathematische Repräsentation von Daten. Er besteht aus Knoten, die Datenpunkte eines Datensatzes repräsentieren. Diese Knoten sind im Graphen durch sog. Kanten miteinander verbun- den. Die Kanten zeigen ob und wie sehr Datenpunkte mit einander verbunden sind, bzw. ob und wie ähnlich sie zueinander sind (Erciyes, 2021c). Das Spectral Clustering lässt sich genauer in die Spectral Theorie einordnen. Diese Theorie zeigt, dass man mit Hilfe von Umwandlungen eines Graphen bestimmte Eigenschaften des Graphen herausfinden kann. Insbesondere ist hier relevent, dass man bestimmen kann, an welchen Stellen ein Graph geteilt werden sollte. (Fiedler, 1973; Chung und Sciences, 1997; Shi und Malik, 2000; Luxburg, 2007).  
Mit der Zeit wurden viele Varianten des Spectral Clusterings entwickelt. Sie unterscheiden sich in der Wahl der Parameter, die für das Clustering benötigt werden. Dazu zählt u.a. die Wahl eines Ähnlichkeitsgraphen oder die Wahl der Anzahl an Cluster, die in einem Datensatz gefunden werden sollen. Eine ausführliche Behandlung des Spectral Clustering findet sich in „A tutorial on spectral clustering“ von Luxburg (2007). Die Autorin stellt u.a. drei Varianten des Spectral Clusterings vor. Von Luxburg weist darauf hin, dass es eine Wissenlücke gibt, wie man die richtigen Parameter für das Clusteringverfahren auswählt und höchstens Daumenregeln vorhanden sind.  
In meiner Arbeit untersuche empirisch die Auswirkungen verschiedener Parameter auf die Performance des Spectral Clusterings. In den Untersuchungen bestätigt sich, dass die Performance sehr empfindlich auf die Parameterwahl reagiert. Die Clusteranalyse beim Spectral Clustering kann zwischen der besten und schlechtesten Güte schwanken. Daher ist es sinnvoll eine Clusteringanalyse mit verschiedenen Parameterkombinationen durchzuführen. In meinen Untersuchungen können die Vorschläge zur Parameterwahl, die von Luxburg vorstellt, nicht unbedingt bekräftigt werden. Das kann an den verwendeten Datensätzen liegen und wie ich die Ausprägungen der Parameter ausgewählt habe.  
Diese Arbeit ist in zwei große Abschnitte Aufgeteilt. Als erstes wird das Spectral Clustering vorgestellt. Darin gebe ich eine Einführung in die Graphentheorie, die Grundlage für das Spectral Clustering ist. Ich zeige das Verfahren des Spectral Clustering mit verschiedenen Varianten und erläutere das Verfahren an einem Beispiel. Ich fasse zu- sammen, welche Parameter man wählen kann und welche Empfehlungen es zur Wahl der Parameter gibt. Anschließend zeige ich vier Gütemaße, mit denen man eine Clusteranalyse auswerten kann. Im zweiten Teil der Arbeit führe ich eine Clusteranalyse mit dem Spectral Clustering an drei synthetischen und einem realen Datensatz durch. Dabei wende ich Kombinationen verschiedener Parameter an. Ich werte die Clusteranalyse mit den vorgestellten Gütemaße aus und betrachte den Einfluss verschiedener Parameter auf die Performance der Analyse. Zum Schluss erfolgt eine Zusammenfassung meiner Ergebnisse.
