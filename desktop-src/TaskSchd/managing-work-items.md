---
title: Manipuler des éléments de travail
description: L’interface IScheduledWorkItem fournit des méthodes pour récupérer et définir des propriétés d’élément de travail ; création, récupération et suppression de déclencheurs pour les éléments de travail (la définition du déclencheur doit être effectuée à l’aide de la méthode ITaskTrigger SetTrigger); et pour exécuter, terminer et supprimer l’élément de travail. Remarque pour les propriétés d’un type d’élément de travail spécifique, reportez-vous à l’interface de ce type d’objet. Par exemple, vous ne pouvez pas définir le niveau de priorité d’un élément de travail ; Toutefois, vous pouvez utiliser les méthodes de l’interface ITask pour récupérer et définir la priorité d’une tâche.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- éléments de travail Planificateur de tâches, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728548"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="d194a-105">Manipuler des éléments de travail</span><span class="sxs-lookup"><span data-stu-id="d194a-105">Manipulating Work Items</span></span>

<span data-ttu-id="d194a-106">L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fournit des méthodes pour récupérer et définir des propriétés d’élément de travail ; création, récupération et suppression de déclencheurs pour les éléments de travail (la définition du déclencheur doit être effectuée à l’aide de la méthode [**ITaskTrigger :: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); et pour exécuter, terminer et supprimer l’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="d194a-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="d194a-107">Pour les propriétés d’un type d’élément de travail spécifique, reportez-vous à l’interface de ce type d’objet.</span><span class="sxs-lookup"><span data-stu-id="d194a-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="d194a-108">Par exemple, vous ne pouvez pas définir le niveau de priorité d’un élément de travail ; Toutefois, vous pouvez utiliser les méthodes de l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) pour récupérer et définir la priorité d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="d194a-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="d194a-109">Chaque fois que vous modifiez un élément de travail, vous devez appeler l’objet [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer l’élément de travail modifié sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d194a-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="d194a-110">L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard qui est prise en charge par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="d194a-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="d194a-111">Pour obtenir des exemples de</span><span class="sxs-lookup"><span data-stu-id="d194a-111">For examples of</span></span>                                                            | <span data-ttu-id="d194a-112">Consultez</span><span class="sxs-lookup"><span data-stu-id="d194a-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d194a-113">Récupération des propriétés qui s’appliquent à tous les types d’éléments de travail</span><span class="sxs-lookup"><span data-stu-id="d194a-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="d194a-114">Récupération d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="d194a-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="d194a-115">Définition des propriétés qui s’appliquent à tous les types d’éléments de travail</span><span class="sxs-lookup"><span data-stu-id="d194a-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="d194a-116">Définition d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="d194a-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="d194a-117">Exécution d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="d194a-117">Running a known task</span></span>                                                       | [<span data-ttu-id="d194a-118">Exemple de démarrage d’une tâche</span><span class="sxs-lookup"><span data-stu-id="d194a-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="d194a-119">Fin d’une tâche en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="d194a-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="d194a-120">Exemple de fin d’une tâche</span><span class="sxs-lookup"><span data-stu-id="d194a-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="d194a-121">Création d’un déclencheur pour une tâche connue</span><span class="sxs-lookup"><span data-stu-id="d194a-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="d194a-122">Création d’un déclencheur</span><span class="sxs-lookup"><span data-stu-id="d194a-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="d194a-123">Création d’un déclencheur inactif basé sur des événements pour une tâche connue</span><span class="sxs-lookup"><span data-stu-id="d194a-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="d194a-124">Exemple de création d’un déclencheur inactif</span><span class="sxs-lookup"><span data-stu-id="d194a-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="d194a-125">Récupération de la chaîne de déclenchement de tous les déclencheurs associés à une tâche connue</span><span class="sxs-lookup"><span data-stu-id="d194a-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="d194a-126">Exemple de récupération de chaînes de déclencheur</span><span class="sxs-lookup"><span data-stu-id="d194a-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 