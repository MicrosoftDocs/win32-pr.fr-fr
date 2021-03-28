---
description: Suivi d’v nements pour Windows (ETW) est une fonctionnalité de traçage efficace au niveau du noyau qui vous permet d’enregistrer des événements de noyau ou définis par l’application dans un fichier journal.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: À propos du suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951333"
---
# <a name="about-event-tracing"></a>À propos du suivi d’événements

Suivi d’v nements pour Windows (ETW) est une fonctionnalité de traçage efficace au niveau du noyau qui vous permet d’enregistrer des événements de noyau ou définis par l’application dans un fichier journal. Vous pouvez consommer les événements en temps réel ou à partir d’un fichier journal et les utiliser pour déboguer une application ou pour déterminer où les problèmes de performances se produisent dans l’application.

ETW vous permet d’activer ou de désactiver le suivi des événements de manière dynamique, ce qui vous permet d’effectuer un suivi détaillé dans un environnement de production sans nécessiter le redémarrage de l’ordinateur ou de l’application.

L’API de suivi d’événements est divisée en trois composants distincts :

-   [Contrôleurs](#controllers), qui démarrent et arrêtent une session de suivi d’événements et activent les fournisseurs
-   [Fournisseurs](#providers), qui fournissent les événements
-   [Consommateurs](#consumers), qui consomment les événements

Le diagramme suivant illustre le modèle de suivi d’événements.

![modèle de suivi d’événements](images/etdiag2.png)

## <a name="controllers"></a>Controllers

Les contrôleurs sont des applications qui définissent la taille et l’emplacement du fichier journal, démarrent et arrêtent les [sessions de suivi des événements](event-tracing-sessions.md), activent les fournisseurs afin de pouvoir consigner les événements dans la session, gérer la taille du pool de mémoires tampons et obtenir des statistiques d’exécution pour les sessions. Les statistiques de session incluent le nombre de mémoires tampons utilisées, le nombre de mémoires tampons livrées et le nombre d’événements et de tampons perdus. 

Pour plus d’informations, consultez [contrôle des sessions de suivi d’événements](controlling-event-tracing-sessions.md).

## <a name="providers"></a>Fournisseurs

Les fournisseurs sont des applications qui contiennent l’instrumentation de traçage d’événements. Une fois qu’un fournisseur s’est inscrit lui-même, un contrôleur peut ensuite activer ou désactiver le suivi des événements dans le fournisseur. Le fournisseur définit son interprétation de l’activation ou de la désactivation. En règle générale, un fournisseur activé génère des événements, contrairement à un fournisseur désactivé. Cela vous permet d’ajouter le suivi d’événements à votre application sans qu’il ne soit nécessaire de générer des événements en permanence. 

Bien que le modèle ETW sépare le contrôleur et le fournisseur en applications distinctes, une application peut inclure les deux composants.

Pour plus d’informations, consultez [fourniture d’événements](providing-events.md).

### <a name="types-of-providers"></a>Types de fournisseurs

Il existe quatre types principaux de fournisseurs : fournisseurs MOF (Classic), fournisseurs WPP, fournisseurs basés sur un manifeste et fournisseurs TraceLogging. Vous devez utiliser un fournisseur basé sur un manifeste ou un fournisseur TraceLogging si vous écrivez des applications pour Windows Vista ou version ultérieure qui n’ont pas besoin de prendre en charge les systèmes hérités.

#### <a name="mof-classic-providers"></a>Fournisseurs MOF (classiques) :

-   Utilisez les fonctions [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) et [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour inscrire et écrire des événements.
-   Utilisez les classes MOF pour définir des événements afin que les consommateurs sachent comment les utiliser.
-   Ne peut être activé que par une seule session de suivi à la fois.

#### <a name="wpp-providers"></a>Fournisseurs WPP :

-   Utilisez les fonctions [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) et [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour inscrire et écrire des événements.
-   Avoir des fichiers TMF associés (compilés dans le fichier. pdb d’un binaire) qui contiennent des informations de décodage déduites de l’analyse du préprocesseur de l’instrumentation WPP dans le code source.
-   Ne peut être activé que par une seule session de suivi à la fois.

#### <a name="manifest-based-providers"></a>Fournisseurs basés sur un manifeste :

-   Utilisez [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) et [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) pour inscrire et écrire des événements.
-   Utilisez un manifeste pour définir des événements afin que les consommateurs sachent comment les utiliser.
-   Peut être activée simultanément jusqu’à huit sessions de suivi.

#### <a name="tracelogging-providers"></a>Fournisseurs [TraceLogging](/windows/desktop/tracelogging/trace-logging-about) :

-   Utilisez [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) et [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) pour inscrire et écrire des événements.
-   Utilisez des événements auto-descriptifs afin que les événements eux-mêmes contiennent toutes les informations requises pour les consommer.
-   Peut être activée simultanément jusqu’à huit sessions de suivi.

Tous les fournisseurs d’événements utilisent fondamentalement la famille d’API de suivi d’événements ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) pour les technologies héritées et [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) pour les versions plus récentes). Les fournisseurs d’événements diffèrent simplement dans les types de champs qu’ils stockent dans les charges utiles d’événement et où ils stockent les informations de décodage d’événements associées.

## <a name="consumers"></a>Consommateurs

Les consommateurs sont des applications qui sélectionnent une ou plusieurs sessions de suivi d’événements comme source d’événements. Un consommateur peut demander simultanément des événements de plusieurs sessions de suivi d’événements ; le système remet les événements dans l’ordre chronologique. Les consommateurs peuvent recevoir des événements stockés dans des fichiers journaux ou des sessions qui délivrent des événements en temps réel. Lors du traitement des événements, un consommateur peut spécifier des heures de début et de fin, et seuls les événements qui se produisent dans le laps de temps spécifié sont remis. 

Pour plus d’informations, consultez [consommation d’événements](consuming-events.md).

## <a name="missing-events"></a>Événements manquants

Perfmon, diagnostics du système et d’autres outils système peuvent signaler des événements manquants dans le journal des événements et indiquer que les paramètres de Suivi d’v nements pour Windows (ETW) peuvent ne pas être optimaux. Les événements peuvent être perdus pour plusieurs raisons :

-   La taille totale de l’événement est supérieure à 64 Ko. Cela comprend l’en-tête ETW plus les données ou la charge utile. Un utilisateur n’a aucun contrôle sur ces événements manquants, car la taille de l’événement est configurée par l’application.

-   La taille de la mémoire tampon ETW est inférieure à la taille totale de l’événement. Un utilisateur n’a aucun contrôle sur ces événements manquants, car la taille de l’événement est configurée par l’application consignant les événements.

-   Pour la journalisation en temps réel, le consommateur en temps réel ne consomme pas d’événements assez rapidement ou n’est pas entièrement présent, puis le fichier de sauvegarde est saturé. Cela peut se produire si le service journal des événements est arrêté et démarré lors de la journalisation des événements. Un utilisateur n’a aucun contrôle sur ces événements manquants.

-   Lors de la journalisation dans un fichier, le disque est trop lent pour suivre le taux de journalisation.

Pour l’une de ces raisons, veuillez signaler ces problèmes au fournisseur de l’application ou du service qui génère les événements. Ces problèmes peuvent être résolus uniquement par le développeur de l’application ou le service qui journalise les événements. Si les événements manquants sont signalés dans le service journal des événements, cela peut indiquer un problème avec la configuration du service journal des événements. L’utilisateur peut avoir une capacité limitée à augmenter l’espace disque maximal à utiliser par le service journal des événements, ce qui peut réduire le nombre d’événements manquants.

 

 
