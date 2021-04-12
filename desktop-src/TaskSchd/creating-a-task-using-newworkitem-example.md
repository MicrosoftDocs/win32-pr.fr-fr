---
title: Exemple de création d’une tâche à l’aide de NewWorkItem
description: Lorsque vous créez une tâche, vous allez utiliser deux interfaces Planificateur de tâches ITaskScheduler et ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- créer des éléments de travail Planificateur de tâches
- éléments de travail Planificateur de tâches, création de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315821"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="8a40d-105">Exemple de création d’une tâche à l’aide de NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="8a40d-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="8a40d-106">Lorsque vous créez une tâche, vous allez utiliser deux interfaces de Planificateur de tâches : [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) et [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="8a40d-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="8a40d-107">Vous devez fournir un nom unique pour la tâche, l’identificateur de classe de l’objet de tâche et l’identificateur d’interface de **ITask**.</span><span class="sxs-lookup"><span data-stu-id="8a40d-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="8a40d-108">L’identificateur de classe et l’identificateur d’interface sont affichés dans l’exemple de code qui suit cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8a40d-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="8a40d-109">Vous pouvez également créer une tâche en appelant [**ITaskScheduler :: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span><span class="sxs-lookup"><span data-stu-id="8a40d-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="8a40d-110">Lorsque vous prenez cet itinéraire, il vous incombe de créer une instance de l’objet de **tâche** (qui prend en charge l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ), puis d’ajouter la tâche avec le nom que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="8a40d-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="8a40d-111">Par défaut, seul un membre du groupe administrateurs, opérateurs de sauvegarde ou opérateurs de serveur peut créer des tâches sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8a40d-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="8a40d-112">Un membre du groupe administrateurs peut modifier le descripteur de sécurité du \\ dossier de tâches Windows pour permettre aux autres utilisateurs de créer des tâches.</span><span class="sxs-lookup"><span data-stu-id="8a40d-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="8a40d-113">Le nom que vous fournissez pour la tâche doit être unique dans le dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="8a40d-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="8a40d-114">Si une tâche portant le même nom existe déjà, [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) retourne le \_ fichier d’erreurs \_ existe.</span><span class="sxs-lookup"><span data-stu-id="8a40d-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="8a40d-115">Si vous recevez cette valeur de retour, vous devez spécifier un autre nom et tenter à nouveau de créer la tâche.</span><span class="sxs-lookup"><span data-stu-id="8a40d-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="8a40d-116">La procédure suivante décrit comment créer une tâche d’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="8a40d-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="8a40d-117">**Pour créer une tâche d’élément de travail**</span><span class="sxs-lookup"><span data-stu-id="8a40d-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="8a40d-118">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="8a40d-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="8a40d-119">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="8a40d-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="8a40d-120">Appelez [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) pour créer une nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="8a40d-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="8a40d-121">(Cette méthode retourne un pointeur vers une interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="8a40d-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="8a40d-122">Enregistrez la nouvelle tâche sur le disque en appelant [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="8a40d-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="8a40d-123">(L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard prise en charge par l’interface **ITask** .)</span><span class="sxs-lookup"><span data-stu-id="8a40d-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="8a40d-124">Appelez **ITask :: Release** pour libérer toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="8a40d-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="8a40d-125">(Notez que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="8a40d-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="8a40d-126">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="8a40d-126">For a code example of</span></span>  | <span data-ttu-id="8a40d-127">Consultez</span><span class="sxs-lookup"><span data-stu-id="8a40d-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a40d-128">Création d’une tâche unique</span><span class="sxs-lookup"><span data-stu-id="8a40d-128">Creating a single task</span></span> | [<span data-ttu-id="8a40d-129">Exemple de code C/C++ : création d’une tâche à l’aide de NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="8a40d-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="8a40d-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a40d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a40d-131">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="8a40d-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 