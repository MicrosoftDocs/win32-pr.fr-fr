---
title: Élément documentation (registrationInfoType)
description: Spécifie toute documentation supplémentaire pour la tâche.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Planificateur de tâches d’élément de documentation
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515483"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="7b9b3-104">Élément documentation (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="7b9b3-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="7b9b3-105">Spécifie toute documentation supplémentaire pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b9b3-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="7b9b3-106">L’élément **documentation** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7b9b3-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7b9b3-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7b9b3-107">Parent element</span></span>



| <span data-ttu-id="7b9b3-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7b9b3-108">Element</span></span>                                                                           | <span data-ttu-id="7b9b3-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7b9b3-109">Derived from</span></span>                                                                         | <span data-ttu-id="7b9b3-110">Description</span><span class="sxs-lookup"><span data-stu-id="7b9b3-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b9b3-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="7b9b3-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="7b9b3-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="7b9b3-113">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="7b9b3-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7b9b3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7b9b3-114">Remarks</span></span>

<span data-ttu-id="7b9b3-115">Pour les applications de script, une documentation supplémentaire sur les tâches est spécifiée à l’aide de la propriété [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) .</span><span class="sxs-lookup"><span data-stu-id="7b9b3-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="7b9b3-116">Pour les applications C++, une documentation supplémentaire sur les tâches est spécifiée à l’aide de la propriété [**IRegistrationInfo ::D ocumentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .</span><span class="sxs-lookup"><span data-stu-id="7b9b3-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9b3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b9b3-117">Requirements</span></span>



| <span data-ttu-id="7b9b3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b9b3-118">Requirement</span></span> | <span data-ttu-id="7b9b3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b9b3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b9b3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9b3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9b3-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9b3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b9b3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9b3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9b3-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9b3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b9b3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b9b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9b3-125">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7b9b3-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





