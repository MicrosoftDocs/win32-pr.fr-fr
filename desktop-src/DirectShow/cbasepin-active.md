---
description: 'CBasePin. active, méthode : la méthode active indique au code confidentiel que le filtre est maintenant actif.'
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
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096106"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="ee642-103">CBasePin. active, méthode</span><span class="sxs-lookup"><span data-stu-id="ee642-103">CBasePin.Active method</span></span>

<span data-ttu-id="ee642-104">La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="ee642-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee642-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee642-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="ee642-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee642-106">Parameters</span></span>

<span data-ttu-id="ee642-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee642-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee642-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ee642-108">Return value</span></span>

<span data-ttu-id="ee642-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee642-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee642-110">Notes </span><span class="sxs-lookup"><span data-stu-id="ee642-110">Remarks</span></span>

<span data-ttu-id="ee642-111">Lorsque le filtre passe de arrêté à suspendu, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur toutes les broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="ee642-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="ee642-112">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="ee642-112">This method does nothing in the base class.</span></span> <span data-ttu-id="ee642-113">Les classes dérivées peuvent substituer cette méthode. par exemple, un code confidentiel peut valider des allocateurs ou obtenir des ressources matérielles.</span><span class="sxs-lookup"><span data-stu-id="ee642-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="ee642-114">L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour avant le retour de cette fonction membre, donc ne Testez pas l’État à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ee642-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee642-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee642-115">Requirements</span></span>



| <span data-ttu-id="ee642-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee642-116">Requirement</span></span> | <span data-ttu-id="ee642-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee642-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee642-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee642-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ee642-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee642-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ee642-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee642-120">Library</span></span><br/> | <dl> <span data-ttu-id="ee642-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ee642-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee642-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee642-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee642-123">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="ee642-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




