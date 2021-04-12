---
title: Type complexe registrationTriggerType
description: Définit des éléments enfants et des informations de séquencement pour l’élément RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- Planificateur de tâches de type complexe registrationTriggerType
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384999"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="15bbe-104">Type complexe registrationTriggerType</span><span class="sxs-lookup"><span data-stu-id="15bbe-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="15bbe-105">Définit des éléments enfants et des informations de séquencement pour l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="15bbe-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="15bbe-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="15bbe-106">Child elements</span></span>



| <span data-ttu-id="15bbe-107">Élément</span><span class="sxs-lookup"><span data-stu-id="15bbe-107">Element</span></span>                                                                    | <span data-ttu-id="15bbe-108">Type</span><span class="sxs-lookup"><span data-stu-id="15bbe-108">Type</span></span>     | <span data-ttu-id="15bbe-109">Description</span><span class="sxs-lookup"><span data-stu-id="15bbe-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15bbe-110">**Retard**</span><span class="sxs-lookup"><span data-stu-id="15bbe-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="15bbe-111">duration</span><span class="sxs-lookup"><span data-stu-id="15bbe-111">duration</span></span> | <span data-ttu-id="15bbe-112">Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="15bbe-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="15bbe-113">Notes</span><span class="sxs-lookup"><span data-stu-id="15bbe-113">Remarks</span></span>

<span data-ttu-id="15bbe-114">Outre les éléments enfants définis ici, l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="15bbe-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="15bbe-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15bbe-115">Requirements</span></span>



| <span data-ttu-id="15bbe-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15bbe-116">Requirement</span></span> | <span data-ttu-id="15bbe-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="15bbe-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15bbe-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15bbe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15bbe-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15bbe-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15bbe-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15bbe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15bbe-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15bbe-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15bbe-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15bbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15bbe-123">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="15bbe-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="15bbe-124">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="15bbe-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





