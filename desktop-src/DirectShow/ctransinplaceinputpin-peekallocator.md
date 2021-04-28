---
description: 'Méthode CTransInPlaceInputPin. PeekAllocator : la méthode PeekAllocator retourne un pointeur vers l’allocateur du pin. La méthode n’incrémente pas le nombre de références sur l’interface.'
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Méthode CTransInPlaceInputPin. PeekAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084667"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="95a8f-104">Méthode CTransInPlaceInputPin. PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="95a8f-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="95a8f-105">La `PeekAllocator` méthode retourne un pointeur vers l’allocateur du pin.</span><span class="sxs-lookup"><span data-stu-id="95a8f-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="95a8f-106">La méthode n’incrémente pas le nombre de références sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="95a8f-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95a8f-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="95a8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95a8f-108">Parameters</span></span>

<span data-ttu-id="95a8f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="95a8f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95a8f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95a8f-110">Return value</span></span>

<span data-ttu-id="95a8f-111">Retourne la variable de membre [**CBaseInputPin :: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="95a8f-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a8f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95a8f-112">Requirements</span></span>



| <span data-ttu-id="95a8f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95a8f-113">Requirement</span></span> | <span data-ttu-id="95a8f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="95a8f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a8f-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="95a8f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="95a8f-116"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95a8f-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95a8f-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95a8f-117">Library</span></span><br/> | <dl> <span data-ttu-id="95a8f-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95a8f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a8f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95a8f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a8f-120">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="95a8f-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




