---
description: La méthode pStateLock récupère un pointeur vers l’objet de section critique du filtre.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Méthode CSource. pStateLock (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532731"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="c64a7-103">Méthode CSource. pStateLock</span><span class="sxs-lookup"><span data-stu-id="c64a7-103">CSource.pStateLock method</span></span>

<span data-ttu-id="c64a7-104">La méthode **pStateLock** récupère un pointeur vers l’objet de section critique du filtre.</span><span class="sxs-lookup"><span data-stu-id="c64a7-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="c64a7-105">Bien qu’elle soit nommée comme une variable membre, **pStateLock** est une méthode.</span><span class="sxs-lookup"><span data-stu-id="c64a7-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c64a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c64a7-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="c64a7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c64a7-107">Parameters</span></span>

<span data-ttu-id="c64a7-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c64a7-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c64a7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c64a7-109">Return value</span></span>

<span data-ttu-id="c64a7-110">Retourne un pointeur vers la variable membre [**CSource :: m \_ cStateLock**](csource-m-cstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="c64a7-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c64a7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c64a7-111">Requirements</span></span>



| <span data-ttu-id="c64a7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c64a7-112">Requirement</span></span> | <span data-ttu-id="c64a7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c64a7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c64a7-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="c64a7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c64a7-115"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c64a7-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c64a7-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c64a7-116">Library</span></span><br/> | <dl> <span data-ttu-id="c64a7-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c64a7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c64a7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c64a7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c64a7-119">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="c64a7-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




