---
description: La méthode CanReconnectWhenActive interroge si le code PIN prend en charge les reconnexions dynamiques.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Méthode CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525568"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="69496-103">Méthode CBasePin. CanReconnectWhenActive</span><span class="sxs-lookup"><span data-stu-id="69496-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="69496-104">La `CanReconnectWhenActive` méthode interroge si le code PIN prend en charge les reconnexions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="69496-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="69496-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69496-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="69496-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69496-106">Parameters</span></span>

<span data-ttu-id="69496-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="69496-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69496-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69496-108">Return value</span></span>

<span data-ttu-id="69496-109">Retourne une valeur booléenne qui spécifie si le code confidentiel peut se reconnecter dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="69496-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="69496-110">Si la **valeur est true**, le code confidentiel peut se reconnecter dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="69496-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="69496-111">Notes</span><span class="sxs-lookup"><span data-stu-id="69496-111">Remarks</span></span>

<span data-ttu-id="69496-112">Par défaut, vous devez arrêter un filtre avant de reconnecter l’un de ses pin.</span><span class="sxs-lookup"><span data-stu-id="69496-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="69496-113">Toutefois, si un code PIN prend en charge la reconnexion dynamique, il peut se reconnecter alors que le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="69496-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="69496-114">Pour plus d’informations, consultez [génération de graphiques dynamiques](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="69496-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69496-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69496-115">Requirements</span></span>



| <span data-ttu-id="69496-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69496-116">Requirement</span></span> | <span data-ttu-id="69496-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="69496-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69496-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="69496-118">Header</span></span><br/>  | <dl> <span data-ttu-id="69496-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69496-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="69496-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69496-120">Library</span></span><br/> | <dl> <span data-ttu-id="69496-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="69496-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69496-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69496-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69496-123">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="69496-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




