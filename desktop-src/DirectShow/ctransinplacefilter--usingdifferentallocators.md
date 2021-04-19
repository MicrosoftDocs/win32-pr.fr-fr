---
description: La méthode UsingDifferentAllocators détermine si les broches d’entrée et de sortie utilisent des allocateurs différents.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Méthode CTransInPlaceFilter. UsingDifferentAllocators (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537888"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a><span data-ttu-id="bad1b-103">Méthode CTransInPlaceFilter. UsingDifferentAllocators</span><span class="sxs-lookup"><span data-stu-id="bad1b-103">CTransInPlaceFilter.UsingDifferentAllocators method</span></span>

<span data-ttu-id="bad1b-104">La `UsingDifferentAllocators` méthode détermine si les broches d’entrée et de sortie utilisent des allocateurs différents.</span><span class="sxs-lookup"><span data-stu-id="bad1b-104">The `UsingDifferentAllocators` method determines whether the input and output pins are using different allocators.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad1b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bad1b-105">Syntax</span></span>


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a><span data-ttu-id="bad1b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bad1b-106">Parameters</span></span>

<span data-ttu-id="bad1b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bad1b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bad1b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bad1b-108">Return value</span></span>

<span data-ttu-id="bad1b-109">Retourne la **valeur true** si les broches d’entrée et de sortie utilisent différents allocators, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bad1b-109">Returns **TRUE** if the input and output pins are using different allocators, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad1b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bad1b-110">Requirements</span></span>



| <span data-ttu-id="bad1b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bad1b-111">Requirement</span></span> | <span data-ttu-id="bad1b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bad1b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad1b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="bad1b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="bad1b-114"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bad1b-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bad1b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bad1b-115">Library</span></span><br/> | <dl> <span data-ttu-id="bad1b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bad1b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad1b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bad1b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad1b-118">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="bad1b-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




