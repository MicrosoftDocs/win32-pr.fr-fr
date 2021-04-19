---
title: Type complexe triggersType
description: Définit le groupe (triggerGroup) pour tous les éléments déclencheurs.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- Planificateur de tâches de type complexe triggersType
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517330"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="297b8-104">Type complexe triggersType</span><span class="sxs-lookup"><span data-stu-id="297b8-104">triggersType Complex Type</span></span>

<span data-ttu-id="297b8-105">Définit le groupe ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) pour tous les éléments déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="297b8-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="297b8-106">Le groupe [**triggerGroup**](taskschedulerschema-triggergroup-group.md) contient la liste des déclencheurs qui peuvent être utilisés dans une tâche.</span><span class="sxs-lookup"><span data-stu-id="297b8-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="297b8-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="297b8-107">Requirements</span></span>



| <span data-ttu-id="297b8-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="297b8-108">Requirement</span></span> | <span data-ttu-id="297b8-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="297b8-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="297b8-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="297b8-110">Minimum supported client</span></span><br/> | <span data-ttu-id="297b8-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="297b8-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="297b8-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="297b8-112">Minimum supported server</span></span><br/> | <span data-ttu-id="297b8-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="297b8-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="297b8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="297b8-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297b8-115">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="297b8-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





