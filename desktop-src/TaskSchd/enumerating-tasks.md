---
title: Énumération des tâches
description: Planificateur de tâches 1,0 fournit un objet d’énumération pour l’énumération des tâches dans le dossier tâches planifiées.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- énumération des tâches Planificateur de tâches
- énumération des tâches Planificateur de tâches, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029505"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="1b743-105">Énumération des tâches</span><span class="sxs-lookup"><span data-stu-id="1b743-105">Enumerating Tasks</span></span>

<span data-ttu-id="1b743-106">Planificateur de tâches 1,0 fournit un objet d’énumération pour l’énumération des tâches dans le [*dossier tâches planifiées*](s.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="1b743-107">Pour qu’un ordinateur Windows Server 2003, Windows XP ou Windows 2000 crée, surveille ou contrôle des tâches sur un ordinateur Windows Vista, certaines opérations doivent être effectuées sur l’ordinateur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b743-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="1b743-108">Pour plus d’informations, consultez l’article [Tâches MSBuild](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="1b743-109">Utilisation de l’objet d’énumération</span><span class="sxs-lookup"><span data-stu-id="1b743-109">Using the Enumeration Object</span></span>

<span data-ttu-id="1b743-110">L’interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de cet objet fournit des méthodes pour énumérer les tâches dans le dossier, réinitialisation de la séquence d’énumération au début de la liste, ignorer des tâches et faire une copie de l’objet d’énumération actuel pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1b743-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="1b743-111">Pour plus d’informations sur l’énumération des tâches du dossier tâches planifiées, consultez [**IEnumWorkItems :: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span><span class="sxs-lookup"><span data-stu-id="1b743-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="1b743-112">Pour plus d’informations sur la réinitialisation de l’énumération au début de la liste, consultez [**IEnumWorkItems :: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span><span class="sxs-lookup"><span data-stu-id="1b743-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="1b743-113">Pour plus d’informations sur les tâches ignorées, consultez [**IEnumWorkItems :: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span><span class="sxs-lookup"><span data-stu-id="1b743-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="1b743-114">Pour plus d’informations sur la création d’une copie de l’objet d’énumération actuel, consultez [**IEnumWorkItems :: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span><span class="sxs-lookup"><span data-stu-id="1b743-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="1b743-115">Pour obtenir un exemple d’énumération des tâches dans le dossier tâches planifiées, consultez [exemple d’énumération de tâches](enumerating-tasks-example.md).</span><span class="sxs-lookup"><span data-stu-id="1b743-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b743-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b743-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1b743-117">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1b743-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1b743-118">Informations sur la tâche Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="1b743-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




