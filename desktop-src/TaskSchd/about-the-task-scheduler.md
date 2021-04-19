---
title: À propos de l’Planificateur de tâches
description: Le service Planificateur de tâches vous permet d’effectuer des tâches automatisées sur un ordinateur choisi.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Planificateur de tâches Planificateur de tâches, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545732"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="6f822-104">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6f822-104">About the Task Scheduler</span></span>

<span data-ttu-id="6f822-105">Le service Planificateur de tâches vous permet d’effectuer des tâches automatisées sur un ordinateur choisi.</span><span class="sxs-lookup"><span data-stu-id="6f822-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="6f822-106">Avec ce service, vous pouvez planifier l’exécution de n’importe quel programme à un moment opportun pour vous ou quand un événement spécifique se produit.</span><span class="sxs-lookup"><span data-stu-id="6f822-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="6f822-107">Le Planificateur de tâches surveille l’heure ou les critères d’événement que vous choisissez, puis exécute la tâche lorsque ces critères sont satisfaits.</span><span class="sxs-lookup"><span data-stu-id="6f822-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="6f822-108">Emplacement d’installation de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6f822-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="6f822-109">Le Planificateur de tâches est installé automatiquement avec plusieurs systèmes d’exploitation Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f822-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="6f822-110">Planificateur de tâches 1,0 est installé avec les systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6f822-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="6f822-111">Planificateur de tâches 2,0 est installé avec Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6f822-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="6f822-112">L’API Planificateur de tâches 2,0 doit être utilisée pour développer des applications qui utilisent le service Planificateur de tâches sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f822-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="6f822-113">Pour plus d’informations, consultez [Planificateur de tâches référence](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6f822-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="6f822-114">Planificateur de tâches est démarré à chaque démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6f822-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="6f822-115">Il peut être exécuté par le biais de l’interface utilisateur graphique (GUI) Planificateur de tâches ou via l’API Planificateur de tâches décrite dans ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="6f822-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="6f822-116">Informations sur les tâches</span><span class="sxs-lookup"><span data-stu-id="6f822-116">Information about Tasks</span></span>

<span data-ttu-id="6f822-117">Les tâches sont le composant principal du Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="6f822-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="6f822-118">Pour plus d’informations sur les tâches et leurs composants, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f822-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="6f822-119">Tâches</span><span class="sxs-lookup"><span data-stu-id="6f822-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="6f822-120">Actions de tâche</span><span class="sxs-lookup"><span data-stu-id="6f822-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="6f822-121">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="6f822-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="6f822-122">Informations d’inscription de la tâche</span><span class="sxs-lookup"><span data-stu-id="6f822-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="6f822-123">Conditions d’inactivité de la tâche</span><span class="sxs-lookup"><span data-stu-id="6f822-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="6f822-124">Contextes de sécurité pour les tâches</span><span class="sxs-lookup"><span data-stu-id="6f822-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="6f822-125">Répétition d’une tâche</span><span class="sxs-lookup"><span data-stu-id="6f822-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="6f822-126">Maintenance automatique</span><span class="sxs-lookup"><span data-stu-id="6f822-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="6f822-127">Pour plus d’informations et des exemples sur l’utilisation des interfaces Planificateur de tâches, les objets de script et XML, consultez [utilisation du planificateur de tâches](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="6f822-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f822-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f822-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f822-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6f822-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




