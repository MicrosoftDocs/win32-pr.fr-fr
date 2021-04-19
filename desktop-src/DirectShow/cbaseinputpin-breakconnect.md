---
description: La méthode BreakConnect libère le code confidentiel d’une connexion.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Méthode CBaseInputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6981ef97b98cc25b1996f1599d6d66b8e7d41f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541110"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="c2d1e-103">Méthode CBaseInputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="c2d1e-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="c2d1e-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="c2d1e-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d1e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2d1e-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="c2d1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2d1e-106">Parameters</span></span>

<span data-ttu-id="c2d1e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c2d1e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2d1e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2d1e-108">Return value</span></span>

<span data-ttu-id="c2d1e-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c2d1e-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2d1e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c2d1e-110">Remarks</span></span>

<span data-ttu-id="c2d1e-111">Cette méthode remplace la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d1e-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="c2d1e-112">Il annule l’allocation et libère l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="c2d1e-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="c2d1e-113">Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.</span><span class="sxs-lookup"><span data-stu-id="c2d1e-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="c2d1e-114">Dans le cas contraire, vous risquez de provoquer des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c2d1e-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2d1e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2d1e-115">Requirements</span></span>



| <span data-ttu-id="c2d1e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2d1e-116">Requirement</span></span> | <span data-ttu-id="c2d1e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2d1e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2d1e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2d1e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c2d1e-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2d1e-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2d1e-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2d1e-120">Library</span></span><br/> | <dl> <span data-ttu-id="c2d1e-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2d1e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2d1e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2d1e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d1e-123">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="c2d1e-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




