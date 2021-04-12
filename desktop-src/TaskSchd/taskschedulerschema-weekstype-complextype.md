---
title: Type complexe weeksType
description: Définit l’élément enfant et les informations de séquencement de l’élément week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- Planificateur de tâches de type complexe weeksType
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105349"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="39463-104">Type complexe weeksType</span><span class="sxs-lookup"><span data-stu-id="39463-104">weeksType Complex Type</span></span>

<span data-ttu-id="39463-105">Définit l’élément enfant et les informations de séquencement de l’élément [**week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="39463-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="39463-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="39463-106">Child elements</span></span>



| <span data-ttu-id="39463-107">Élément</span><span class="sxs-lookup"><span data-stu-id="39463-107">Element</span></span>                                                    | <span data-ttu-id="39463-108">Type</span><span class="sxs-lookup"><span data-stu-id="39463-108">Type</span></span>                                                        | <span data-ttu-id="39463-109">Description</span><span class="sxs-lookup"><span data-stu-id="39463-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="39463-110">**Week**</span><span class="sxs-lookup"><span data-stu-id="39463-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="39463-111">**weekType**</span><span class="sxs-lookup"><span data-stu-id="39463-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="39463-112">Spécifie la semaine d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="39463-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="39463-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39463-113">Requirements</span></span>



| <span data-ttu-id="39463-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39463-114">Requirement</span></span> | <span data-ttu-id="39463-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="39463-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39463-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39463-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39463-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39463-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39463-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39463-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39463-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39463-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39463-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39463-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39463-121">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="39463-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





