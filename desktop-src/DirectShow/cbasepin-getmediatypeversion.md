---
description: La méthode GetMediaTypeVersion récupère un numéro de version pour l’ensemble de types de médias préférés.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Méthode CBasePin. GetMediaTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542789"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="1a00f-103">Méthode CBasePin. GetMediaTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1a00f-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="1a00f-104">La `GetMediaTypeVersion` méthode récupère un numéro de version pour l’ensemble de types de médias préférés.</span><span class="sxs-lookup"><span data-stu-id="1a00f-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a00f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a00f-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="1a00f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a00f-106">Parameters</span></span>

<span data-ttu-id="1a00f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1a00f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a00f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a00f-108">Return value</span></span>

<span data-ttu-id="1a00f-109">Retourne la variable de membre [**CBasePin :: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1a00f-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a00f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1a00f-110">Remarks</span></span>

<span data-ttu-id="1a00f-111">Le constructeur **CBasePin** Initialise le numéro de version à 1.</span><span class="sxs-lookup"><span data-stu-id="1a00f-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="1a00f-112">Dans la classe de base, ce nombre ne change jamais.</span><span class="sxs-lookup"><span data-stu-id="1a00f-112">In the base class, this number never changes.</span></span> <span data-ttu-id="1a00f-113">Si le code PIN change dynamiquement sa liste de types de média préférés, il doit incrémenter le numéro de version chaque fois que la liste change.</span><span class="sxs-lookup"><span data-stu-id="1a00f-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="1a00f-114">Pour incrémenter le numéro de version, appelez la méthode [**CBasePin :: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1a00f-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="1a00f-115">L’énumérateur de type de média, qui est implémenté par la classe [**CEnumMediaTypes**](cenummediatypes.md) , utilise le numéro de version pour rester synchronisé avec le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="1a00f-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a00f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a00f-116">Requirements</span></span>



| <span data-ttu-id="1a00f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a00f-117">Requirement</span></span> | <span data-ttu-id="1a00f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a00f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a00f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a00f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1a00f-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a00f-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a00f-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a00f-121">Library</span></span><br/> | <dl> <span data-ttu-id="1a00f-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a00f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a00f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a00f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a00f-124">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="1a00f-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




