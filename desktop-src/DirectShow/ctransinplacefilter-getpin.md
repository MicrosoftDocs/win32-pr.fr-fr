---
description: La méthode GetPin récupère un code confidentiel.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Méthode CTransInPlaceFilter. GetPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae93b663af5427bc61367ae03a3abd6790b8634a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533169"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="5b1ec-103">Méthode CTransInPlaceFilter. GetPin</span><span class="sxs-lookup"><span data-stu-id="5b1ec-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="5b1ec-104">La `GetPin` méthode récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b1ec-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="5b1ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b1ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1ec-107">*n*</span><span class="sxs-lookup"><span data-stu-id="5b1ec-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="5b1ec-108">Numéro du code confidentiel spécifié, indexé à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="5b1ec-109">Sur ce filtre, la broche 0 est la broche d’entrée et la broche 1 est la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1ec-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b1ec-110">Return value</span></span>

<span data-ttu-id="5b1ec-111">Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel, ou **null** si la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b1ec-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5b1ec-112">Remarks</span></span>

<span data-ttu-id="5b1ec-113">Cette méthode remplace la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="5b1ec-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="5b1ec-114">La première fois que la méthode est appelée, elle crée les deux broches.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="5b1ec-115">Cette méthode n’incrémente pas le nombre de références sur le pin retourné, donc le code confidentiel retourné n’a pas de nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="5b1ec-116">Si l’appelant doit conserver une référence sur le code confidentiel, il doit appeler la méthode **IUnknown :: AddRef** sur le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="5b1ec-117">Si le filtre utilise les codes confidentiels par défaut [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) et [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) , vous n’avez probablement pas besoin de substituer cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="5b1ec-118">Toutefois, si le filtre utilise des codes confidentiels qui étendent ces classes, vous devez substituer cette méthode pour créer des broches de ce type.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1ec-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b1ec-119">Requirements</span></span>



| <span data-ttu-id="5b1ec-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b1ec-120">Requirement</span></span> | <span data-ttu-id="5b1ec-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b1ec-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1ec-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b1ec-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5b1ec-123"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b1ec-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b1ec-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5b1ec-124">Library</span></span><br/> | <dl> <span data-ttu-id="5b1ec-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5b1ec-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b1ec-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b1ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1ec-127">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="5b1ec-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




