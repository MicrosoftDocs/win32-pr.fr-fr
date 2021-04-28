---
description: 'Méthode CSourceSeeking. ses : la méthode seplaces définit la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: se.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Méthode CSourceSeeking. se, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098737"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="ff34a-104">CSourceSeeking. se, méthode</span><span class="sxs-lookup"><span data-stu-id="ff34a-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="ff34a-105">La `SetRate` méthode définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="ff34a-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="ff34a-106">Cette méthode implémente la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se.</span><span class="sxs-lookup"><span data-stu-id="ff34a-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff34a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff34a-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="ff34a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff34a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff34a-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="ff34a-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ff34a-110">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="ff34a-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff34a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff34a-111">Return value</span></span>

<span data-ttu-id="ff34a-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff34a-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff34a-113">Notes </span><span class="sxs-lookup"><span data-stu-id="ff34a-113">Remarks</span></span>

<span data-ttu-id="ff34a-114">Cette méthode met à jour la valeur de la variable membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , puis appelle la méthode virtuelle pure [**CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="ff34a-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="ff34a-115">La méthode ne valide pas le paramètre *dRate* .</span><span class="sxs-lookup"><span data-stu-id="ff34a-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff34a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff34a-116">Requirements</span></span>



| <span data-ttu-id="ff34a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff34a-117">Requirement</span></span> | <span data-ttu-id="ff34a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff34a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff34a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff34a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ff34a-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff34a-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff34a-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff34a-121">Library</span></span><br/> | <dl> <span data-ttu-id="ff34a-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ff34a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff34a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff34a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff34a-124">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="ff34a-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




