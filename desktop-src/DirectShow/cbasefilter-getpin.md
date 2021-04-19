---
description: La méthode GetPin récupère un code confidentiel. La classe CEnumPins appelle cette méthode pour énumérer les codes confidentiels sur le filtre.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Méthode CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541152"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="f1854-104">Méthode CBaseFilter. GetPin</span><span class="sxs-lookup"><span data-stu-id="f1854-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="f1854-105">La méthode **GetPin** récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f1854-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="f1854-106">La classe [**CEnumPins**](cenumpins.md) appelle cette méthode pour énumérer les codes confidentiels sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="f1854-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1854-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1854-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f1854-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1854-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1854-109">*n*</span><span class="sxs-lookup"><span data-stu-id="f1854-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="f1854-110">Index de base zéro du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f1854-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1854-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1854-111">Return value</span></span>

<span data-ttu-id="f1854-112">Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f1854-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1854-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f1854-113">Remarks</span></span>

<span data-ttu-id="f1854-114">Vous devez implémenter cette méthode virtuelle pure dans votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="f1854-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="f1854-115">Retourne un pointeur vers le *n* ième pin sur ce filtre, indexé à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="f1854-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="f1854-116">Vous pouvez choisir un ordre d’indexation arbitraire, à condition que l’ordre soit fixe.</span><span class="sxs-lookup"><span data-stu-id="f1854-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="f1854-117">Si le filtre ajoute ou supprime des broches, ou si le classement change pour une autre raison au moment de l’exécution, appelez la méthode [**CBaseFilter :: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="f1854-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1854-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1854-118">Requirements</span></span>



| <span data-ttu-id="f1854-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1854-119">Requirement</span></span> | <span data-ttu-id="f1854-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1854-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1854-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1854-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f1854-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1854-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1854-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1854-123">Library</span></span><br/> | <dl> <span data-ttu-id="f1854-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f1854-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1854-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1854-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1854-126">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f1854-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




