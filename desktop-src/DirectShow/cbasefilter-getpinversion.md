---
description: La méthode GetPinVersion récupère un numéro de version pour l’ensemble de broches sur ce filtre.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Méthode CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545607"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="b6a73-103">Méthode CBaseFilter. GetPinVersion</span><span class="sxs-lookup"><span data-stu-id="b6a73-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="b6a73-104">La `GetPinVersion` méthode récupère un numéro de version pour l’ensemble de broches sur ce filtre.</span><span class="sxs-lookup"><span data-stu-id="b6a73-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6a73-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="b6a73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6a73-106">Parameters</span></span>

<span data-ttu-id="b6a73-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6a73-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6a73-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6a73-108">Return value</span></span>

<span data-ttu-id="b6a73-109">Retourne la variable de membre [**CBaseFilter :: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a73-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a73-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b6a73-110">Remarks</span></span>

<span data-ttu-id="b6a73-111">Le constructeur **CBaseFilter** initialise la version du code confidentiel sur 1.</span><span class="sxs-lookup"><span data-stu-id="b6a73-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="b6a73-112">Dans la classe de base, ce nombre ne change jamais.</span><span class="sxs-lookup"><span data-stu-id="b6a73-112">In the base class, this number never changes.</span></span> <span data-ttu-id="b6a73-113">Si le filtre crée ou détruit dynamiquement des épingles, il doit incrémenter la version du code confidentiel chaque fois que les codes confidentiels changent.</span><span class="sxs-lookup"><span data-stu-id="b6a73-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="b6a73-114">Pour incrémenter le numéro de version, appelez la méthode [**CBaseFilter :: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a73-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="b6a73-115">L’objet d’énumérateur de code confidentiel, qui est implémenté par la classe [**CEnumPins**](cenumpins.md) , utilise la version du code confidentiel pour rester synchronisé avec le filtre.</span><span class="sxs-lookup"><span data-stu-id="b6a73-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a73-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6a73-116">Requirements</span></span>



| <span data-ttu-id="b6a73-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6a73-117">Requirement</span></span> | <span data-ttu-id="b6a73-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6a73-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a73-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6a73-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b6a73-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6a73-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b6a73-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6a73-121">Library</span></span><br/> | <dl> <span data-ttu-id="b6a73-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b6a73-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a73-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6a73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a73-124">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="b6a73-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




