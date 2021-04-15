---
title: Type complexe bootTriggerType
description: Définit l’élément enfant et les informations de séquencement pour l’élément BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Planificateur de tâches de type complexe bootTriggerType
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466291"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="c0814-104">Type complexe bootTriggerType</span><span class="sxs-lookup"><span data-stu-id="c0814-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="c0814-105">Définit l’élément enfant et les informations de séquencement pour l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c0814-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="c0814-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c0814-106">Child elements</span></span>



| <span data-ttu-id="c0814-107">Élément</span><span class="sxs-lookup"><span data-stu-id="c0814-107">Element</span></span>                                                            | <span data-ttu-id="c0814-108">Type</span><span class="sxs-lookup"><span data-stu-id="c0814-108">Type</span></span>     | <span data-ttu-id="c0814-109">Description</span><span class="sxs-lookup"><span data-stu-id="c0814-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0814-110">**Retard**</span><span class="sxs-lookup"><span data-stu-id="c0814-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="c0814-111">duration</span><span class="sxs-lookup"><span data-stu-id="c0814-111">duration</span></span> | <span data-ttu-id="c0814-112">Intervalle de temps entre le démarrage du système et le déclenchement du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="c0814-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="c0814-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c0814-113">Remarks</span></span>

<span data-ttu-id="c0814-114">En plus de l’élément enfant défini ici, l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0814-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0814-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0814-115">Requirements</span></span>



| <span data-ttu-id="c0814-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0814-116">Requirement</span></span> | <span data-ttu-id="c0814-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0814-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0814-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0814-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0814-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0814-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0814-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0814-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0814-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0814-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0814-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0814-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0814-123">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c0814-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c0814-124">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c0814-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





