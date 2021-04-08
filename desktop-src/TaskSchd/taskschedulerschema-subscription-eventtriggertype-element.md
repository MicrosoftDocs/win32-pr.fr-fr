---
title: Élément Subscription (eventTriggerType)
description: Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Planificateur de tâches d’élément d’abonnement
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743765"
---
# <a name="subscription-eventtriggertype-element"></a><span data-ttu-id="ca523-104">Élément Subscription (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="ca523-104">Subscription (eventTriggerType) Element</span></span>

<span data-ttu-id="ca523-105">Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="ca523-105">Specifies the XPath query that identifies the event that fires the trigger.</span></span>

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

<span data-ttu-id="ca523-106">L’élément d' **abonnement** est défini par le type complexe [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ca523-106">The **Subscription** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ca523-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ca523-107">Parent element</span></span>



| <span data-ttu-id="ca523-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ca523-108">Element</span></span>                                                                       | <span data-ttu-id="ca523-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ca523-109">Derived from</span></span>                                                                 | <span data-ttu-id="ca523-110">Description</span><span class="sxs-lookup"><span data-stu-id="ca523-110">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="ca523-111">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="ca523-111">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="ca523-112">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ca523-112">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="ca523-113">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="ca523-113">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ca523-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ca523-114">Remarks</span></span>

<span data-ttu-id="ca523-115">Pour le développement de script, l’abonnement aux événements est spécifié par la propriété [**EventTrigger. subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="ca523-115">For script development, the event subscription is specified by the [**EventTrigger.Subscription**](eventtrigger-subscription.md) property.</span></span>

<span data-ttu-id="ca523-116">Pour le développement C++, l’abonnement aux événements est spécifié par la propriété [**IEventTrigger :: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .</span><span class="sxs-lookup"><span data-stu-id="ca523-116">For C++ development, the event subscription is specified by the [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca523-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca523-117">Requirements</span></span>



| <span data-ttu-id="ca523-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca523-118">Requirement</span></span> | <span data-ttu-id="ca523-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca523-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ca523-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca523-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca523-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca523-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ca523-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca523-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca523-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca523-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca523-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca523-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca523-125">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ca523-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ca523-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ca523-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





