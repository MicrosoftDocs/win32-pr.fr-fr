---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20f14980646680e0f6a0418470416801240ca17
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473115"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Objectif

TraceLogging est la nouvelle infrastructure de suivi d’événements Windows 10 pour les applications en mode utilisateur et les pilotes en mode noyau. TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="trace-logging-about.md">À propos de TraceLogging</a><br /> | TraceLogging est le nouveau suivi d’événements Windows 10 pour les applications en mode utilisateur et les pilotes en mode noyau. TraceLogging est un format pour l’auto-description Suivi d’v nements pour Windows (ETW). TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code.<br /> | 
| <a href="tracelogging-using-tracelogging.md">Utilisation de TraceLogging</a><br /> | Les rubriques suivantes fournissent un démarrage rapide TraceLogging pour le code natif et managé, avec des exemples.<br /> | 
| <a href="trace-logging-reference.md">Référence TraceLogging</a><br /> | Les rubriques suivantes fournissent des informations sur l’API TraceLogging native.<br /> TraceLogging s’appuie sur Suivi d’v nements pour Windows (ETW) et fournit un moyen simplifié d’instrumenter le code. TraceLogging vous permet d’inclure des données structurées avec des événements, de mettre en corrélation des événements et ne requiert pas de fichier XML de manifeste d’instrumentation distinct.<br /><span class="underline">Pour les développeurs WinRT</span><br /><ul><li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> a été étendu dans Windows 10 pour consigner les événements ETW (auto-description Suivi d’v nements pour Windows) sans avoir besoin d’un manifeste.</li><li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> a été étendu dans Windows 10 pour fournir des méthodes de démarrage et d’arrêt de l’activité qui permettent de contrôler le format et le contenu des événements de démarrage et d’arrêt. En outre, les activités peuvent être imbriquées.</li></ul><span class="underline">pour les développeurs de code managé (Microsoft .NET Framework)</span><br /><ul><li>la classe <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> fournie avec les versions précédentes du .NET Framework prend déjà en charge l’écriture d’événements ETW sans nécessiter de manifeste. Toutefois, les développeurs devaient utiliser EventSource comme classe de base et ajouter automatiquement des attributs et des méthodes à la classe dérivée qui ont été transformés en manifeste ETW. Désormais, les développeurs n’ont pas besoin de dériver de EventSource et peuvent plutôt utiliser EventSource directement pour consigner les événements à Description automatique qui ne nécessitent pas de manifeste.</li></ul><span class="underline">Pour les développeurs C/C++</span><br /><ul><li>TraceLoggingProvider. h est l’API recommandée pour les développeurs C/C++ en mode utilisateur ou en mode noyau. Cette API n’est pas bien adaptée à une utilisation dans des scénarios dynamiques (scriptés) tels que JavaScript. Les liens suivants décrivent l’API C/C++.</li></ul> | 




 

## <a name="developer-audience"></a>Développeurs concernés

TraceLogging est conçu pour être utilisé par les développeurs d’applications en mode utilisateur et les développeurs de pilotes en mode noyau qui souhaitent ajouter le suivi à leur code.

