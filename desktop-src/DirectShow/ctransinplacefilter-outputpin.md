---
description: La méthode OutputPin récupère un pointeur vers la broche de sortie du filtre.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Méthode CTransInPlaceFilter. OutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532869"
---
# <a name="ctransinplacefilteroutputpin-method"></a><span data-ttu-id="67cfe-103">Méthode CTransInPlaceFilter. OutputPin</span><span class="sxs-lookup"><span data-stu-id="67cfe-103">CTransInPlaceFilter.OutputPin method</span></span>

<span data-ttu-id="67cfe-104">La `OutputPin` méthode récupère un pointeur vers la broche de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="67cfe-104">The `OutputPin` method retrieves a pointer to the filter's output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="67cfe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67cfe-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a><span data-ttu-id="67cfe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67cfe-106">Parameters</span></span>

<span data-ttu-id="67cfe-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="67cfe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67cfe-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67cfe-108">Return value</span></span>

<span data-ttu-id="67cfe-109">Retourne la variable de membre [**CTransformFilter :: m \_ pOutput**](ctransformfilter-m-poutput.md) .</span><span class="sxs-lookup"><span data-stu-id="67cfe-109">Returns the [**CTransformFilter::m\_pOutput**](ctransformfilter-m-poutput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="67cfe-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67cfe-110">Requirements</span></span>



| <span data-ttu-id="67cfe-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67cfe-111">Requirement</span></span> | <span data-ttu-id="67cfe-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="67cfe-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67cfe-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="67cfe-113">Header</span></span><br/>  | <dl> <span data-ttu-id="67cfe-114"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67cfe-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67cfe-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67cfe-115">Library</span></span><br/> | <dl> <span data-ttu-id="67cfe-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="67cfe-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67cfe-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67cfe-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cfe-118">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="67cfe-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




