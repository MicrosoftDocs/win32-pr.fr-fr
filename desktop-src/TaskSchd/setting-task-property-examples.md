---
title: Définition des exemples de propriétés de tâche
description: Pour définir les propriétés d’une tâche, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet de tâche, puis appelez la méthode ITask appropriée pour définir la propriété de tâche qui vous intéresse.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- définition des propriétés de la tâche Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518022"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="adcba-104">Définition des exemples de propriétés de tâche</span><span class="sxs-lookup"><span data-stu-id="adcba-104">Setting Task Property Examples</span></span>

<span data-ttu-id="adcba-105">Pour définir les propriétés d’une tâche, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface de l’objet de tâche, puis appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour définir la propriété de tâche qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="adcba-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="adcba-106">Les exemples de code répertoriés en bas de la page montrent comment définir les propriétés qui sont propres aux objets de tâche.</span><span class="sxs-lookup"><span data-stu-id="adcba-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="adcba-107">Pour les autres propriétés d' [*élément de travail*](w.md) qui s’appliquent également aux tâches, consultez Définition d’exemples de propriétés d' [élément de travail](setting-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="adcba-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="adcba-108">Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="adcba-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="adcba-109">Dans les exemples suivants, l’objet de tâche modifié est toujours enregistré sur le disque par un appel à [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="adcba-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="adcba-110">(L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard héritée par l’objet Task.)</span><span class="sxs-lookup"><span data-stu-id="adcba-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="adcba-111">La procédure suivante décrit comment définir une propriété de tâche.</span><span class="sxs-lookup"><span data-stu-id="adcba-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="adcba-112">**Pour définir une propriété de tâche**</span><span class="sxs-lookup"><span data-stu-id="adcba-112">**To set a task property**</span></span>

1.  <span data-ttu-id="adcba-113">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="adcba-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="adcba-114">(Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="adcba-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="adcba-115">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="adcba-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="adcba-116">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="adcba-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="adcba-117">Appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour définir la propriété qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="adcba-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="adcba-118">Appelez [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour stocker l’objet de tâche modifié sur le disque.</span><span class="sxs-lookup"><span data-stu-id="adcba-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="adcba-119">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="adcba-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="adcba-120">Consultez</span><span class="sxs-lookup"><span data-stu-id="adcba-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adcba-121">Définition du nom de l’application associée à une tâche connue</span><span class="sxs-lookup"><span data-stu-id="adcba-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="adcba-122">Exemple de code C/C++ : définition du nom de l’application</span><span class="sxs-lookup"><span data-stu-id="adcba-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="adcba-123">Définition de la durée maximale d’exécution d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="adcba-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="adcba-124">Exemple de code C/C++ : définition de durée maximale</span><span class="sxs-lookup"><span data-stu-id="adcba-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="adcba-125">Effacement de tous les paramètres de ligne de commande associés à une tâche connue</span><span class="sxs-lookup"><span data-stu-id="adcba-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="adcba-126">Exemple de code C/C++ : définition de paramètres de tâche</span><span class="sxs-lookup"><span data-stu-id="adcba-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="adcba-127">Cet exemple définit la priorité d’une tâche de test, puis enregistre la tâche.</span><span class="sxs-lookup"><span data-stu-id="adcba-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="adcba-128">Cet exemple suppose que la tâche de test existe déjà sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="adcba-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="adcba-129">Exemple de code C/C++ : définition de la priorité de la tâche</span><span class="sxs-lookup"><span data-stu-id="adcba-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="adcba-130">Définition du [*Répertoire de travail*](w.md) d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="adcba-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="adcba-131">Exemple de code C/C++ : définition du répertoire de travail</span><span class="sxs-lookup"><span data-stu-id="adcba-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="adcba-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="adcba-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adcba-133">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="adcba-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 