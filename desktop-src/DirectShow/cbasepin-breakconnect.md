---
description: La méthode BreakConnect libère le code confidentiel d’une connexion.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Méthode CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526661"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="22b2b-103">Méthode CBasePin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="22b2b-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="22b2b-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="22b2b-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22b2b-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="22b2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22b2b-106">Parameters</span></span>

<span data-ttu-id="22b2b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="22b2b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22b2b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22b2b-108">Return value</span></span>

<span data-ttu-id="22b2b-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22b2b-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="22b2b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="22b2b-110">Remarks</span></span>

<span data-ttu-id="22b2b-111">Cette méthode est appelée lors de la déconnexion du code confidentiel par la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="22b2b-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="22b2b-112">Elle est également appelée pendant une tentative de connexion si la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) échoue.</span><span class="sxs-lookup"><span data-stu-id="22b2b-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="22b2b-113">Cette méthode doit libérer toutes les ressources qui ont été obtenues par la méthode **CheckConnect** .</span><span class="sxs-lookup"><span data-stu-id="22b2b-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="22b2b-114">Par exemple, si **CheckConnect** alloue de la mémoire, `BreakConnect` doit libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="22b2b-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="22b2b-115">Si **CheckConnect** interroge le code PIN de connexion pour une interface, `BreakConnect` doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="22b2b-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="22b2b-116">Notez que `BreakConnect` peut être appelé sans appel correspondant à **CompleteConnect**.</span><span class="sxs-lookup"><span data-stu-id="22b2b-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="22b2b-117">Par conséquent, vous ne pouvez pas supposer que **CompleteConnect** a été appelé précédemment.</span><span class="sxs-lookup"><span data-stu-id="22b2b-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b2b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22b2b-118">Requirements</span></span>



| <span data-ttu-id="22b2b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22b2b-119">Requirement</span></span> | <span data-ttu-id="22b2b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="22b2b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b2b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="22b2b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22b2b-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22b2b-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22b2b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22b2b-123">Library</span></span><br/> | <dl> <span data-ttu-id="22b2b-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="22b2b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b2b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22b2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b2b-126">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="22b2b-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




