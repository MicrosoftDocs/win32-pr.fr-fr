---
description: 'Méthode CBasePin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099437"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="45875-103">Méthode CBasePin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="45875-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="45875-104">La `BreakConnect` méthode libère le code confidentiel d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="45875-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="45875-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45875-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="45875-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45875-106">Parameters</span></span>

<span data-ttu-id="45875-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="45875-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45875-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="45875-108">Return value</span></span>

<span data-ttu-id="45875-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45875-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="45875-110">Notes </span><span class="sxs-lookup"><span data-stu-id="45875-110">Remarks</span></span>

<span data-ttu-id="45875-111">Cette méthode est appelée lors de la déconnexion du code confidentiel par la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="45875-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="45875-112">Elle est également appelée pendant une tentative de connexion si la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) échoue.</span><span class="sxs-lookup"><span data-stu-id="45875-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="45875-113">Cette méthode doit libérer toutes les ressources qui ont été obtenues par la méthode **CheckConnect** .</span><span class="sxs-lookup"><span data-stu-id="45875-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="45875-114">Par exemple, si **CheckConnect** alloue de la mémoire, `BreakConnect` doit libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="45875-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="45875-115">Si **CheckConnect** interroge le code PIN de connexion pour une interface, `BreakConnect` doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="45875-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="45875-116">Notez que `BreakConnect` peut être appelé sans appel correspondant à **CompleteConnect**.</span><span class="sxs-lookup"><span data-stu-id="45875-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="45875-117">Par conséquent, vous ne pouvez pas supposer que **CompleteConnect** a été appelé précédemment.</span><span class="sxs-lookup"><span data-stu-id="45875-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="45875-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45875-118">Requirements</span></span>



| <span data-ttu-id="45875-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45875-119">Requirement</span></span> | <span data-ttu-id="45875-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="45875-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45875-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="45875-121">Header</span></span><br/>  | <dl> <span data-ttu-id="45875-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45875-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="45875-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="45875-123">Library</span></span><br/> | <dl> <span data-ttu-id="45875-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="45875-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45875-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45875-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45875-126">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="45875-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




