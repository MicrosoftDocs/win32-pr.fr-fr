---
description: La méthode IncrementTypeVersion incrémente le numéro de version sur le jeu de types de médias préférés.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Méthode CBasePin. IncrementTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529001"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="a8ac3-103">Méthode CBasePin. IncrementTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a8ac3-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="a8ac3-104">La `IncrementTypeVersion` méthode incrémente le numéro de version sur le jeu de types de médias préférés.</span><span class="sxs-lookup"><span data-stu-id="a8ac3-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ac3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8ac3-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="a8ac3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8ac3-106">Parameters</span></span>

<span data-ttu-id="a8ac3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a8ac3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8ac3-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8ac3-108">Return value</span></span>

<span data-ttu-id="a8ac3-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a8ac3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ac3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a8ac3-110">Remarks</span></span>

<span data-ttu-id="a8ac3-111">Cette méthode incrémente la variable membre [**CBasePin :: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ac3-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="a8ac3-112">Si le code PIN modifie dynamiquement la liste des types de média préférés, appelez cette méthode chaque fois que la liste change.</span><span class="sxs-lookup"><span data-stu-id="a8ac3-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="a8ac3-113">Pour plus d’informations, consultez [**CBasePin :: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span><span class="sxs-lookup"><span data-stu-id="a8ac3-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ac3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8ac3-114">Requirements</span></span>



| <span data-ttu-id="a8ac3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8ac3-115">Requirement</span></span> | <span data-ttu-id="a8ac3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8ac3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ac3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8ac3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a8ac3-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8ac3-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a8ac3-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8ac3-119">Library</span></span><br/> | <dl> <span data-ttu-id="a8ac3-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a8ac3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ac3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8ac3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ac3-122">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="a8ac3-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




