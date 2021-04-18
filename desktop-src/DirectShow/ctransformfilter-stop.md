---
description: 'Arrête le filtre. Cette méthode implémente la méthode IMediaFilter :: Stop.'
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: CTransformFilter. Stop, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543283"
---
# <a name="ctransformfilterstop-method"></a><span data-ttu-id="6de5e-104">CTransformFilter. Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="6de5e-104">CTransformFilter.Stop method</span></span>

<span data-ttu-id="6de5e-105">Arrête le filtre.</span><span class="sxs-lookup"><span data-stu-id="6de5e-105">Stops the filter.</span></span> <span data-ttu-id="6de5e-106">Cette méthode implémente la méthode [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="6de5e-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de5e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6de5e-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="6de5e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6de5e-108">Parameters</span></span>

<span data-ttu-id="6de5e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6de5e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6de5e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6de5e-110">Return value</span></span>

<span data-ttu-id="6de5e-111">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6de5e-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6de5e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6de5e-112">Remarks</span></span>

<span data-ttu-id="6de5e-113">Une fois que cette méthode a désvalidé les deux allocateurs, elle appelle la méthode [**StopStreaming**](ctransformfilter-stopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="6de5e-113">After this method decommits both allocators, it calls the [**StopStreaming**](ctransformfilter-stopstreaming.md) method.</span></span> <span data-ttu-id="6de5e-114">La méthode **StopStreaming** n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="6de5e-114">The **StopStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de5e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6de5e-115">Requirements</span></span>



| <span data-ttu-id="6de5e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6de5e-116">Requirement</span></span> | <span data-ttu-id="6de5e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6de5e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de5e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="6de5e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6de5e-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6de5e-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6de5e-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6de5e-120">Library</span></span><br/> | <dl> <span data-ttu-id="6de5e-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6de5e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de5e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6de5e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de5e-123">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="6de5e-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




