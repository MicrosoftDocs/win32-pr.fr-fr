---
title: Démarrage d’un exécutable au démarrage du système
description: L’écriture d’une tâche qui démarre un exécutable lorsqu’un système est amorcé s’effectue en définissant un déclencheur de démarrage et une action exécutable.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Planificateur de tâches des exemples de Planificateur de tâches, déclencheur de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120613"
---
# <a name="starting-an-executable-on-system-boot"></a>Démarrage d’un exécutable au démarrage du système

L’écriture d’une tâche qui démarre un exécutable lorsqu’un système est amorcé s’effectue en définissant un déclencheur de démarrage et une action exécutable.

## <a name="boot-trigger"></a>Déclencheur de démarrage

Les déclencheurs de démarrage sont activés par leur limite de démarrage, mais ils ne démarrent pas l’exécutable tant que le système n’est pas démarré. Vous pouvez également spécifier un délai dans le déclencheur de démarrage qui spécifie la durée entre le démarrage du système et le démarrage de la tâche. Cela est défini par la propriété [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) dans l’interface [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (objet [**BootTrigger**](boottrigger.md) pour les scripts).

## <a name="boot-trigger-examples"></a>Exemples de déclencheurs de démarrage

les exemples suivants démarrent Bloc-notes après le démarrage du système :

-   [Exemple de déclencheur de démarrage (script)](boot-trigger-example--scripting-.md)
-   [Exemple de déclencheur de démarrage (C++)](boot-trigger-example--c---.md)
-   [Exemple de déclencheur de démarrage (XML)](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




