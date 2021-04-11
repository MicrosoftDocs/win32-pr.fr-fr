---
title: Élément SecurityDescriptor (registrationInfoType)
description: Spécifie le descripteur de sécurité de la tâche.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Élément SecurityDescriptor Planificateur de tâches
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032532"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="b553f-104">Élément SecurityDescriptor (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="b553f-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="b553f-105">Spécifie le descripteur de sécurité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="b553f-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="b553f-106">L’élément **SecurityDescriptor** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b553f-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b553f-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b553f-107">Parent element</span></span>



| <span data-ttu-id="b553f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b553f-108">Element</span></span>                                                                           | <span data-ttu-id="b553f-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b553f-109">Derived from</span></span>                                                                         | <span data-ttu-id="b553f-110">Description</span><span class="sxs-lookup"><span data-stu-id="b553f-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b553f-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b553f-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="b553f-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="b553f-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="b553f-113">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="b553f-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b553f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b553f-114">Remarks</span></span>

<span data-ttu-id="b553f-115">Pour le développement de scripts, le descripteur de sécurité d’une tâche est spécifié à l’aide de la propriété [**RegistrationInfo. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="b553f-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="b553f-116">Pour le développement C++, le descripteur de sécurité d’une tâche est spécifié à l’aide de la propriété [**IRegistrationInfo :: SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b553f-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b553f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b553f-117">Requirements</span></span>



| <span data-ttu-id="b553f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b553f-118">Requirement</span></span> | <span data-ttu-id="b553f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b553f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b553f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b553f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b553f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b553f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b553f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b553f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b553f-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b553f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b553f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b553f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b553f-125">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b553f-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b553f-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b553f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





