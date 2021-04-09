---
title: Élément Date (registrationInfoType)
description: Spécifie la date et l’heure d’enregistrement de la tâche.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Élément Date Planificateur de tâches
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104635"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="7b10f-104">Élément Date (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="7b10f-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="7b10f-105">Spécifie la date et l’heure d’enregistrement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b10f-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="7b10f-106">L’élément **Date** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7b10f-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7b10f-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7b10f-107">Parent element</span></span>



| <span data-ttu-id="7b10f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7b10f-108">Element</span></span>                                                                           | <span data-ttu-id="7b10f-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7b10f-109">Derived from</span></span>                                                                         | <span data-ttu-id="7b10f-110">Description</span><span class="sxs-lookup"><span data-stu-id="7b10f-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b10f-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="7b10f-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="7b10f-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="7b10f-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="7b10f-113">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="7b10f-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7b10f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7b10f-114">Remarks</span></span>

<span data-ttu-id="7b10f-115">Pour le développement de script, la date d’inscription d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. date**](registrationinfo-date.md) .</span><span class="sxs-lookup"><span data-stu-id="7b10f-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="7b10f-116">Pour le développement C++, la date d’inscription d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo ::D ATE**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .</span><span class="sxs-lookup"><span data-stu-id="7b10f-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b10f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b10f-117">Requirements</span></span>



| <span data-ttu-id="7b10f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b10f-118">Requirement</span></span> | <span data-ttu-id="7b10f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b10f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b10f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b10f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b10f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b10f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b10f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b10f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b10f-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b10f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b10f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b10f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b10f-125">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7b10f-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7b10f-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7b10f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





