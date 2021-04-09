---
title: Type simple priorityType
description: Définit les valeurs minimales et maximales de l’élément Priority (settingsType).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- Planificateur de tâches de type simple priorityType
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033103"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="23b2f-104">Type simple priorityType</span><span class="sxs-lookup"><span data-stu-id="23b2f-104">priorityType Simple Type</span></span>

<span data-ttu-id="23b2f-105">Définit les valeurs minimales et maximales de l’élément [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="23b2f-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="23b2f-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="23b2f-106">Enumeration values</span></span>

<span data-ttu-id="23b2f-107">Le type simple **priorityType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="23b2f-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="23b2f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="23b2f-108">Value</span></span> | <span data-ttu-id="23b2f-109">Description</span><span class="sxs-lookup"><span data-stu-id="23b2f-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="23b2f-110">0</span><span class="sxs-lookup"><span data-stu-id="23b2f-110">0</span></span>     | <span data-ttu-id="23b2f-111">Entier minimal autorisé.</span><span class="sxs-lookup"><span data-stu-id="23b2f-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="23b2f-112">10</span><span class="sxs-lookup"><span data-stu-id="23b2f-112">10</span></span>    | <span data-ttu-id="23b2f-113">Entier maximal autorisé.</span><span class="sxs-lookup"><span data-stu-id="23b2f-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="23b2f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23b2f-114">Requirements</span></span>



| <span data-ttu-id="23b2f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23b2f-115">Requirement</span></span> | <span data-ttu-id="23b2f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="23b2f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23b2f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23b2f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="23b2f-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23b2f-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23b2f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23b2f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="23b2f-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23b2f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23b2f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23b2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b2f-122">Types simples de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="23b2f-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="23b2f-123">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="23b2f-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





