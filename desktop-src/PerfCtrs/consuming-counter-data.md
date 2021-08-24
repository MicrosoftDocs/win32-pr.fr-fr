---
description: 'Vous pouvez consommer des données de performances à l’aide de l’une des interfaces suivantes : l’interface PDH (Performance Data Helper), qui fournit un accès de haut niveau aux données des fournisseurs de compteurs de performances version 1 et version 2. L’interface du Registre, qui fournit un accès de bas niveau aux données à partir des fournisseurs de compteurs de performances. L’interface de la bibliothèque de performances, qui fournit un accès direct aux données des fournisseurs de compteurs de performances de la version 2. L’interface PDH est plus facile à utiliser que l’interface du Registre et est recommandée pour la plupart des tâches de collecte des données de performances. L’interface PDH est essentiellement une abstraction de niveau supérieur des fonctionnalités fournies par l’interface du Registre. Utilisez l’interface de la bibliothèque de performances uniquement si vous ne pouvez pas utiliser les fonctions de couche d’abstraction PDH.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Consommation de données de compteur
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f3abcc6dd5a385ebffdc887516613efb76b53359e5f8995bc28ba7f6239187b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775679"
---
# <a name="consuming-counter-data"></a>Consommation de données de compteur

les programmes qui veulent lire et utiliser des données de compteurs de Performance Windows peuvent utiliser l’une des interfaces appropriées pour le scénario.

- Les scripts peuvent utiliser les [classes de compteur de performance WMI](/windows/desktop/WmiSdk/monitoring-performance-data) ou l’outil [typeperf](/windows-server/administration/windows-commands/typeperf) .
- Les programmes .NET peuvent utiliser la [classe PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).
- La [bibliothèque PDH (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) fournit un accès de haut niveau aux données des fournisseurs de compteurs de performances v1 et v2 via une API Win32 (C/C++).
- L' [interface du Registre](using-the-registry-functions-to-consume-counter-data.md) fournit l’accès aux données des fournisseurs de compteurs de performances v1 et v2 via la `HKEY_PERFORMANCE_DATA` clé de Registre spéciale.
- Les [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) offrent un accès de bas niveau aux données des fournisseurs de compteurs de performances v2 via une API Win32 (C/C++).

L’interface PDH est recommandée pour la plupart des tâches de collecte de données de performances C/C++, car elle est plus facile à utiliser que les interfaces Registry et PerfLib.
