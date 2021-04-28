---
description: 'Méthode CTransInPlaceFilter. GetPin : la méthode GetPin récupère un code confidentiel.'
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
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084767"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="890ef-103">Méthode CTransInPlaceFilter. GetPin</span><span class="sxs-lookup"><span data-stu-id="890ef-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="890ef-104">La `GetPin` méthode récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="890ef-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="890ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="890ef-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="890ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="890ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="890ef-107">*n*</span><span class="sxs-lookup"><span data-stu-id="890ef-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="890ef-108">Numéro du code confidentiel spécifié, indexé à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="890ef-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="890ef-109">Sur ce filtre, la broche 0 est la broche d’entrée et la broche 1 est la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="890ef-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="890ef-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="890ef-110">Return value</span></span>

<span data-ttu-id="890ef-111">Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel, ou **null** si la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="890ef-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="890ef-112">Notes </span><span class="sxs-lookup"><span data-stu-id="890ef-112">Remarks</span></span>

<span data-ttu-id="890ef-113">Cette méthode remplace la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="890ef-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="890ef-114">La première fois que la méthode est appelée, elle crée les deux broches.</span><span class="sxs-lookup"><span data-stu-id="890ef-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="890ef-115">Cette méthode n’incrémente pas le nombre de références sur le pin retourné, donc le code confidentiel retourné n’a pas de nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="890ef-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="890ef-116">Si l’appelant doit conserver une référence sur le code confidentiel, il doit appeler la méthode **IUnknown :: AddRef** sur le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="890ef-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="890ef-117">Si le filtre utilise les codes confidentiels par défaut [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) et [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) , vous n’avez probablement pas besoin de substituer cette méthode.</span><span class="sxs-lookup"><span data-stu-id="890ef-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="890ef-118">Toutefois, si le filtre utilise des codes confidentiels qui étendent ces classes, vous devez substituer cette méthode pour créer des broches de ce type.</span><span class="sxs-lookup"><span data-stu-id="890ef-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="890ef-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="890ef-119">Requirements</span></span>



| <span data-ttu-id="890ef-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="890ef-120">Requirement</span></span> | <span data-ttu-id="890ef-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="890ef-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="890ef-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="890ef-122">Header</span></span><br/>  | <dl> <span data-ttu-id="890ef-123"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="890ef-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="890ef-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="890ef-124">Library</span></span><br/> | <dl> <span data-ttu-id="890ef-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="890ef-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="890ef-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="890ef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="890ef-127">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="890ef-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




