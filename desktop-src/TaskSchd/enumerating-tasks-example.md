---
title: Exemple d’énumération de tâches
description: Pour énumérer des tâches, vous devez appeler l’énumération ITaskScheduler pour créer un objet d’énumération. Ensuite, utilisez l’interface IEnumWorkItems de l’objet d’énumération pour énumérer les tâches dans le dossier tâches planifiées.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511702"
---
# <a name="enumerating-tasks-example"></a><span data-ttu-id="67f8e-104">Exemple d’énumération de tâches</span><span class="sxs-lookup"><span data-stu-id="67f8e-104">Enumerating Tasks Example</span></span>

<span data-ttu-id="67f8e-105">Pour énumérer des tâches, vous devez appeler [**ITaskScheduler :: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) pour créer un [*objet d’énumération*](e.md).</span><span class="sxs-lookup"><span data-stu-id="67f8e-105">To enumerate tasks, you must call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to create an [*enumeration object*](e.md).</span></span> <span data-ttu-id="67f8e-106">Ensuite, utilisez l’interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de l’objet d’énumération pour énumérer les tâches dans le dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="67f8e-106">Then, use the enumeration object's [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="67f8e-107">La procédure suivante décrit comment énumérer les tâches dans le dossier tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="67f8e-107">The following procedure describes how to enumerate the tasks in the Scheduled Tasks folder.</span></span>

<span data-ttu-id="67f8e-108">**Pour énumérer les tâches du dossier tâches planifiées**</span><span class="sxs-lookup"><span data-stu-id="67f8e-108">**To enumerate the tasks in the Scheduled Tasks folder**</span></span>

1.  <span data-ttu-id="67f8e-109">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="67f8e-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="67f8e-110">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="67f8e-110">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="67f8e-111">Appelez [**ITaskScheduler :: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) pour récupérer un objet d’énumération.</span><span class="sxs-lookup"><span data-stu-id="67f8e-111">Call [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) to get an enumeration object.</span></span>
3.  <span data-ttu-id="67f8e-112">Appelez [**IEnumWorkItems :: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) pour récupérer les tâches.</span><span class="sxs-lookup"><span data-stu-id="67f8e-112">Call [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) to retrieve the tasks.</span></span> <span data-ttu-id="67f8e-113">(Cet exemple essaie de récupérer cinq tâches avec chaque appel.)</span><span class="sxs-lookup"><span data-stu-id="67f8e-113">(This example tries to retrieve five tasks with each call.)</span></span>
4.  <span data-ttu-id="67f8e-114">Traitez les tâches retournées.</span><span class="sxs-lookup"><span data-stu-id="67f8e-114">Process the tasks returned.</span></span> <span data-ttu-id="67f8e-115">(Cet exemple affiche simplement le nom de chaque tâche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="67f8e-115">(This example simply prints the name of each task to the screen.</span></span>
5.  <span data-ttu-id="67f8e-116">Libérer les ressources.</span><span class="sxs-lookup"><span data-stu-id="67f8e-116">Release resources.</span></span> <span data-ttu-id="67f8e-117">Appelez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire utilisée pour les noms.</span><span class="sxs-lookup"><span data-stu-id="67f8e-117">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory used for names.</span></span>



| <span data-ttu-id="67f8e-118">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="67f8e-118">For a code example of</span></span>                                                         | <span data-ttu-id="67f8e-119">Consultez</span><span class="sxs-lookup"><span data-stu-id="67f8e-119">See</span></span>                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="67f8e-120">Énumération de toutes les tâches dans le dossier tâches planifiées de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="67f8e-120">Enumerating all the tasks in the Scheduled Tasks folder of the local computer</span></span> | [<span data-ttu-id="67f8e-121">Exemple de code C/C++ : énumération de tâches</span><span class="sxs-lookup"><span data-stu-id="67f8e-121">C/C++ Code Example: Enumerating Tasks</span></span>](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a><span data-ttu-id="67f8e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67f8e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67f8e-123">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="67f8e-123">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 