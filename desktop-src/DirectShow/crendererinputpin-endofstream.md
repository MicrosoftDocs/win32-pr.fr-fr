---
description: 'La méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode remplace la méthode CBasePin :: EndOfStream.'
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Méthode CRendererInputPin. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537899"
---
# <a name="crendererinputpinendofstream-method"></a><span data-ttu-id="22155-104">Méthode CRendererInputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="22155-104">CRendererInputPin.EndOfStream method</span></span>

<span data-ttu-id="22155-105">La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="22155-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="22155-106">Cette méthode remplace la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="22155-106">This method overrides the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22155-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22155-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="22155-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22155-108">Parameters</span></span>

<span data-ttu-id="22155-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="22155-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22155-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22155-110">Return value</span></span>

<span data-ttu-id="22155-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22155-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="22155-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22155-112">Requirements</span></span>



| <span data-ttu-id="22155-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22155-113">Requirement</span></span> | <span data-ttu-id="22155-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="22155-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22155-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="22155-115">Header</span></span><br/>  | <dl> <span data-ttu-id="22155-116"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22155-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22155-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22155-117">Library</span></span><br/> | <dl> <span data-ttu-id="22155-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="22155-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22155-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22155-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22155-120">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="22155-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




