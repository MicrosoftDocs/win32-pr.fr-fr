---
title: Description (registrationInfoType) (élément)
description: Spécifie la description de la tâche.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Élément Description Planificateur de tâches
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740821"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="49fe8-104">Description (registrationInfoType) (élément)</span><span class="sxs-lookup"><span data-stu-id="49fe8-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="49fe8-105">Spécifie la description de la tâche.</span><span class="sxs-lookup"><span data-stu-id="49fe8-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="49fe8-106">L’élément **Description** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="49fe8-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="49fe8-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="49fe8-107">Parent element</span></span>



| <span data-ttu-id="49fe8-108">Élément</span><span class="sxs-lookup"><span data-stu-id="49fe8-108">Element</span></span>                                                                           | <span data-ttu-id="49fe8-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="49fe8-109">Derived from</span></span>                                                                         | <span data-ttu-id="49fe8-110">Description</span><span class="sxs-lookup"><span data-stu-id="49fe8-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49fe8-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="49fe8-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="49fe8-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="49fe8-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="49fe8-113">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="49fe8-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="49fe8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="49fe8-114">Remarks</span></span>

<span data-ttu-id="49fe8-115">Pour le développement de script, la description d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. Description**](registrationinfo-description.md) .</span><span class="sxs-lookup"><span data-stu-id="49fe8-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="49fe8-116">Pour le développement C++, la description d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo ::D escription**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .</span><span class="sxs-lookup"><span data-stu-id="49fe8-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="49fe8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49fe8-117">Requirements</span></span>



| <span data-ttu-id="49fe8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49fe8-118">Requirement</span></span> | <span data-ttu-id="49fe8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="49fe8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49fe8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49fe8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49fe8-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49fe8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49fe8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49fe8-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49fe8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49fe8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49fe8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fe8-125">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="49fe8-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="49fe8-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="49fe8-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





