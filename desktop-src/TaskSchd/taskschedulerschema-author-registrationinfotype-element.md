---
title: Élément Author (registrationInfoType)
description: Spécifie l’auteur de la tâche.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Élément author Planificateur de tâches
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942346"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="cc7c4-104">Élément Author (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="cc7c4-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="cc7c4-105">Spécifie l’auteur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="cc7c4-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="cc7c4-106">L’élément **Author** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cc7c4-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cc7c4-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="cc7c4-107">Parent element</span></span>



| <span data-ttu-id="cc7c4-108">Élément</span><span class="sxs-lookup"><span data-stu-id="cc7c4-108">Element</span></span>                                                                           | <span data-ttu-id="cc7c4-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="cc7c4-109">Derived from</span></span>                                                                         | <span data-ttu-id="cc7c4-110">Description</span><span class="sxs-lookup"><span data-stu-id="cc7c4-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc7c4-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="cc7c4-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="cc7c4-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="cc7c4-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="cc7c4-113">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="cc7c4-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cc7c4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="cc7c4-114">Remarks</span></span>

<span data-ttu-id="cc7c4-115">Pour le développement de script, l’auteur de la tâche est spécifié à l’aide de la propriété [**RegistrationInfo. Author**](registrationinfo-author.md) .</span><span class="sxs-lookup"><span data-stu-id="cc7c4-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="cc7c4-116">Pour le développement C++, l’auteur de la tâche est spécifié à l’aide de la propriété [**IRegistrationInfo :: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .</span><span class="sxs-lookup"><span data-stu-id="cc7c4-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="cc7c4-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="cc7c4-117">Examples</span></span>

<span data-ttu-id="cc7c4-118">Le code XML suivant définit l’auteur d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="cc7c4-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="cc7c4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc7c4-119">Requirements</span></span>



| <span data-ttu-id="cc7c4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc7c4-120">Requirement</span></span> | <span data-ttu-id="cc7c4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc7c4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc7c4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc7c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc7c4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc7c4-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc7c4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc7c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc7c4-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc7c4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc7c4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc7c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7c4-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cc7c4-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="cc7c4-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cc7c4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





