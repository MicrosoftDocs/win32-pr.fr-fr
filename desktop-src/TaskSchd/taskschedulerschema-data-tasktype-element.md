---
title: Élément Data (taskType)
description: Définit des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Planificateur de tâches d’élément de données
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740828"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="51d2b-104">Élément Data (taskType)</span><span class="sxs-lookup"><span data-stu-id="51d2b-104">Data (taskType) Element</span></span>

<span data-ttu-id="51d2b-105">Définit des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="51d2b-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="51d2b-106">L’élément de **données** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="51d2b-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="51d2b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="51d2b-107">Parent element</span></span>



| <span data-ttu-id="51d2b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="51d2b-108">Element</span></span>                                          | <span data-ttu-id="51d2b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="51d2b-109">Derived from</span></span>                                                 | <span data-ttu-id="51d2b-110">Description</span><span class="sxs-lookup"><span data-stu-id="51d2b-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="51d2b-111">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="51d2b-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="51d2b-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="51d2b-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="51d2b-113">Définit la tâche qui est effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="51d2b-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="51d2b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="51d2b-114">Remarks</span></span>

<span data-ttu-id="51d2b-115">En guise d’exemple de ce type de données, le service de Journaux et alertes de performance utilise cette propriété comme un conteneur de stockage pour la requête de compteur de performances associée à une tâche.</span><span class="sxs-lookup"><span data-stu-id="51d2b-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="51d2b-116">Pour le développement C++, les données d’une tâche sont spécifiées à l’aide [**de la propriété de données de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span><span class="sxs-lookup"><span data-stu-id="51d2b-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="51d2b-117">Dans le développement de scripts, les données d’une tâche sont spécifiées à l’aide de la propriété [**TaskDefinition. Data**](taskdefinition-data.md) .</span><span class="sxs-lookup"><span data-stu-id="51d2b-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="51d2b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51d2b-118">Requirements</span></span>



| <span data-ttu-id="51d2b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51d2b-119">Requirement</span></span> | <span data-ttu-id="51d2b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="51d2b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51d2b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51d2b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51d2b-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51d2b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51d2b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51d2b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51d2b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51d2b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51d2b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51d2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d2b-126">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="51d2b-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="51d2b-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="51d2b-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





