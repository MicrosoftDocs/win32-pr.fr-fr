---
title: Type complexe eventTriggerType
description: Définit les éléments enfants et les informations de séquencement pour l’élément EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Planificateur de tâches de type complexe eventTriggerType
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538612"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="93985-104">Type complexe eventTriggerType</span><span class="sxs-lookup"><span data-stu-id="93985-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="93985-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="93985-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="93985-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="93985-106">Child elements</span></span>



| <span data-ttu-id="93985-107">Élément</span><span class="sxs-lookup"><span data-stu-id="93985-107">Element</span></span>                                                                           | <span data-ttu-id="93985-108">Type</span><span class="sxs-lookup"><span data-stu-id="93985-108">Type</span></span>                                                                    | <span data-ttu-id="93985-109">Description</span><span class="sxs-lookup"><span data-stu-id="93985-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93985-110">**Retard**</span><span class="sxs-lookup"><span data-stu-id="93985-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="93985-111">duration</span><span class="sxs-lookup"><span data-stu-id="93985-111">duration</span></span>                                                                | <span data-ttu-id="93985-112">Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="93985-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="93985-113">**Abonnement**</span><span class="sxs-lookup"><span data-stu-id="93985-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="93985-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="93985-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="93985-115">Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="93985-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="93985-116">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="93985-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="93985-117">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="93985-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="93985-118">Spécifie une séquence d’éléments qui contiennent chacun un nom et une valeur de requête XPath.</span><span class="sxs-lookup"><span data-stu-id="93985-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="93985-119">Les requêtes sont appliquées à un événement renvoyé par l’abonnement à un événement spécifié dans l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="93985-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="93985-120">Le nom de la valeur de requête XPath peut être utilisé en tant que variable dans l’élément [**Body**](taskschedulerschema-body-showmessagetype-element.md) de la section d’action [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="93985-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="93985-121">Notes</span><span class="sxs-lookup"><span data-stu-id="93985-121">Remarks</span></span>

<span data-ttu-id="93985-122">En plus de l’élément enfant défini ici, l’élément [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) utilise également des éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="93985-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="93985-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93985-123">Requirements</span></span>



| <span data-ttu-id="93985-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93985-124">Requirement</span></span> | <span data-ttu-id="93985-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="93985-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93985-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93985-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93985-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93985-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93985-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93985-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93985-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93985-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93985-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93985-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93985-131">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="93985-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="93985-132">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="93985-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





