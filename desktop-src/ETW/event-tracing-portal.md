---
description: Cette documentation est destinée aux applications en mode utilisateur qui souhaitent utiliser ETW. pour plus d’informations sur l’instrumentation des pilotes de périphérique qui s’exécutent en mode noyau, voir WPP Software tracing et ajout d’Event tracing to Kernel-Mode drivers in the Windows Driver Kit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908e935d48749d80e5b2cfe237efeed5413c839157e53b489f4857c0349b4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070219"
---
# <a name="event-tracing"></a>Suivi d’événements

## <a name="purpose"></a>Objectif

Suivi d’v nements pour Windows (ETW) fournit aux programmeurs d’applications la possibilité de démarrer et d’arrêter les sessions de suivi d’événements, d’instrumenter une application pour fournir des événements de trace et de consommer des événements de trace. Les événements de trace contiennent un en-tête d’événement et des données définies par le fournisseur qui décrivent l’état actuel d’une application ou d’une opération. Vous pouvez utiliser les événements pour déboguer une application et effectuer une analyse de la capacité et des performances.

Cette documentation est destinée aux applications en mode utilisateur qui souhaitent utiliser ETW. pour plus d’informations sur l’instrumentation des pilotes de périphérique qui s’exécutent en mode noyau, voir [WPP Software tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) et [ajout d’Event tracing to Kernel-Mode drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).

## <a name="where-applicable"></a>Le cas échéant

Utilisez ETW lorsque vous souhaitez instrumenter votre application, consigner des événements utilisateur ou de noyau dans un fichier journal, et consommer des événements à partir d’un fichier journal ou en temps réel.

## <a name="developer-audience"></a>Développeurs concernés

ETW est conçu pour les développeurs C et C++ qui écrivent des applications en mode utilisateur.

## <a name="run-time-requirements"></a>Conditions d’exécution

ETW est inclus dans Microsoft Windows 2000 et versions ultérieures. Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.

## <a name="process-etw-traces-in-net-code"></a>Traiter les traces ETW dans le code .NET

Vous pouvez utiliser l' [API .net TraceProcessing](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) pour analyser les traces ETW pour vos applications et d’autres composants logiciels. cette API est utilisée en interne chez Microsoft pour analyser les données ETW produites par le système d’ingénierie Windows, et elle est également utilisée pour alimenter plusieurs tables dans [Windows analyseur de performances](/windows-hardware/test/wpt/windows-performance-analyzer). cette API est disponible sous la forme d’un package NuGet.

Pour plus d’informations, consultez [cet article](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                     | Description                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Nouveautés du suivi d’événements](what-s-new-in-event-tracing.md)<br/> | Nouvelles fonctionnalités qui ont été ajoutées au suivi d’événements dans chaque version.<br/>          |
| [À propos du suivi d’événements](about-event-tracing.md)<br/>                 | Informations générales sur le suivi des événements.<br/>                                |
| [Utilisation du suivi d’événements](using-event-tracing.md)<br/>                 | Rubriques relatives aux tâches qui décrivent comment utiliser l’API ETW.<br/>               |
| [Référence de suivi d’événements](event-tracing-reference.md)<br/>         | Description détaillée des fonctions ETW et d’autres éléments de programmation. <br/> |



 

 

 
