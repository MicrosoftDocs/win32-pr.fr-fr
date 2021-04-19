---
description: La méthode active indique au code confidentiel que le filtre est maintenant actif.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: CBasePin. active, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521655"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="9f9ac-103">CBasePin. active, méthode</span><span class="sxs-lookup"><span data-stu-id="9f9ac-103">CBasePin.Active method</span></span>

<span data-ttu-id="9f9ac-104">La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f9ac-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="9f9ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f9ac-106">Parameters</span></span>

<span data-ttu-id="9f9ac-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f9ac-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f9ac-108">Return value</span></span>

<span data-ttu-id="9f9ac-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9ac-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9f9ac-110">Remarks</span></span>

<span data-ttu-id="9f9ac-111">Lorsque le filtre passe de arrêté à suspendu, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur toutes les broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="9f9ac-112">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-112">This method does nothing in the base class.</span></span> <span data-ttu-id="9f9ac-113">Les classes dérivées peuvent substituer cette méthode. par exemple, un code confidentiel peut valider des allocateurs ou obtenir des ressources matérielles.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="9f9ac-114">L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour avant le retour de cette fonction membre, donc ne Testez pas l’État à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9f9ac-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f9ac-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f9ac-115">Requirements</span></span>



| <span data-ttu-id="9f9ac-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f9ac-116">Requirement</span></span> | <span data-ttu-id="9f9ac-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f9ac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9ac-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f9ac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9f9ac-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f9ac-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f9ac-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f9ac-120">Library</span></span><br/> | <dl> <span data-ttu-id="9f9ac-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f9ac-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f9ac-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f9ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9ac-123">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="9f9ac-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




