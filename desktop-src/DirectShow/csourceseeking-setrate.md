---
description: 'La méthode sechaque définit la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: se.'
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
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532647"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="2039b-104">CSourceSeeking. se, méthode</span><span class="sxs-lookup"><span data-stu-id="2039b-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="2039b-105">La `SetRate` méthode définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="2039b-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="2039b-106">Cette méthode implémente la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se.</span><span class="sxs-lookup"><span data-stu-id="2039b-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2039b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2039b-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="2039b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2039b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2039b-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="2039b-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="2039b-110">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="2039b-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2039b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2039b-111">Return value</span></span>

<span data-ttu-id="2039b-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2039b-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2039b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2039b-113">Remarks</span></span>

<span data-ttu-id="2039b-114">Cette méthode met à jour la valeur de la variable membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , puis appelle la méthode virtuelle pure [**CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="2039b-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="2039b-115">La méthode ne valide pas le paramètre *dRate* .</span><span class="sxs-lookup"><span data-stu-id="2039b-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2039b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2039b-116">Requirements</span></span>



| <span data-ttu-id="2039b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2039b-117">Requirement</span></span> | <span data-ttu-id="2039b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2039b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2039b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2039b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2039b-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2039b-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2039b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2039b-121">Library</span></span><br/> | <dl> <span data-ttu-id="2039b-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2039b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2039b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2039b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2039b-124">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="2039b-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




