---
description: La méthode BreakConnect libère le code confidentiel d’une connexion.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Méthode CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542424"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="ec630-103">Méthode CBaseOutputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="ec630-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="ec630-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="ec630-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec630-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec630-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="ec630-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec630-106">Parameters</span></span>

<span data-ttu-id="ec630-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ec630-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec630-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec630-108">Return value</span></span>

<span data-ttu-id="ec630-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ec630-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec630-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ec630-110">Remarks</span></span>

<span data-ttu-id="ec630-111">Cette méthode remplace la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ec630-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="ec630-112">Il annule l’allocation et libère les interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) et [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="ec630-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="ec630-113">Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.</span><span class="sxs-lookup"><span data-stu-id="ec630-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="ec630-114">Dans le cas contraire, vous risquez de provoquer des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ec630-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec630-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec630-115">Requirements</span></span>



| <span data-ttu-id="ec630-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec630-116">Requirement</span></span> | <span data-ttu-id="ec630-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec630-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec630-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec630-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ec630-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec630-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ec630-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec630-120">Library</span></span><br/> | <dl> <span data-ttu-id="ec630-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec630-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec630-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec630-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec630-123">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ec630-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




