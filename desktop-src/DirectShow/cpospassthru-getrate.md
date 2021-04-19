---
description: 'La méthode GetRate récupère la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: GetRate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Méthode CPosPassThru. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530292"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="a24a4-104">Méthode CPosPassThru. GetRate</span><span class="sxs-lookup"><span data-stu-id="a24a4-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="a24a4-105">La `GetRate` méthode récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="a24a4-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="a24a4-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="a24a4-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a24a4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a24a4-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="a24a4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a24a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24a4-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="a24a4-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="a24a4-110">Pointeur vers une variable qui reçoit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="a24a4-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24a4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a24a4-111">Return value</span></span>

<span data-ttu-id="a24a4-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="a24a4-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24a4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a24a4-113">Requirements</span></span>



| <span data-ttu-id="a24a4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a24a4-114">Requirement</span></span> | <span data-ttu-id="a24a4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a24a4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a24a4-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a24a4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a24a4-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a24a4-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a24a4-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a24a4-118">Library</span></span><br/> | <dl> <span data-ttu-id="a24a4-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a24a4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24a4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a24a4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24a4-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="a24a4-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




