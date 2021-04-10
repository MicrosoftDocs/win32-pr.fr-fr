---
title: Démarrage d’un exécutable au démarrage du système
description: L’écriture d’une tâche qui démarre un exécutable lorsqu’un système est amorcé s’effectue en définissant un déclencheur de démarrage et une action exécutable.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Planificateur de tâches des exemples de Planificateur de tâches, déclencheur de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674585"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="d394d-104">Démarrage d’un exécutable au démarrage du système</span><span class="sxs-lookup"><span data-stu-id="d394d-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="d394d-105">L’écriture d’une tâche qui démarre un exécutable lorsqu’un système est amorcé s’effectue en définissant un déclencheur de démarrage et une action exécutable.</span><span class="sxs-lookup"><span data-stu-id="d394d-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="d394d-106">Déclencheur de démarrage</span><span class="sxs-lookup"><span data-stu-id="d394d-106">Boot Trigger</span></span>

<span data-ttu-id="d394d-107">Les déclencheurs de démarrage sont activés par leur limite de démarrage, mais ils ne démarrent pas l’exécutable tant que le système n’est pas démarré.</span><span class="sxs-lookup"><span data-stu-id="d394d-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="d394d-108">Vous pouvez également spécifier un délai dans le déclencheur de démarrage qui spécifie la durée entre le démarrage du système et le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="d394d-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="d394d-109">Cela est défini par la propriété [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) dans l’interface [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (objet [**BootTrigger**](boottrigger.md) pour les scripts).</span><span class="sxs-lookup"><span data-stu-id="d394d-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="d394d-110">Exemples de déclencheurs de démarrage</span><span class="sxs-lookup"><span data-stu-id="d394d-110">Boot Trigger Examples</span></span>

<span data-ttu-id="d394d-111">Les exemples suivants démarrent le bloc-notes après le démarrage du système :</span><span class="sxs-lookup"><span data-stu-id="d394d-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="d394d-112">Exemple de déclencheur de démarrage (script)</span><span class="sxs-lookup"><span data-stu-id="d394d-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="d394d-113">Exemple de déclencheur de démarrage (C++)</span><span class="sxs-lookup"><span data-stu-id="d394d-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="d394d-114">Exemple de déclencheur de démarrage (XML)</span><span class="sxs-lookup"><span data-stu-id="d394d-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="d394d-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d394d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d394d-116">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d394d-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




