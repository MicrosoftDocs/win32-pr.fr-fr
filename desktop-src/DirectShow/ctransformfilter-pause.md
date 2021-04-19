---
description: La méthode pause interrompt le filtre. Cette méthode implémente la méthode IMediaFilter ::P ause.
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: CTransformFilter. pause, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5408b9a39f92fd68eacb83474a18da0acda6b961
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525580"
---
# <a name="ctransformfilterpause-method"></a><span data-ttu-id="f99d3-104">CTransformFilter. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="f99d3-104">CTransformFilter.Pause method</span></span>

<span data-ttu-id="f99d3-105">La `Pause` méthode suspend le filtre.</span><span class="sxs-lookup"><span data-stu-id="f99d3-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="f99d3-106">Cette méthode implémente la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="f99d3-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f99d3-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="f99d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f99d3-108">Parameters</span></span>

<span data-ttu-id="f99d3-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f99d3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f99d3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f99d3-110">Return value</span></span>

<span data-ttu-id="f99d3-111">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f99d3-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f99d3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f99d3-112">Remarks</span></span>

<span data-ttu-id="f99d3-113">Cette méthode appelle la méthode [**StartStreaming**](ctransformfilter-startstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="f99d3-113">This method calls the [**StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span> <span data-ttu-id="f99d3-114">La méthode **StartStreaming** n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="f99d3-114">The **StartStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f99d3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f99d3-115">Requirements</span></span>



| <span data-ttu-id="f99d3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f99d3-116">Requirement</span></span> | <span data-ttu-id="f99d3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f99d3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99d3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f99d3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f99d3-119"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f99d3-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f99d3-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f99d3-120">Library</span></span><br/> | <dl> <span data-ttu-id="f99d3-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f99d3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f99d3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f99d3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99d3-123">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f99d3-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




