---
title: À propos de TraceLogging
description: TraceLogging est le nouveau suivi d’événements Windows 10 pour les applications en mode utilisateur et les pilotes en mode noyau.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312849"
---
# <a name="about-tracelogging"></a>À propos de TraceLogging

TraceLogging est le nouveau suivi d’événements Windows 10 pour les applications en mode utilisateur et les pilotes en mode noyau. TraceLogging est un format pour l’auto-description Suivi d’v nements pour Windows (ETW). TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.

TraceLogging offre la simplicité de Windows le préprocesseur de suivi logiciel (WPP), avec l’avantage supplémentaire de pouvoir inclure des données structurées avec des événements, la possibilité de mettre en corrélation des événements et tout cela sans nécessiter un fichier XML de manifeste d’instrumentation distinct. Les événements sont auto-descriptifs, ce qui signifie qu’un binaire contenant le manifeste d’instrumentation n’a pas besoin d’être inscrit sur le système pour pouvoir utiliser les API TDH (Trace Data Helper) pour décoder et afficher les événements.

Suivi d’v nements pour Windows (ETW) a été introduit avec Windows 2000 et mis à jour dans Windows Vista. Tracelogging s’appuie sur les api ETW de Windows Vista. les fournisseurs peuvent utiliser la technologie TraceLogging et continuer à travailler sur Windows Vista. les contrôleurs existants (à l’aide de Windows VistaAPIs) peuvent être utilisés pour contrôler les fournisseurs TraceLogging.

TraceLogging est également compatible avec les outils existants. Les fournisseurs qui utilisent le ETW basé sur un manifeste sont toujours pris en charge. Vous n’avez pas besoin de convertir les fournisseurs ETW basés sur un manifeste en fournisseurs TraceLogging, sauf si vous souhaitez tirer parti de la simplicité fournie par TraceLogging. Le suivi WPP est également toujours pris en charge.

TraceLogging s’appuie sur ETW, mais présente plusieurs améliorations importantes :

-   Le suivi d’un événement est aussi simple qu’un appel d’API.
-   Les événements sont autodescriptifs et ne nécessitent pas de binaires supplémentaires contenant le manifeste d’événements compilé pour interpréter l’événement. Toutes les métadonnées relatives à l’événement sont enregistrées dans l’événement.
-   Les activités au sein d’un même processus peuvent être facilement exprimées à l’aide d’événements de démarrage et d’arrêt.
-   TraceLogging est compatible avec la prise en charge d’instrumentation existante. Les nouvelles API ETW continuent à prendre en charge les anciens fournisseurs. Vous pouvez investir dans les nouvelles API ETW pour des scénarios stratégiques tout en laissant vos anciens points d’instrumentation tels quels.
-   TraceLogging offre la même API de suivi d’événements pour Windows 10, Xbox One et Windows 10 Mobile.
-   les api TraceLogging sont accessibles à partir de C, C++, .net et Windows Runtime.

## <a name="api-high-level-overview"></a>Vue d’ensemble de l’API

Il existe trois API TraceLogging distinctes qui ciblent différents publics de développeurs. Chaque API a été conçue pour répondre à différents ensembles d’exigences en fonction de l’audience cible de cette API.

Pour les développeurs WinRT :

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) a été étendu dans Windows 10 pour consigner les événements ETW (auto-description Suivi d’v nements pour Windows) sans avoir besoin d’un manifeste.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) a été étendu dans Windows 10 pour fournir des méthodes de démarrage et d’arrêt de l’activité qui permettent de contrôler le format et le contenu des événements de démarrage et d’arrêt. En outre, les activités peuvent être imbriquées.

Pour les développeurs C/C++ :

-   TraceLoggingProvider. h contient l’API la plus efficace, mais cette API n’est pas bien adaptée pour une utilisation dans des scénarios dynamiques (scriptés) tels que JavaScript. Cette API peut être utilisée en mode utilisateur et en mode noyau.

pour les développeurs de code managé (Microsoft .NET Framework) :

-   la classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fournie avec les versions précédentes du .NET Framework déjà pris en charge l’écriture d’événements ETW, générant automatiquement le manifeste et incorporant le manifeste dans le flux d’événements. Toutefois, le développeur devait toujours effectuer le suivi du manifeste pour décoder les événements (sauf si vous travaillez dans un scénario où le manifeste incorporé était pris en charge). TraceLogging permet d’éliminer complètement le manifeste.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du suivi d’événements](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 