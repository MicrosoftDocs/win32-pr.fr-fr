---
description: 'Méthode CTransInPlaceFilter. CompleteConnect : la méthode CompleteConnect termine une connexion de code confidentiel.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Méthode CTransInPlaceFilter. CompleteConnect (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084787"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a><span data-ttu-id="51b49-103">Méthode CTransInPlaceFilter. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="51b49-103">CTransInPlaceFilter.CompleteConnect method</span></span>

<span data-ttu-id="51b49-104">La `CompleteConnect` méthode termine une connexion de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="51b49-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b49-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51b49-105">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="51b49-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51b49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51b49-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="51b49-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="51b49-108">Membre du type énuméré dans la [**\_ direction du code confidentiel**](/windows/win32/api/strmif/ne-strmif-pin_direction) , en spécifiant quelle broche du filtre effectue la connexion.</span><span class="sxs-lookup"><span data-stu-id="51b49-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="51b49-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="51b49-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="51b49-110">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de l’autre code confidentiel dans cette tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="51b49-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51b49-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51b49-111">Return value</span></span>

<span data-ttu-id="51b49-112">Retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="51b49-112">Returns an **HRESULT**.</span></span> <span data-ttu-id="51b49-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="51b49-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="51b49-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="51b49-114">Return code</span></span>                                                                                           | <span data-ttu-id="51b49-115">Description</span><span class="sxs-lookup"><span data-stu-id="51b49-115">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="51b49-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51b49-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="51b49-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="51b49-117">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="51b49-118"><dt>**VFW \_ E \_ pas \_ dans le \_ graphique**</dt></span><span class="sxs-lookup"><span data-stu-id="51b49-118"><dt>**VFW\_E\_NOT\_IN\_GRAPH**</dt></span></span> </dl> | <span data-ttu-id="51b49-119">Le filtre n’est pas dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="51b49-119">The filter is not in a filter graph.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51b49-120">Notes </span><span class="sxs-lookup"><span data-stu-id="51b49-120">Remarks</span></span>

<span data-ttu-id="51b49-121">Cette méthode remplace la méthode [**CTransformFilter :: CompleteConnect**](ctransformfilter-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="51b49-121">This method overrides the [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) method.</span></span>

<span data-ttu-id="51b49-122">Le comportement du filtre dépend de l’ordre des connexions de code confidentiel :</span><span class="sxs-lookup"><span data-stu-id="51b49-122">The behavior of the filter depends on the order of the pin connections:</span></span>

-   <span data-ttu-id="51b49-123">Si la broche d’entrée est connectée en premier, la connexion utilise un allocateur temporaire.</span><span class="sxs-lookup"><span data-stu-id="51b49-123">If the input pin is connected first, the connection uses a temporary allocator.</span></span> <span data-ttu-id="51b49-124">Lorsque la broche de sortie est connectée, le filtre reconnecte la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="51b49-124">When the output pin is connected, the filter reconnects the input pin.</span></span> <span data-ttu-id="51b49-125">Si vous reconnectez la broche d’entrée, le filtre en amont renégocie l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="51b49-125">Reconnecting the input pin causes the upstream filter to renegotiate the allocator.</span></span> <span data-ttu-id="51b49-126">À ce stade, la broche d’entrée propose un allocateur à partir du filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="51b49-126">At that point, the input pin proposes an allocator from the downstream filter.</span></span> <span data-ttu-id="51b49-127">Pour plus d’informations, consultez [**CTransInPlaceInputPin :: GetAllocator**](ctransinplaceinputpin-getallocator.md).</span><span class="sxs-lookup"><span data-stu-id="51b49-127">For more information, see [**CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).</span></span>
-   <span data-ttu-id="51b49-128">Si la broche de sortie est connectée en premier, la broche de sortie ne sélectionne pas d’allocateur.</span><span class="sxs-lookup"><span data-stu-id="51b49-128">If the output pin is connected first, the output pin does not select an allocator.</span></span> <span data-ttu-id="51b49-129">Lorsque la broche d’entrée est connectée, elle négocie un allocateur pour les deux connexions.</span><span class="sxs-lookup"><span data-stu-id="51b49-129">When the input pin is connected, it negotiates an allocator for both connections.</span></span> <span data-ttu-id="51b49-130">Si les types de média d’entrée et de sortie ne sont pas identiques, le filtre reconnecte la broche de sortie à l’aide du type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="51b49-130">If the input and output media types are not the same, the filter reconnects the output pin using the input type.</span></span>

<span data-ttu-id="51b49-131">Le filtre effectue toutes les reconnexions de code confidentiel en appelant la méthode [**CBaseFilter :: ReconnectPin**](cbasefilter-reconnectpin.md) .</span><span class="sxs-lookup"><span data-stu-id="51b49-131">The filter performs all pin reconnections by calling the [**CBaseFilter::ReconnectPin**](cbasefilter-reconnectpin.md) method.</span></span> <span data-ttu-id="51b49-132">La méthode **ReconnectPin** appelle à son tour la méthode [**IFilterGraph2 :: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="51b49-132">The **ReconnectPin** method, in turn, calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b49-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51b49-133">Requirements</span></span>



| <span data-ttu-id="51b49-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51b49-134">Requirement</span></span> | <span data-ttu-id="51b49-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="51b49-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51b49-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="51b49-136">Header</span></span><br/>  | <dl> <span data-ttu-id="51b49-137"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51b49-137"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="51b49-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51b49-138">Library</span></span><br/> | <dl> <span data-ttu-id="51b49-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51b49-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b49-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51b49-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b49-141">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="51b49-141">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




