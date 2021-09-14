---
title: traçage réseau dans l’Architecture Windows 7
description: l’illustration suivante montre l’architecture de suivi réseau de base dans Windows 7.
ms.assetid: b3023469-0f98-451c-b39f-c3eae771eacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41221ebf434c05a8c9b7c8489e861128029b5320
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021163"
---
# <a name="network-tracing-in-windows-7-architecture"></a>traçage réseau dans Windows 7 : Architecture

l’illustration suivante montre l’architecture de suivi réseau de base dans Windows 7.

![diagramme de l’architecture de suivi réseau](images/ut1.png)

le suivi réseau utilise l’infrastructure Suivi d’v nements pour Windows (ETW) disponible dans Windows. Les composants réseau (tels que Winsock, TCP/IP, NDIS, capture de paquets, etc.) s’inscrivent en tant que fournisseurs de suivi ETW et émettent des événements liés à l’activité réseau. Toute activité enregistrable de précision peut être un événement enregistré dans ETW. Le suivi de ces composants réseau et captures de paquets peut être activé à l’aide du contexte de **trace netsh** qui agit comme un contrôleur ETW.

Les traces générées sont collectées dans un fichier journal de suivi d’événements (ETL). Ces fichiers ETL peuvent ensuite être analysés à l’aide d’un certain nombre d’outils, tels que Moniteur réseau 3,2 et versions ultérieures, observateur d’événements, **netsh trace Convert** ou Tracerpt.exe.

Chaque événement ETW possède un en-tête commun dans lequel ETW stocke des informations telles que les propriétés d’événement, les horodatages et l’ID d’activité. (Pour plus d’informations sur les ID d’activité, consultez [écriture d’événements connexes dans un scénario de bout en bout](../etw/writing-related-events-in-an-end-to-end-scenario.md)). L’ID d’activité est utilisé pour corréler les événements. En mode utilisateur, les ID d’activité sont stockés dans les threads, et tous les événements journalisés dans un thread sont automatiquement marqués avec le même ID d’activité. En mode noyau, l’ID d’activité doit être explicitement transmis lorsqu’un événement est enregistré. Par défaut, les fichiers ETL sont corrélés pour regrouper les événements sous des ID d’activité spécifiques.

pour plus d’informations sur les événements de Windows et ETW, consultez [Windows des événements](../events/windows-events.md).

## <a name="etw-components-in-network-tracing"></a>Composants ETW dans le traçage réseau

Le suivi réseau utilise ETW comme mécanisme de suivi principal pour fournir des informations sur les opérations effectuées par les sous-systèmes de mise en réseau. Il existe quatre composants principaux dans ETW : les sessions de suivi d’événements, les fournisseurs d’événements, les contrôleurs d’événements et les consommateurs d’événements.

La mise en mémoire tampon et la journalisation ont lieu dans les *sessions de suivi d’événements*, qui acceptent les événements des fournisseurs et crée des fichiers de trace.

Un *fournisseur d’événements* est une entité logique qui écrit des événements dans des sessions ETW. Un fournisseur d’événements peut être une application en mode utilisateur, une application managée, un pilote ou toute autre entité logicielle. Les fournisseurs d’événements s’inscrivent avec ETW et écrivent des événements à partir de différents points du code en appelant l’API de journalisation ETW. en raison de la croissance de l’instrumentation d’événements dans de nombreux composants du système d’exploitation, même une application ou un scénario simple dans Windows contient plusieurs composants qui sont des fournisseurs d’événements.

Un *contrôleur d’événements* démarre et arrête les sessions de suivi d’événements et active les fournisseurs. Lorsqu’un fournisseur d’événements est activé dynamiquement par l’application du contrôleur d’événements, le fournisseur envoie des événements à une session de suivi d’événements spécifique désignée par le contrôleur d’événements. Chaque événement envoyé par le fournisseur d’événements à la session de suivi d’événements se compose d’un en-tête fixe, qui inclut les métadonnées d’événement et toutes les données personnalisées supplémentaires journalisées par le fournisseur.

Un *consommateur d’événements* est une application qui lit les fichiers journaux ou qui écoute une session de suivi d’événements pour les événements en temps réel et les traite. un exemple de consommateur d’événements est Moniteur réseau Microsoft 3,2, qui comprend la capacité de lire et d’afficher les fichiers journaux générés par le traçage réseau dans Windows 7.

Les événements sont remis aux consommateurs d’événements dans l’ordre chronologique, et il existe plusieurs applications consommateur d’événements qui affichent les événements dans des formats spécifiques. Lorsqu’un événement est enregistré dans une session, ETW ajoute des informations supplémentaires à l’en-tête de l’événement, y compris l’horodatage, le processus et l’ID de thread, le numéro de processeur et les données d’utilisation de l’UC du thread de journalisation. Ces données sont ensuite transmises aux consommateurs d’événements, ainsi que toutes les données personnalisées incluses par le fournisseur.

Les fournisseurs utilisant les nouvelles [API de journalisation des événements](/windows/win32/api/evntprov/nf-evntprov-eventwrite) sont censés fournir un fichier XML appelé « manifeste d' [événements](../wes/eventschema-schema.md)». Ce fichier fournit des métadonnées pour définir toutes les données personnalisées et les informations de mise en page pour les événements écrits par le fournisseur. Une application consommateur à usage général utilise ensuite des API [TDH (Trace Data Helper)](/windows/win32/api/tdh/) pour récupérer les métadonnées d’événement, décoder les événements et les afficher.

avec le traçage réseau dans Windows 7, le contrôleur d’événements/le côté consommateur comprend une prise en charge du suivi basé sur les scénarios de bout en bout, intégrée aux expériences de diagnostic et de support globales Windows. Un scénario définit une collection de fournisseurs d’événements impliqués dans le scénario. Le côté contrôleur/consommateur d’événements définit les scénarios (contextes) dans lesquels le suivi peut être utilisé, y compris les fournisseurs appropriés pour des scénarios donnés à travers les composants réseau. Le côté fournisseur d’événements comprend des événements de suivi réseau standardisés provenant de différents composants de la pile réseau, qui peuvent être corrélés via des ID d’activité ETW. Les fournisseurs utilisent un schéma réseau commun qui normalise l’utilisation de concepts ETW tels que des mots clés, des niveaux, des tâches et des OpCodes. Le schéma définit également des événements qui sont communs à de nombreux composants réseau, tels que les événements d’erreur, les événements de suppression de paquets, les événements de schéma et les événements de transition d’État.

 

 