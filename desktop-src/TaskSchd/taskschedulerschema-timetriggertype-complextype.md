---
title: Type complexe timeTriggerType
description: Définit le type de base pour l’élément TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Planificateur de tâches de type complexe timeTriggerType
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512368"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="8fb16-104">Type complexe timeTriggerType</span><span class="sxs-lookup"><span data-stu-id="8fb16-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="8fb16-105">Définit le type de base pour l’élément [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb16-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8fb16-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8fb16-106">Child elements</span></span>



| <span data-ttu-id="8fb16-107">Élément</span><span class="sxs-lookup"><span data-stu-id="8fb16-107">Element</span></span>                                                                        | <span data-ttu-id="8fb16-108">Type</span><span class="sxs-lookup"><span data-stu-id="8fb16-108">Type</span></span>     | <span data-ttu-id="8fb16-109">Description</span><span class="sxs-lookup"><span data-stu-id="8fb16-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8fb16-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="8fb16-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="8fb16-111">duration</span><span class="sxs-lookup"><span data-stu-id="8fb16-111">duration</span></span> | <span data-ttu-id="8fb16-112">Spécifie le délai d’ajout aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="8fb16-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="8fb16-113">Le format de cette chaîne est P <days> DT <hours> H <minutes> M <seconds> S (par exemple, P2DT5S est un délai de 2 jours, 5 secondes).</span><span class="sxs-lookup"><span data-stu-id="8fb16-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8fb16-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8fb16-114">Remarks</span></span>

<span data-ttu-id="8fb16-115">Notez que cet élément n’ajoute pas d’éléments enfants à ceux définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8fb16-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb16-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fb16-116">Requirements</span></span>



| <span data-ttu-id="8fb16-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fb16-117">Requirement</span></span> | <span data-ttu-id="8fb16-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fb16-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8fb16-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fb16-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb16-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fb16-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8fb16-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fb16-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb16-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fb16-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fb16-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fb16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb16-124">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8fb16-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8fb16-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8fb16-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





