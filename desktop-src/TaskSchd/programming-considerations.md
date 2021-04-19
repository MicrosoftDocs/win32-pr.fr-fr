---
title: Considérations relatives à la programmation (Planificateur de tâches)
description: Lorsque vous développez des applications qui utilisent le Planificateur de tâches 1,0, gardez à l’esprit les problèmes de programmation suivants. Votre application doit s’assurer que le service Planificateur de tâches est en cours d’exécution avant d’essayer d’effectuer des appels à l’aide de l’API Planificateur de tâches. Lorsque vous récupérez des chaînes, veillez à appeler CoTaskMemFree pour libérer chaque chaîne une fois qu’elle n’est plus nécessaire. Lorsque vous récupérez des tableaux de chaînes, assurez-vous d’abord de libérer chaque chaîne dans le tableau, puis de libérer le tableau lui-même. Lors de la création ou de la modification d’un élément de travail, y compris les déclencheurs associés à un élément de travail, veillez à appeler IPersistFile Save pour enregistrer l’élément de travail sur le disque. Après avoir utilisé l’une des interfaces fournies par l’API Planificateur de tâches, veillez à appeler la version d’IUnknown pour libérer l’interface. IUnknown est pris en charge par chaque objet Planificateur de tâches.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- démarrage de Planificateur de tâches
- considérations relatives à la programmation Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510293"
---
# <a name="programming-considerations-task-scheduler"></a><span data-ttu-id="83721-107">Considérations relatives à la programmation (Planificateur de tâches)</span><span class="sxs-lookup"><span data-stu-id="83721-107">Programming Considerations (Task Scheduler)</span></span>

<span data-ttu-id="83721-108">Lorsque vous développez des applications qui utilisent le Planificateur de tâches 1,0, gardez à l’esprit les problèmes de programmation suivants.</span><span class="sxs-lookup"><span data-stu-id="83721-108">When developing applications that use the Task Scheduler 1.0, keep the following programming issues in mind.</span></span>

-   <span data-ttu-id="83721-109">Votre application doit s’assurer que le service Planificateur de tâches est en cours d’exécution avant d’essayer d’effectuer des appels à l’aide de l’API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="83721-109">Your application must ensure the Task Scheduler service is running before attempting to make any calls using the Task Scheduler API.</span></span>
-   <span data-ttu-id="83721-110">Lorsque vous récupérez des chaînes, veillez à appeler [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer chaque chaîne une fois qu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="83721-110">When retrieving strings, make sure that you call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release each string after it is no longer needed.</span></span> <span data-ttu-id="83721-111">Lorsque vous récupérez des tableaux de chaînes, assurez-vous d’abord de libérer chaque chaîne dans le tableau, puis de libérer le tableau lui-même.</span><span class="sxs-lookup"><span data-stu-id="83721-111">When retrieving arrays of strings, make sure you first release each string in the array and then release the array itself.</span></span>
-   <span data-ttu-id="83721-112">Lors de la création ou de la modification d’un élément de travail, y compris les déclencheurs associés à un élément de travail, veillez à appeler [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer l’élément de travail sur le disque.</span><span class="sxs-lookup"><span data-stu-id="83721-112">When creating or modifying a work item, including triggers associated with a work item, make sure you call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the work item to disk.</span></span>
-   <span data-ttu-id="83721-113">Après avoir utilisé l’une des interfaces fournies par l’API Planificateur de tâches, veillez à appeler [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="83721-113">After using any of the interfaces that are provided by the Task Scheduler API, make sure you call [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the interface.</span></span> <span data-ttu-id="83721-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) est pris en charge par chaque objet planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="83721-114">[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is supported by each Task Scheduler object.</span></span>

<span data-ttu-id="83721-115">La section utilisation de la documentation Planificateur de tâches fournit de nombreux exemples qui suivent ces instructions.</span><span class="sxs-lookup"><span data-stu-id="83721-115">The Using section of the Task Scheduler documentation provides numerous examples that follow these guidelines.</span></span> <span data-ttu-id="83721-116">Le tableau ci-dessous fournit des liens vers certains de ces exemples.</span><span class="sxs-lookup"><span data-stu-id="83721-116">The table below provides jumps to some of these examples.</span></span>

| <span data-ttu-id="83721-117">Pour obtenir un exemple de</span><span class="sxs-lookup"><span data-stu-id="83721-117">For an example of</span></span>         | <span data-ttu-id="83721-118">Consultez</span><span class="sxs-lookup"><span data-stu-id="83721-118">See</span></span>                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="83721-119">Libérer des chaînes</span><span class="sxs-lookup"><span data-stu-id="83721-119">Releasing strings</span></span>         | [<span data-ttu-id="83721-120">Récupération d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="83721-120">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="83721-121">Enregistrement des éléments de travail sur le disque</span><span class="sxs-lookup"><span data-stu-id="83721-121">Saving work items to disk</span></span> | [<span data-ttu-id="83721-122">Définition d’exemples de propriétés d’élément de travail</span><span class="sxs-lookup"><span data-stu-id="83721-122">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |
| <span data-ttu-id="83721-123">Libérer des interfaces</span><span class="sxs-lookup"><span data-stu-id="83721-123">Releasing interfaces</span></span>      | [<span data-ttu-id="83721-124">Exemple de création d’une tâche à l’aide de NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="83721-124">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |



 

 

 
