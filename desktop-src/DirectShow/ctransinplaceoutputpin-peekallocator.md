---
description: La méthode PeekAllocator retourne un pointeur vers l’allocateur du pin. La méthode n’incrémente pas le nombre de références sur l’interface.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Méthode CTransInPlaceOutputPin. PeekAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523940"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="7b3a6-104">Méthode CTransInPlaceOutputPin. PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="7b3a6-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="7b3a6-105">La `PeekAllocator` méthode retourne un pointeur vers l’allocateur du pin.</span><span class="sxs-lookup"><span data-stu-id="7b3a6-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="7b3a6-106">La méthode n’incrémente pas le nombre de références sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="7b3a6-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b3a6-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="7b3a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b3a6-108">Parameters</span></span>

<span data-ttu-id="7b3a6-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7b3a6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b3a6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b3a6-110">Return value</span></span>

<span data-ttu-id="7b3a6-111">Retourne la variable de membre [**CBaseOutputPin :: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7b3a6-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3a6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b3a6-112">Requirements</span></span>



| <span data-ttu-id="7b3a6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b3a6-113">Requirement</span></span> | <span data-ttu-id="7b3a6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b3a6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3a6-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b3a6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7b3a6-116"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3a6-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b3a6-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b3a6-117">Library</span></span><br/> | <dl> <span data-ttu-id="7b3a6-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3a6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3a6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b3a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3a6-120">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="7b3a6-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




