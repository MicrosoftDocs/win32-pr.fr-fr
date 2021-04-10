---
title: Élément ValueQueries (eventTriggerType)
description: Contient une séquence d’éléments qui contiennent chacun un nom et une valeur de requête XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Élément ValueQueries Planificateur de tâches
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941820"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="a1553-104">Élément ValueQueries (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="a1553-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="a1553-105">Contient une séquence d’éléments qui contiennent chacun un nom et une valeur de requête XPath.</span><span class="sxs-lookup"><span data-stu-id="a1553-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="a1553-106">Les requêtes sont appliquées à un événement renvoyé par l’abonnement à un événement spécifié dans l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1553-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="a1553-107">Le nom de la valeur de requête XPath peut être utilisé en tant que variable dans la section action d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="a1553-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="a1553-108">L’élément **ValueQueries** est défini par le type complexe [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1553-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a1553-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a1553-109">Parent element</span></span>



| <span data-ttu-id="a1553-110">Élément</span><span class="sxs-lookup"><span data-stu-id="a1553-110">Element</span></span>                                                                                      | <span data-ttu-id="a1553-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="a1553-111">Derived from</span></span>                                                                 | <span data-ttu-id="a1553-112">Description</span><span class="sxs-lookup"><span data-stu-id="a1553-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="a1553-113">**EventTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="a1553-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="a1553-114">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="a1553-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="a1553-115">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="a1553-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a1553-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a1553-116">Remarks</span></span>

<span data-ttu-id="a1553-117">Pour le développement C++, consultez la [**propriété ValueQueries de IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span><span class="sxs-lookup"><span data-stu-id="a1553-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="a1553-118">Pour le développement de scripts, consultez [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="a1553-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a1553-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="a1553-119">Examples</span></span>

<span data-ttu-id="a1553-120">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur d’événement à l’aide de cet élément, consultez [exemple de déclencheur d’événements (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1553-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1553-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1553-121">Requirements</span></span>



| <span data-ttu-id="a1553-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1553-122">Requirement</span></span> | <span data-ttu-id="a1553-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1553-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1553-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1553-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a1553-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1553-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1553-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1553-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a1553-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1553-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

