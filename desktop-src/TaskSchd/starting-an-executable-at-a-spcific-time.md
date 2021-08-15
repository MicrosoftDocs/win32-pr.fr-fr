---
title: Démarrage d’un exécutable à une heure spécifique
description: L’écriture d’une tâche qui démarre un exécutable à un moment précis s’effectue en définissant un déclencheur d’heure et une action exécutable.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Planificateur de tâches exemples Planificateur de tâches, déclencheur Time
- Planificateur de tâches exemples Planificateur de tâches, démarrage d’un fichier exécutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62276568f7c626935d8c5c518d51f58ad0a58b5c313e780ec5651067af625068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059957"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Démarrage d’un exécutable à une heure spécifique

L’écriture d’une tâche qui démarre un exécutable à un moment précis s’effectue en définissant un déclencheur d’heure et une action exécutable.

## <a name="start-boundary"></a>Limite de début

Il est important de noter qu’un déclencheur d’heure diffère des autres déclencheurs temporels en ce qu’il est déclenché lorsque le déclencheur est activé par sa limite de début. D’autres déclencheurs basés sur le temps sont activés par leur limite de début, mais ils ne commencent pas à effectuer leurs actions (dans ce cas, le démarrage d’un exécutable) jusqu’à ce qu’une date planifiée soit atteinte.

## <a name="time-trigger-examples"></a>Exemples de déclencheurs temporels

les exemples suivants démarrent Bloc-notes 30 secondes après l’activation de la tâche :

-   [Exemple de déclencheur de temps (C++)](time-trigger-example--c---.md)
-   [Exemple de déclencheur de temps (script)](time-trigger-example--scripting-.md)
-   [Exemple de déclencheur de temps (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




