---
description: 'CBaseFilter. pause, méthode : la méthode pause interrompt le filtre. Cette méthode implémente la méthode IMediaFilter ::P ause.'
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: CBaseFilter. pause, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120087"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="339f1-104">CBaseFilter. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="339f1-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="339f1-105">La `Pause` méthode suspend le filtre.</span><span class="sxs-lookup"><span data-stu-id="339f1-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="339f1-106">Cette méthode implémente la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="339f1-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="339f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="339f1-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="339f1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="339f1-108">Parameters</span></span>

<span data-ttu-id="339f1-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="339f1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="339f1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="339f1-110">Return value</span></span>

<span data-ttu-id="339f1-111">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="339f1-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="339f1-112">Notes </span><span class="sxs-lookup"><span data-stu-id="339f1-112">Remarks</span></span>

<span data-ttu-id="339f1-113">Cette méthode appelle la méthode [**CBasePin :: active**](cbasepin-active.md) sur chacune des broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="339f1-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="339f1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="339f1-114">Requirements</span></span>



| <span data-ttu-id="339f1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="339f1-115">Requirement</span></span> | <span data-ttu-id="339f1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="339f1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="339f1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="339f1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="339f1-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="339f1-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="339f1-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="339f1-119">Library</span></span><br/> | <dl> <span data-ttu-id="339f1-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="339f1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="339f1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="339f1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="339f1-122">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="339f1-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




