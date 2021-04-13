---
title: Élément source (registrationInfoType)
description: Spécifie l’origine de la tâche. Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Planificateur de tâches de l’élément source
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384095"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="457cc-105">Élément source (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="457cc-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="457cc-106">Spécifie l’origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="457cc-106">Specifies where the task originated from.</span></span> <span data-ttu-id="457cc-107">Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="457cc-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="457cc-108">L’élément **source** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="457cc-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="457cc-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="457cc-109">Parent element</span></span>



| <span data-ttu-id="457cc-110">Élément</span><span class="sxs-lookup"><span data-stu-id="457cc-110">Element</span></span>                                                                           | <span data-ttu-id="457cc-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="457cc-111">Derived from</span></span>                                                                         | <span data-ttu-id="457cc-112">Description</span><span class="sxs-lookup"><span data-stu-id="457cc-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="457cc-113">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="457cc-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="457cc-114">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="457cc-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="457cc-115">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="457cc-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="457cc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="457cc-116">Remarks</span></span>

<span data-ttu-id="457cc-117">Pour le développement de script, la source d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. source**](registrationinfo-source.md) .</span><span class="sxs-lookup"><span data-stu-id="457cc-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="457cc-118">Pour le développement C++, la source d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo :: source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .</span><span class="sxs-lookup"><span data-stu-id="457cc-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="457cc-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="457cc-119">Requirements</span></span>



| <span data-ttu-id="457cc-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="457cc-120">Requirement</span></span> | <span data-ttu-id="457cc-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="457cc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="457cc-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="457cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="457cc-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="457cc-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="457cc-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="457cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="457cc-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="457cc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="457cc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="457cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457cc-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="457cc-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="457cc-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="457cc-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





