---
description: Stocke et récupère des informations sur les abonnements aux événements. Cette interface étend l’interface IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interface IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516192"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="df093-104">Interface IEventSubscription2</span><span class="sxs-lookup"><span data-stu-id="df093-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="df093-105">Stocke et récupère des informations sur les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="df093-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="df093-106">Cette interface étend l’interface [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .</span><span class="sxs-lookup"><span data-stu-id="df093-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="df093-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="df093-107">When to implement</span></span>

<span data-ttu-id="df093-108">Vous n’avez pas besoin d’implémenter l’interface **IEventSubscription2** .</span><span class="sxs-lookup"><span data-stu-id="df093-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="df093-109">Une classe d’objet d’événement fournie par le système (CLSID \_ CEventSubscription) implémente **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="df093-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="df093-110">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="df093-110">When to use</span></span>

<span data-ttu-id="df093-111">Le système d' [événements com+](com--events.md) utilise cette interface pour obtenir des informations sur les abonnements individuels.</span><span class="sxs-lookup"><span data-stu-id="df093-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="df093-112">Membres</span><span class="sxs-lookup"><span data-stu-id="df093-112">Members</span></span>

<span data-ttu-id="df093-113">L’interface **IEventSubscription2** hérite de **IEventSubscription**.</span><span class="sxs-lookup"><span data-stu-id="df093-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="df093-114">**IEventSubscription2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df093-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="df093-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df093-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df093-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df093-116">Properties</span></span>

<span data-ttu-id="df093-117">L’interface **IEventSubscription2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="df093-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="df093-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="df093-118">Property</span></span>                                                                      | <span data-ttu-id="df093-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="df093-119">Access type</span></span>           | <span data-ttu-id="df093-120">Description</span><span class="sxs-lookup"><span data-stu-id="df093-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="df093-121">**FilterCriteria**</span><span class="sxs-lookup"><span data-stu-id="df093-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="df093-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="df093-122">Read/write</span></span><br/> | <span data-ttu-id="df093-123">Critères de filtre régissant l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="df093-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="df093-124">**SubscriberMoniker**</span><span class="sxs-lookup"><span data-stu-id="df093-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="df093-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="df093-125">Read/write</span></span><br/> | <span data-ttu-id="df093-126">Moniker de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="df093-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="df093-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df093-127">Requirements</span></span>



| <span data-ttu-id="df093-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df093-128">Requirement</span></span> | <span data-ttu-id="df093-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="df093-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="df093-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df093-130">Minimum supported client</span></span><br/> | <span data-ttu-id="df093-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df093-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="df093-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df093-132">Minimum supported server</span></span><br/> | <span data-ttu-id="df093-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df093-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="df093-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df093-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df093-135">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="df093-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




