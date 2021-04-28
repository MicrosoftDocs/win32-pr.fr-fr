---
description: 'Méthode CBaseInputPin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
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
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099737"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="d37a9-103">Méthode CBaseInputPin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="d37a9-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="d37a9-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="d37a9-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d37a9-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="d37a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d37a9-106">Parameters</span></span>

<span data-ttu-id="d37a9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d37a9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d37a9-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d37a9-108">Return value</span></span>

<span data-ttu-id="d37a9-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d37a9-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d37a9-110">Notes </span><span class="sxs-lookup"><span data-stu-id="d37a9-110">Remarks</span></span>

<span data-ttu-id="d37a9-111">Cette méthode remplace la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="d37a9-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="d37a9-112">Il annule l’allocation et libère l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="d37a9-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="d37a9-113">Si vous substituez cette méthode, appelez la méthode de la classe de base à partir de votre méthode de substitution.</span><span class="sxs-lookup"><span data-stu-id="d37a9-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="d37a9-114">Dans le cas contraire, vous risquez de provoquer des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d37a9-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="d37a9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d37a9-115">Requirements</span></span>



| <span data-ttu-id="d37a9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d37a9-116">Requirement</span></span> | <span data-ttu-id="d37a9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d37a9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d37a9-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d37a9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d37a9-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d37a9-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d37a9-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d37a9-120">Library</span></span><br/> | <dl> <span data-ttu-id="d37a9-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d37a9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d37a9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d37a9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37a9-123">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="d37a9-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




