---
description: 'La méthode SetSink définit un gestionnaire de qualité externe. Cette méthode implémente la méthode IQualityControl :: SetSink.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Méthode CBasePin. SetSink (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533036"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="967eb-104">Méthode CBasePin. SetSink</span><span class="sxs-lookup"><span data-stu-id="967eb-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="967eb-105">La `SetSink` méthode définit un gestionnaire de qualité externe.</span><span class="sxs-lookup"><span data-stu-id="967eb-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="967eb-106">Cette méthode implémente la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .</span><span class="sxs-lookup"><span data-stu-id="967eb-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="967eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="967eb-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="967eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="967eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967eb-109">*piqc*</span><span class="sxs-lookup"><span data-stu-id="967eb-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="967eb-110">Pointeur vers l’interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) du gestionnaire de qualité.</span><span class="sxs-lookup"><span data-stu-id="967eb-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967eb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="967eb-111">Return value</span></span>

<span data-ttu-id="967eb-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="967eb-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="967eb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="967eb-113">Remarks</span></span>

<span data-ttu-id="967eb-114">Appelez cette méthode pour rediriger les messages de contrôle qualité vers un gestionnaire de qualité externe.</span><span class="sxs-lookup"><span data-stu-id="967eb-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="967eb-115">Pour plus d’informations, consultez [gestion du contrôle qualité](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="967eb-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="967eb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="967eb-116">Requirements</span></span>



| <span data-ttu-id="967eb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="967eb-117">Requirement</span></span> | <span data-ttu-id="967eb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="967eb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="967eb-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="967eb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="967eb-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="967eb-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="967eb-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="967eb-121">Library</span></span><br/> | <dl> <span data-ttu-id="967eb-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="967eb-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967eb-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="967eb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967eb-124">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="967eb-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




