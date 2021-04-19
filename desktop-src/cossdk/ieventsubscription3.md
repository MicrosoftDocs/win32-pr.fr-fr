---
description: Stocke et récupère des informations sur les abonnements aux événements. Cette interface étend l’interface IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interface IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513156"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="a2da4-104">Interface IEventSubscription3</span><span class="sxs-lookup"><span data-stu-id="a2da4-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="a2da4-105">Stocke et récupère des informations sur les abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="a2da4-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="a2da4-106">Cette interface étend l’interface [**IEventSubscription2**](ieventsubscription2.md) .</span><span class="sxs-lookup"><span data-stu-id="a2da4-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a2da4-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="a2da4-107">When to implement</span></span>

<span data-ttu-id="a2da4-108">Vous n’avez pas besoin d’implémenter l’interface **IEventSubscription3** .</span><span class="sxs-lookup"><span data-stu-id="a2da4-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="a2da4-109">Une classe d’objet d’événement fournie par le système (CLSID \_ CEventSubscription) implémente **IEventSubscription3**.</span><span class="sxs-lookup"><span data-stu-id="a2da4-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a2da4-110">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="a2da4-110">When to use</span></span>

<span data-ttu-id="a2da4-111">Le système d' [événements com+](com--events.md) utilise cette interface pour obtenir des informations sur les abonnements individuels.</span><span class="sxs-lookup"><span data-stu-id="a2da4-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="a2da4-112">Membres</span><span class="sxs-lookup"><span data-stu-id="a2da4-112">Members</span></span>

<span data-ttu-id="a2da4-113">L’interface **IEventSubscription3** hérite de **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="a2da4-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="a2da4-114">**IEventSubscription3** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2da4-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="a2da4-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2da4-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2da4-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2da4-116">Properties</span></span>

<span data-ttu-id="a2da4-117">L’interface **IEventSubscription3** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2da4-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="a2da4-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="a2da4-118">Property</span></span>                                                                                  | <span data-ttu-id="a2da4-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a2da4-119">Access type</span></span>           | <span data-ttu-id="a2da4-120">Description</span><span class="sxs-lookup"><span data-stu-id="a2da4-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="a2da4-121">**EventClassApplicationID**</span><span class="sxs-lookup"><span data-stu-id="a2da4-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="a2da4-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a2da4-122">Read/write</span></span><br/> | <span data-ttu-id="a2da4-123">GUID de l’application de l’objet de classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="a2da4-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="a2da4-124">**EventClassPartitionID**</span><span class="sxs-lookup"><span data-stu-id="a2da4-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="a2da4-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a2da4-125">Read/write</span></span><br/> | <span data-ttu-id="a2da4-126">GUID de la partition de l’objet de classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="a2da4-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="a2da4-127">**SubscriberApplicationID**</span><span class="sxs-lookup"><span data-stu-id="a2da4-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="a2da4-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a2da4-128">Read/write</span></span><br/> | <span data-ttu-id="a2da4-129">GUID de l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="a2da4-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="a2da4-130">**SubscriberPartitionID**</span><span class="sxs-lookup"><span data-stu-id="a2da4-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="a2da4-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a2da4-131">Read/write</span></span><br/> | <span data-ttu-id="a2da4-132">GUID de la partition de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="a2da4-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="a2da4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2da4-133">Requirements</span></span>



| <span data-ttu-id="a2da4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2da4-134">Requirement</span></span> | <span data-ttu-id="a2da4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2da4-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a2da4-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2da4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a2da4-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2da4-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a2da4-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2da4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a2da4-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2da4-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a2da4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2da4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2da4-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="a2da4-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




