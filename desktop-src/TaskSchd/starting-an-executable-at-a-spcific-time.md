---
title: Démarrage d’un exécutable à une heure spécifique
description: L’écriture d’une tâche qui démarre un exécutable à un moment précis s’effectue en définissant un déclencheur d’heure et une action exécutable.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Planificateur de tâches exemples Planificateur de tâches, déclencheur Time
- Planificateur de tâches exemples Planificateur de tâches, démarrage d’un fichier exécutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840385"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="f88dc-105">Démarrage d’un exécutable à une heure spécifique</span><span class="sxs-lookup"><span data-stu-id="f88dc-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="f88dc-106">L’écriture d’une tâche qui démarre un exécutable à un moment précis s’effectue en définissant un déclencheur d’heure et une action exécutable.</span><span class="sxs-lookup"><span data-stu-id="f88dc-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="f88dc-107">Limite de début</span><span class="sxs-lookup"><span data-stu-id="f88dc-107">Start Boundary</span></span>

<span data-ttu-id="f88dc-108">Il est important de noter qu’un déclencheur d’heure diffère des autres déclencheurs temporels en ce qu’il est déclenché lorsque le déclencheur est activé par sa limite de début.</span><span class="sxs-lookup"><span data-stu-id="f88dc-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="f88dc-109">D’autres déclencheurs basés sur le temps sont activés par leur limite de début, mais ils ne commencent pas à effectuer leurs actions (dans ce cas, le démarrage d’un exécutable) jusqu’à ce qu’une date planifiée soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="f88dc-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="f88dc-110">Exemples de déclencheurs temporels</span><span class="sxs-lookup"><span data-stu-id="f88dc-110">Time Trigger Examples</span></span>

<span data-ttu-id="f88dc-111">Les exemples suivants démarrent le bloc-notes 30 secondes après l’activation de la tâche :</span><span class="sxs-lookup"><span data-stu-id="f88dc-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="f88dc-112">Exemple de déclencheur de temps (C++)</span><span class="sxs-lookup"><span data-stu-id="f88dc-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="f88dc-113">Exemple de déclencheur de temps (script)</span><span class="sxs-lookup"><span data-stu-id="f88dc-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="f88dc-114">Exemple de déclencheur de temps (XML)</span><span class="sxs-lookup"><span data-stu-id="f88dc-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="f88dc-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f88dc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f88dc-116">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f88dc-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




