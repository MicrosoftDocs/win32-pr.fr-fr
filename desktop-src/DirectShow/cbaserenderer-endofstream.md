---
description: La méthode EndOfStream avertit le filtre que la broche d’entrée a reçu une notification de fin de flux.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Méthode CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530566"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="8365c-103">Méthode CBaseRenderer. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="8365c-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="8365c-104">La `EndOfStream` méthode notifie le filtre que la broche d’entrée a reçu une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="8365c-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="8365c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8365c-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="8365c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8365c-106">Parameters</span></span>

<span data-ttu-id="8365c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8365c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8365c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8365c-108">Return value</span></span>

<span data-ttu-id="8365c-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8365c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8365c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8365c-110">Remarks</span></span>

<span data-ttu-id="8365c-111">La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit une notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="8365c-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="8365c-112">Cette méthode affecte à l’indicateur [**CBaseRenderer :: m \_ BeOS**](cbaserenderer-m-beos.md) la **valeur true** et appelle la méthode [**CBaseRenderer :: SendEndOfStream**](cbaserenderer-sendendofstream.md) pour planifier un événement [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="8365c-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="8365c-113">Si le filtre est suspendu et en attente d’un exemple, cette méthode termine la transition d’État.</span><span class="sxs-lookup"><span data-stu-id="8365c-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="8365c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8365c-114">Requirements</span></span>



| <span data-ttu-id="8365c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8365c-115">Requirement</span></span> | <span data-ttu-id="8365c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8365c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8365c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="8365c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8365c-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8365c-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8365c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8365c-119">Library</span></span><br/> | <dl> <span data-ttu-id="8365c-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8365c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8365c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8365c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8365c-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="8365c-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




