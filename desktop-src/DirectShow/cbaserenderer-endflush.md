---
description: La méthode EndFlush termine une opération de vidage.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Méthode CBaseRenderer. EndFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524064"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="32082-103">Méthode CBaseRenderer. EndFlush</span><span class="sxs-lookup"><span data-stu-id="32082-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="32082-104">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="32082-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="32082-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32082-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="32082-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32082-106">Parameters</span></span>

<span data-ttu-id="32082-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="32082-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32082-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32082-108">Return value</span></span>

<span data-ttu-id="32082-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32082-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="32082-110">Notes</span><span class="sxs-lookup"><span data-stu-id="32082-110">Remarks</span></span>

<span data-ttu-id="32082-111">La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un appel à la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="32082-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32082-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32082-112">Requirements</span></span>



| <span data-ttu-id="32082-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32082-113">Requirement</span></span> | <span data-ttu-id="32082-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="32082-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32082-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="32082-115">Header</span></span><br/>  | <dl> <span data-ttu-id="32082-116"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32082-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="32082-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32082-117">Library</span></span><br/> | <dl> <span data-ttu-id="32082-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="32082-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32082-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32082-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32082-120">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="32082-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




