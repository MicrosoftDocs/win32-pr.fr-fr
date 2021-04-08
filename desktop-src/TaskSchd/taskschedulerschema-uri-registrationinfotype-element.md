---
title: Élément URI (registrationInfoType)
description: Spécifie l’URI de la tâche.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Élément URI Planificateur de tâches
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743749"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="f01e2-104">Élément URI (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="f01e2-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="f01e2-105">Spécifie l’URI de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f01e2-105">Specifies the URI of the task.</span></span> <span data-ttu-id="f01e2-106">Cet élément est utilisé pour spécifier l’emplacement de la tâche inscrite dans l’arborescence des dossiers des tâches.</span><span class="sxs-lookup"><span data-stu-id="f01e2-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="f01e2-107">L’élément **URI** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f01e2-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f01e2-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f01e2-108">Parent element</span></span>



| <span data-ttu-id="f01e2-109">Élément</span><span class="sxs-lookup"><span data-stu-id="f01e2-109">Element</span></span>                                                                           | <span data-ttu-id="f01e2-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f01e2-110">Derived from</span></span>                                                                         | <span data-ttu-id="f01e2-111">Description</span><span class="sxs-lookup"><span data-stu-id="f01e2-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f01e2-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="f01e2-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="f01e2-113">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="f01e2-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="f01e2-114">Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="f01e2-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f01e2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f01e2-115">Remarks</span></span>

<span data-ttu-id="f01e2-116">Pour le développement de script, l’URI de la tâche est spécifié à l’aide de la propriété [**RegistrationInfo. Uri**](registrationinfo-uri.md) .</span><span class="sxs-lookup"><span data-stu-id="f01e2-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="f01e2-117">Pour le développement C++, l’URI de la tâche est spécifié à l’aide de la propriété [**IRegistrationInfo :: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .</span><span class="sxs-lookup"><span data-stu-id="f01e2-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01e2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f01e2-118">Requirements</span></span>



| <span data-ttu-id="f01e2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f01e2-119">Requirement</span></span> | <span data-ttu-id="f01e2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f01e2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f01e2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f01e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f01e2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f01e2-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f01e2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f01e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f01e2-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f01e2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f01e2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f01e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01e2-126">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f01e2-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f01e2-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f01e2-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





