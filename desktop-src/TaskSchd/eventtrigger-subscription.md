---
title: Propriété EventTrigger. subscription
description: Pour les scripts, obtient ou définit une chaîne de requête qui identifie l’événement qui déclenche le déclencheur.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Planificateur de tâches de propriété d’abonnement
- Planificateur de tâches de propriété d’abonnement, objet EventTrigger
- Objet EventTrigger Planificateur de tâches, propriété Subscription
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512185"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="bcf37-106">Propriété EventTrigger. subscription</span><span class="sxs-lookup"><span data-stu-id="bcf37-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="bcf37-107">Pour les scripts, obtient ou définit une chaîne de requête qui identifie l’événement qui déclenche le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="bcf37-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf37-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcf37-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="bcf37-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bcf37-109">Property value</span></span>

<span data-ttu-id="bcf37-110">Chaîne de requête qui identifie l’événement qui déclenche le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="bcf37-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf37-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bcf37-111">Remarks</span></span>

<span data-ttu-id="bcf37-112">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, l’abonnement aux événements est spécifié à l’aide de l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="bcf37-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="bcf37-113">Pour plus d’informations sur l’écriture d’une chaîne de requête pour certains événements, consultez [sélection d’événements](/previous-versions//aa385231(v=vs.85)) et [abonnement à des événements](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="bcf37-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bcf37-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="bcf37-114">Examples</span></span>

<span data-ttu-id="bcf37-115">La chaîne de requête suivante définit un abonnement à tous les événements de niveau 2 dans le canal système :</span><span class="sxs-lookup"><span data-stu-id="bcf37-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="bcf37-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf37-116">Requirements</span></span>



| <span data-ttu-id="bcf37-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcf37-117">Requirement</span></span> | <span data-ttu-id="bcf37-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcf37-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf37-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcf37-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf37-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcf37-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bcf37-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcf37-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf37-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcf37-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bcf37-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bcf37-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcf37-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bcf37-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bcf37-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf37-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf37-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf37-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf37-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf37-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bcf37-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bcf37-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="bcf37-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

