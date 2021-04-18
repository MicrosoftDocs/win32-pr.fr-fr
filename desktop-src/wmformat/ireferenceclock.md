---
title: Interface IReferenceClock
description: L’interface IReferenceClock fournit l’accès à une horloge externe. Cette interface est fournie pour permettre la synchronisation de toutes les routines de rendu avec la même horloge. Cette interface peut être obtenue à partir d’un objet lecteur.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Format Windows Media de l’interface IReferenceClock
- Interface IReferenceClock format Windows Media, décrit
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511894"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="c1aa7-106">Interface IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="c1aa7-106">IReferenceClock interface</span></span>

<span data-ttu-id="c1aa7-107">L’interface **IReferenceClock** fournit l’accès à une horloge externe.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="c1aa7-108">Cette interface est fournie pour permettre la synchronisation de toutes les routines de rendu avec la même horloge.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="c1aa7-109">Cette interface peut être obtenue à partir d’un objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="c1aa7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c1aa7-110">Members</span></span>

<span data-ttu-id="c1aa7-111">L’interface **IReferenceClock** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c1aa7-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c1aa7-112">**IReferenceClock** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c1aa7-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="c1aa7-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1aa7-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c1aa7-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1aa7-114">Methods</span></span>

<span data-ttu-id="c1aa7-115">L’interface **IReferenceClock** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="c1aa7-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="c1aa7-116">Method</span></span>                                                   | <span data-ttu-id="c1aa7-117">Description</span><span class="sxs-lookup"><span data-stu-id="c1aa7-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="c1aa7-118">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="c1aa7-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="c1aa7-119">Non implémenté par ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c1aa7-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="c1aa7-120">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="c1aa7-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="c1aa7-121">Demande une notification asynchrone qu’une heure s’est écoulée.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="c1aa7-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="c1aa7-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="c1aa7-123">Récupère le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="c1aa7-124">**Arrêter**</span><span class="sxs-lookup"><span data-stu-id="c1aa7-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="c1aa7-125">Annule une demande de notification.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="c1aa7-126">Notes</span><span class="sxs-lookup"><span data-stu-id="c1aa7-126">Remarks</span></span>

<span data-ttu-id="c1aa7-127">Pour plus d’informations sur les autres interfaces qui peuvent être obtenues à l’aide de la méthode QueryInterface de cette interface, consultez objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="c1aa7-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1aa7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1aa7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1aa7-129">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="c1aa7-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 

