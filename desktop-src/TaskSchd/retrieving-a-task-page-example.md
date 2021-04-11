---
title: Exemple de récupération d’une page de tâche
description: Pour récupérer une page de tâche, vous devez appeler ITask QueryInterface pour récupérer l’interface IProvideTaskPage, puis appeler IProvideTaskPage GetPage. La méthode GetPage retourne un handle vers la page, qui peut ensuite être utilisé pour afficher la page que vous avez demandée.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- récupération de la page de tâches Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031407"
---
# <a name="retrieving-a-task-page-example"></a><span data-ttu-id="cc3f6-105">Exemple de récupération d’une page de tâche</span><span class="sxs-lookup"><span data-stu-id="cc3f6-105">Retrieving a Task Page Example</span></span>

<span data-ttu-id="cc3f6-106">Pour récupérer une page de tâche, vous devez appeler **ITask :: QueryInterface** pour récupérer l’interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) , puis appeler [**IProvideTaskPage :: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span><span class="sxs-lookup"><span data-stu-id="cc3f6-106">To retrieve a task page you must call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface, then call [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage).</span></span> <span data-ttu-id="cc3f6-107">La méthode **GetPage** retourne un handle vers la page, qui peut ensuite être utilisé pour afficher la page que vous avez demandée.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-107">The **GetPage** method returns a handle to the page, which can then be used to display the page you requested.</span></span>

> [!Note]  
> <span data-ttu-id="cc3f6-108">Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="cc3f6-109">La procédure suivante décrit comment créer un nouveau déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-109">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="cc3f6-110">**Pour créer un déclencheur**</span><span class="sxs-lookup"><span data-stu-id="cc3f6-110">**To create a new trigger**</span></span>

1.  <span data-ttu-id="cc3f6-111">Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="cc3f6-112">(Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)</span><span class="sxs-lookup"><span data-stu-id="cc3f6-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="cc3f6-113">Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="cc3f6-114">(Notez que cet exemple obtient la tâche « tester la tâche ».)</span><span class="sxs-lookup"><span data-stu-id="cc3f6-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="cc3f6-115">Appelez **ITask :: QueryInterface** pour récupérer l’interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) et [**IProvideTaskPage :: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) pour récupérer la page.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-115">Call **ITask::QueryInterface** to retrieve the [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) interface and [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) to retrieve the page.</span></span>
4.  <span data-ttu-id="cc3f6-116">À l’aide du handle de page retourné, affichez la page.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-116">Using the returned page handle, display the page.</span></span>



| <span data-ttu-id="cc3f6-117">Pour obtenir un exemple de code de</span><span class="sxs-lookup"><span data-stu-id="cc3f6-117">For a code example of</span></span>                                   | <span data-ttu-id="cc3f6-118">Consultez</span><span class="sxs-lookup"><span data-stu-id="cc3f6-118">See</span></span>                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="cc3f6-119">Récupération et affichage de la page de tâche d’une tâche connue</span><span class="sxs-lookup"><span data-stu-id="cc3f6-119">Retrieving and displaying the Task page of a known task</span></span> | [<span data-ttu-id="cc3f6-120">Récupération d’une page de tâche</span><span class="sxs-lookup"><span data-stu-id="cc3f6-120">Retrieving a Task Page</span></span>](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a><span data-ttu-id="cc3f6-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc3f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc3f6-122">Exemples de Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="cc3f6-122">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 