---
description: 'La méthode AlterQuality avertit le filtre qu’une modification de qualité est demandée. Cette méthode remplace la méthode CTransformFilter :: AlterQuality.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Méthode CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537317"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="505fb-104">Méthode CVideoTransformFilter. AlterQuality</span><span class="sxs-lookup"><span data-stu-id="505fb-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="505fb-105">La `AlterQuality` méthode notifie le filtre qu’une modification de qualité est demandée.</span><span class="sxs-lookup"><span data-stu-id="505fb-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="505fb-106">Cette méthode remplace la méthode [**CTransformFilter :: AlterQuality**](ctransformfilter-alterquality.md) .</span><span class="sxs-lookup"><span data-stu-id="505fb-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="505fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="505fb-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="505fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="505fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="505fb-109">*question*</span><span class="sxs-lookup"><span data-stu-id="505fb-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="505fb-110">Structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) qui contient le message de contrôle qualité.</span><span class="sxs-lookup"><span data-stu-id="505fb-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="505fb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="505fb-111">Return value</span></span>

<span data-ttu-id="505fb-112">Retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="505fb-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="505fb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="505fb-113">Remarks</span></span>

<span data-ttu-id="505fb-114">Cette méthode est appelée lorsque la broche de sortie reçoit un message de qualité (par le biais de la méthode [**IQualityControl :: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).</span><span class="sxs-lookup"><span data-stu-id="505fb-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="505fb-115">La valeur de fin de *q* est stockée dans la variable de membre **m \_ itrLate** .</span><span class="sxs-lookup"><span data-stu-id="505fb-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="505fb-116">La valeur de retour de E \_ Fail indique que le convertisseur doit rattraper le problème en supprimant des frames, bien que la classe **CVideoTransformFilter** dépose également des frames dans les conditions appropriées.</span><span class="sxs-lookup"><span data-stu-id="505fb-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="505fb-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="505fb-117">Requirements</span></span>



| <span data-ttu-id="505fb-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="505fb-118">Requirement</span></span> | <span data-ttu-id="505fb-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="505fb-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="505fb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="505fb-120">Header</span></span><br/>  | <dl> <span data-ttu-id="505fb-121"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="505fb-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="505fb-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="505fb-122">Library</span></span><br/> | <dl> <span data-ttu-id="505fb-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="505fb-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="505fb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="505fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="505fb-125">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="505fb-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="505fb-126">**CVideoTransformFilter::ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="505fb-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




