---
description: La méthode inactive indique au code confidentiel que le filtre n’est plus actif.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: CBasePin. inactive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544456"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="4fe09-103">CBasePin. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="4fe09-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="4fe09-104">La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="4fe09-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fe09-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="4fe09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fe09-106">Parameters</span></span>

<span data-ttu-id="4fe09-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4fe09-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4fe09-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4fe09-108">Return value</span></span>

<span data-ttu-id="4fe09-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4fe09-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe09-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4fe09-110">Remarks</span></span>

<span data-ttu-id="4fe09-111">Quand le filtre s’arrête, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur toutes les broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="4fe09-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="4fe09-112">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="4fe09-112">This method does nothing in the base class.</span></span> <span data-ttu-id="4fe09-113">Les classes dérivées doivent remplacer cette méthode pour libérer toutes les ressources obtenues par la méthode [**CBasePin :: active**](cbasepin-active.md) ; par exemple, pour désallouer les allocateurs du pin.</span><span class="sxs-lookup"><span data-stu-id="4fe09-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="4fe09-114">L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour tant que cette méthode n’a pas retourné de valeur, donc ne Testez pas l’État à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4fe09-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe09-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fe09-115">Requirements</span></span>



| <span data-ttu-id="4fe09-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fe09-116">Requirement</span></span> | <span data-ttu-id="4fe09-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fe09-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe09-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fe09-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4fe09-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fe09-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4fe09-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4fe09-120">Library</span></span><br/> | <dl> <span data-ttu-id="4fe09-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4fe09-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe09-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fe09-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe09-123">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="4fe09-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




