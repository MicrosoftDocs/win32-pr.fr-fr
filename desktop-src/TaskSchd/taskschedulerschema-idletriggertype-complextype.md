---
title: Type complexe idleTriggerType
description: Définit le type de base pour l’élément IdleTrigger.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- Planificateur de tâches de type complexe idleTriggerType
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97868d5b13f224bc55661b681246be29f3a4a20b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740445"
---
# <a name="idletriggertype-complex-type"></a><span data-ttu-id="26321-104">Type complexe idleTriggerType</span><span class="sxs-lookup"><span data-stu-id="26321-104">idleTriggerType Complex Type</span></span>

<span data-ttu-id="26321-105">Définit le type de base pour l’élément [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="26321-105">Defines the base type for the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="26321-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26321-106">Requirements</span></span>



| <span data-ttu-id="26321-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26321-107">Requirement</span></span> | <span data-ttu-id="26321-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="26321-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26321-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26321-109">Minimum supported client</span></span><br/> | <span data-ttu-id="26321-110">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26321-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26321-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26321-111">Minimum supported server</span></span><br/> | <span data-ttu-id="26321-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26321-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26321-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26321-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26321-114">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26321-114">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="26321-115">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26321-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





