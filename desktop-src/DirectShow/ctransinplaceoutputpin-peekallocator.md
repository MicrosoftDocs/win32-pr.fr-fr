---
description: 'Méthode CTransInPlaceOutputPin. PeekAllocator : la méthode PeekAllocator retourne un pointeur vers l’allocateur du pin. La méthode n’incrémente pas le nombre de références sur l’interface.'
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
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084597"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="efbbb-104">Méthode CTransInPlaceOutputPin. PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="efbbb-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="efbbb-105">La `PeekAllocator` méthode retourne un pointeur vers l’allocateur du pin.</span><span class="sxs-lookup"><span data-stu-id="efbbb-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="efbbb-106">La méthode n’incrémente pas le nombre de références sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="efbbb-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbbb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efbbb-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="efbbb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efbbb-108">Parameters</span></span>

<span data-ttu-id="efbbb-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="efbbb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="efbbb-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="efbbb-110">Return value</span></span>

<span data-ttu-id="efbbb-111">Retourne la variable de membre [**CBaseOutputPin :: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="efbbb-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbbb-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efbbb-112">Requirements</span></span>



| <span data-ttu-id="efbbb-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efbbb-113">Requirement</span></span> | <span data-ttu-id="efbbb-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="efbbb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbbb-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="efbbb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="efbbb-116"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efbbb-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="efbbb-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="efbbb-117">Library</span></span><br/> | <dl> <span data-ttu-id="efbbb-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="efbbb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbbb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efbbb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbbb-120">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="efbbb-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




