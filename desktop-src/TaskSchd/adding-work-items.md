---
title: Ajouter des éléments de travail
description: Il existe deux façons d’ajouter des éléments de travail aux Tasksfolder planifiés. Vous pouvez créer un nouvel élément de travail dans le dossier, ou vous pouvez ajouter un élément de travail existant au dossier.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- éléments de travail Planificateur de tâches, ajouter
- tâches Planificateur de tâches, ajout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106527137"
---
# <a name="adding-work-items"></a><span data-ttu-id="7390f-106">Ajouter des éléments de travail</span><span class="sxs-lookup"><span data-stu-id="7390f-106">Adding Work Items</span></span>

<span data-ttu-id="7390f-107">Il existe deux façons d’ajouter des [*éléments de travail*](w.md) aux [*Tasksfolder planifiés*](s.md).</span><span class="sxs-lookup"><span data-stu-id="7390f-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="7390f-108">Vous pouvez créer un nouvel élément de travail dans le dossier, ou vous pouvez ajouter un élément de travail existant au dossier.</span><span class="sxs-lookup"><span data-stu-id="7390f-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="7390f-109">Actuellement, seuls les objets de tâche peuvent être ajoutés au dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="7390f-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="7390f-110">Lorsque vous ajoutez une tâche, vous devez connaître les identificateurs de la classe de tâche et de l’interface de tâche [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="7390f-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="7390f-111">Pour créer des éléments de travail, vous devez appeler la méthode [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) .</span><span class="sxs-lookup"><span data-stu-id="7390f-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="7390f-112">Cette méthode crée un objet d’élément de travail à l’aide du nom que vous fournissez et ajoute l’élément de travail au dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="7390f-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="7390f-113">Lorsque vous créez un élément de travail, le Planificateur de tâches alloue la mémoire requise pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="7390f-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="7390f-114">Pour ajouter des éléments de travail existants au dossier tâches planifiées, appelez la méthode [**ITaskScheduler :: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) .</span><span class="sxs-lookup"><span data-stu-id="7390f-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="7390f-115">Lorsque vous appelez cette méthode, vous devez créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="7390f-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="7390f-116">Les noms que vous fournissez pour les éléments de travail doivent être uniques dans le dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="7390f-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="7390f-117">Si un élément de travail du même nom existe déjà lorsque vous appelez la méthode [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ou la méthode [**ITaskScheduler :: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , la méthode retourne une erreur indiquant que le **fichier d’erreur \_ \_ existe** .</span><span class="sxs-lookup"><span data-stu-id="7390f-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="7390f-118">Pour plus d’informations, consultez [création d’une tâche à l’aide de l’exemple NewWorkItem](creating-a-task-using-newworkitem-example.md).</span><span class="sxs-lookup"><span data-stu-id="7390f-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




