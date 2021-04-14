---
title: Référence TraceLogging
description: Les rubriques suivantes fournissent des informations sur l’API TraceLogging native. TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382708"
---
# <a name="tracelogging-reference"></a>Référence TraceLogging

Les rubriques suivantes fournissent des informations sur l’API TraceLogging native.

TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code. TraceLogging vous permet d’inclure des données structurées avec des événements, de mettre en corrélation des événements et ne requiert pas de fichier XML de manifeste d’instrumentation distinct.

<span class="underline">Pour les développeurs WinRT</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) a été étendu dans Windows 10 pour consigner les événements de suivi d’v nements pour Windows autodescriptifs (ETW) sans nécessiter de manifeste.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) a été étendu dans Windows 10 afin de fournir des méthodes de démarrage et d’arrêt de l’activité qui permettent de contrôler le format et le contenu des événements de démarrage et d’arrêt. En outre, les activités peuvent être imbriquées.

<span class="underline">Pour les développeurs de code managé (Microsoft .NET Framework)</span>

-   La classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fournie avec les versions précédentes du .NET Framework prend déjà en charge l’écriture d’événements ETW sans nécessiter de manifeste. Toutefois, les développeurs devaient utiliser EventSource comme classe de base et ajouter automatiquement des attributs et des méthodes à la classe dérivée qui ont été transformés en manifeste ETW. Désormais, les développeurs n’ont pas besoin de dériver de EventSource et peuvent plutôt utiliser EventSource directement pour consigner les événements à Description automatique qui ne nécessitent pas de manifeste.

<span class="underline">Pour les développeurs C/C++</span>

-   TraceLoggingProvider. h est l’API recommandée pour les développeurs C/C++ en mode utilisateur ou en mode noyau. Cette API n’est pas bien adaptée à une utilisation dans des scénarios dynamiques (scriptés) tels que JavaScript. Les liens suivants décrivent l’API C/C++.

<!-- -->

-   [Classes](trace-logging-classes.md)
-   [Fonctions](trace-logging-functions.md)
-   [Macros](trace-logging-macros.md)

Notez que la valeur de WINVER aura un impact sur le comportement de TraceLoggingProvider. h.

-   Si WINVER n’est pas défini avant d’inclure <Windows. h>, <Windows. h> affectera à WINVER une valeur par défaut correspondant à la version du kit de développement logiciel (SDK).
-   Si vous utilisez TraceLoggingProvider. h avec WINVER défini sur 0x0602 (Windows 8) ou une version ultérieure, le programme ne s’exécutera pas sur Windows Vista ou Windows 7.
-   Si vous utilisez TraceLoggingProvider. h avec WINVER défini sur 0x0600 (Windows Vista) ou 0x0601 (Windows 7), le programme sera configuré pour la compatibilité et fonctionnera sur les versions spécifiées de Windows.

 

 