---
title: Déclencheurs de tâche
description: Un déclencheur est un ensemble de critères qui, lorsqu’il est rempli, démarre l’exécution d’une tâche.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- création de déclencheurs Planificateur de tâches
- déclencheurs Planificateur de tâches
- déclencheurs Planificateur de tâches, décrits
- déclencheurs Planificateur de tâches, basés sur la durée
- déclencheurs Planificateur de tâches, basés sur les événements
- déclencheurs basés sur les événements Planificateur de tâches
- déclencheurs basés sur l’heure Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0060511556615c638eb8385a757e9c44147720b659bb11bfe4f0849e4499ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002297"
---
# <a name="task-triggers"></a>Déclencheurs de tâche

Un déclencheur est un ensemble de critères qui, lorsqu’il est rempli, démarre l’exécution d’une tâche. Planificateur de tâches fournit des déclencheurs basés sur des événements et des temps qui peuvent démarrer une tâche de différentes façons. Une tâche donnée peut être démarrée par un ou plusieurs déclencheurs. Une tâche peut avoir un maximum de 48 déclencheurs.

## <a name="time-based-triggers"></a>Déclencheurs basés sur l’heure

Les déclencheurs basés sur le temps démarrent les tâches aux heures spécifiées. Cela comprend le démarrage de la tâche une fois à une heure spécifique ou le démarrage de la tâche plusieurs fois selon une planification quotidienne, hebdomadaire, mensuelle ou mensuelle.

## <a name="event-based-triggers"></a>Déclencheurs basés sur des événements

Les déclencheurs basés sur des événements démarrent une tâche en réponse à certains événements système. Par exemple, les déclencheurs basés sur des événements peuvent être définis pour démarrer une tâche au démarrage du système, lorsqu’un utilisateur ouvre une session sur l’ordinateur local ou lorsque le système devient inactif.

## <a name="multiple-triggers"></a>Déclencheurs multiples

Chaque tâche peut être démarrée par un ou plusieurs déclencheurs, ce qui permet à la tâche d’être démarrée de plusieurs façons. Toutefois, plusieurs déclencheurs sont implémentés différemment dans Planificateur de tâches 1,0 et Planificateur de tâches 2,0.

Dans Planificateur de tâches 2,0, chaque déclencheur est défini par une API de déclencheur distincte associée à la tâche via la collection de déclencheurs.

Dans Planificateur de tâches 1,0, plusieurs déclencheurs peuvent être considérés comme une planification, un ensemble de fois où la tâche démarre. Dans ce cas, la planification est l’ensemble de fois (spécifié par l’Union de tous les déclencheurs associés à l’élément de travail) à laquelle un élément de travail s’exécutera.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Répétition d’une tâche](repeating-a-task.md)
</dt> <dt>

[Types de déclencheurs](trigger-types.md)
</dt> <dt>

[Interfaces de déclencheur](trigger-interfaces.md)
</dt> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> </dl>

 

 




