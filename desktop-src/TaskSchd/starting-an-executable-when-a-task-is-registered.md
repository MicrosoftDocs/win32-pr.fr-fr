---
title: Démarrage d’un exécutable quand une tâche est inscrite
description: L’écriture d’une tâche qui démarre un exécutable quand une tâche est inscrite est effectuée en définissant un déclencheur d’inscription et une action exécutable.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Planificateur de tâches des exemples de Planificateur de tâches, déclencheur d’inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940077"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="a5e11-104">Démarrage d’un exécutable quand une tâche est inscrite</span><span class="sxs-lookup"><span data-stu-id="a5e11-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="a5e11-105">L’écriture d’une tâche qui démarre un exécutable quand une tâche est inscrite est effectuée en définissant un déclencheur d’inscription et une action exécutable.</span><span class="sxs-lookup"><span data-stu-id="a5e11-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="a5e11-106">Déclencheur d’inscription</span><span class="sxs-lookup"><span data-stu-id="a5e11-106">Registration Trigger</span></span>

<span data-ttu-id="a5e11-107">Les déclencheurs d’inscription démarrent une tâche dès qu’elle est inscrite.</span><span class="sxs-lookup"><span data-stu-id="a5e11-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="a5e11-108">Vous pouvez également spécifier un délai pour le déclencheur d’inscription, qui démarre une tâche après un laps de temps spécifique (délai) après l’inscription de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a5e11-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="a5e11-109">Le délai est spécifié dans la propriété [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) de l’interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) pour l’écriture de scripts).</span><span class="sxs-lookup"><span data-stu-id="a5e11-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="a5e11-110">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="a5e11-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="a5e11-111">Exemples de déclencheurs d’inscription</span><span class="sxs-lookup"><span data-stu-id="a5e11-111">Registration Trigger Examples</span></span>

<span data-ttu-id="a5e11-112">Les exemples suivants démarrent le bloc-notes quand une tâche est inscrite :</span><span class="sxs-lookup"><span data-stu-id="a5e11-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="a5e11-113">Exemple de déclencheur d’inscription (script)</span><span class="sxs-lookup"><span data-stu-id="a5e11-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="a5e11-114">Exemple de déclencheur d’inscription (C++)</span><span class="sxs-lookup"><span data-stu-id="a5e11-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="a5e11-115">Exemple de déclencheur d’inscription (XML)</span><span class="sxs-lookup"><span data-stu-id="a5e11-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="a5e11-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5e11-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e11-117">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a5e11-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




