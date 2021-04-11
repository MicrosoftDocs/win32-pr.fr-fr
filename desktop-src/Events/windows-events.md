---
title: Événements Windows
description: Les événements sont généralement utilisés pour résoudre les problèmes liés aux logiciels d’application et aux pilotes. Avant Windows Vista, vous utiliseriez l’Suivi d’v nements pour Windows (ETW) ou la journalisation des événements pour consigner les événements. Windows Vista a introduit un nouveau modèle d’événement qui unifiait à la fois l’API Suivi d’v nements pour Windows (ETW) et le journal des événements Windows. Windows 10 introduit TraceLogging, qui s’appuie sur ETW et fournit un moyen simplifié d’instrumenter du code pour les développeurs natifs, .NET et WinRT.
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3d22580c38e45d06f5362e99626642eebdfe20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031189"
---
# <a name="windows-events"></a>Événements Windows

Les événements sont généralement utilisés pour résoudre les problèmes liés aux logiciels d’application et aux pilotes.

-   Avant Windows Vista, vous utiliseriez l' [suivi d’v nements pour Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) ou la [journalisation des événements](/windows/desktop/EventLog/event-logging) pour consigner les événements.
-   Windows Vista a introduit un nouveau modèle d’événement qui unifiait à la fois l’API [suivi d’v nements pour Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) et le [Journal des événements Windows](/windows/desktop/WES/windows-event-log) .
-   Windows 10 introduit [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) , qui s’appuie sur ETW et fournit un moyen simplifié d’instrumenter du code pour les développeurs natifs, .net et WinRT.

Le nouveau modèle [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) vous permet d’inclure des données structurées avec des événements, de corréler des événements et ne nécessite pas de fichier XML de manifeste d’instrumentation distinct.

Le modèle Windows Vista utilise un manifeste XML pour définir les événements que vous souhaitez publier. Les événements peuvent être publiés sur un canal ou une session ETW. Vous pouvez publier les événements sur les types de canaux suivants : admin, opérationnel, analyse et débogage. Si vous utilisez uniquement ETW pour activer le serveur de publication, vous n’avez pas besoin de spécifier de canaux dans votre manifeste. Pour plus d’informations sur l’écriture d’un manifeste, consultez [écriture d’un manifeste d’instrumentation](/windows/desktop/WES/writing-an-instrumentation-manifest)et pour plus d’informations sur les canaux, consultez [définition de canaux](/windows/desktop/WES/defining-channels).

Pour inscrire votre éditeur d’événements et publier des événements, vous utilisez l’API ETW. Pour plus d’informations, consultez [fourniture d’événements](/windows/desktop/ETW/providing-events) et [développement d’un fournisseur](/windows/desktop/WES/developing-a-provider). L’éditeur d’événements écrit automatiquement les événements dans les canaux spécifiés dans le manifeste s’ils sont activés.

Si vous souhaitez contrôler les événements publiés par un éditeur d’événements à un niveau de granularité plus élevé, utilisez l’API ETW. Par exemple, si le manifeste définit à la fois les événements d’écriture et de lecture, vous pouvez activer uniquement les événements d’écriture. Un événement peut également spécifier une valeur de niveau comme un avertissement ou une erreur. vous pouvez donc limiter les événements écrits à ceux qui spécifient le niveau d’erreur. Pour plus d’informations, consultez [contrôle des sessions de suivi d’événements](/windows/desktop/ETW/controlling-event-tracing-sessions). Les événements sont écrits dans le fichier journal de la session.

La consommation d’événements implique la récupération des événements à partir d’un canal d’événement, d’un fichier journal des événements (fichiers. evtx ou. evt), d’un fichier de trace (fichiers. ETL) ou d’une session ETW en temps réel. Pour consommer des événements à partir d’un fichier de trace ETW ou d’une session ETW en temps réel, utilisez les fonctions d’assistance des données de trace (TDH) dans ETW pour consommer les événements. Vous pouvez également utiliser TDH pour lire les métadonnées d’événement. Pour plus d’informations, consultez [consommation d’événements](/windows/desktop/ETW/consuming-events). Pour consommer des événements à partir d’un canal d’événements ou d’un fichier journal des événements, utilisez les fonctions du journal des événements Windows pour interroger ou s’abonner à des événements. Pour plus d’informations, consultez [interrogation d’événements](/windows/desktop/WES/querying-for-events) ou [abonnement à des événements](/windows/desktop/WES/subscribing-to-events).

Avant Windows Vista, vous devez utiliser [suivi d’v nements pour Windows](/windows/desktop/ETW/event-tracing-portal) ou la [journalisation des événements](/windows/desktop/EventLog/event-logging) pour publier et consommer des événements.

 

 