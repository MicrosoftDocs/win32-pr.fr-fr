---
description: 'La méthode active indique au code confidentiel que le filtre est maintenant actif. Cette méthode remplace la méthode CBasePin :: active.'
ms.assetid: e98ca947-df2f-41a7-9785-b35bd1dde1e6
title: CRenderedInputPin. active, méthode (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae56439f5e19aa5c039ac81bdd8a7aafe0f2174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524055"
---
# <a name="crenderedinputpinactive-method"></a><span data-ttu-id="7c824-104">CRenderedInputPin. active, méthode</span><span class="sxs-lookup"><span data-stu-id="7c824-104">CRenderedInputPin.Active method</span></span>

<span data-ttu-id="7c824-105">La `Active` méthode notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="7c824-105">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="7c824-106">Cette méthode remplace la méthode [**CBasePin :: active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="7c824-106">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c824-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c824-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="7c824-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c824-108">Parameters</span></span>

<span data-ttu-id="7c824-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7c824-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c824-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c824-110">Return value</span></span>

<span data-ttu-id="7c824-111">Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7c824-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c824-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c824-112">Requirements</span></span>



| <span data-ttu-id="7c824-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c824-113">Requirement</span></span> | <span data-ttu-id="7c824-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c824-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c824-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c824-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7c824-116"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c824-116"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c824-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c824-117">Library</span></span><br/> | <dl> <span data-ttu-id="7c824-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7c824-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c824-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c824-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c824-120">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="7c824-120">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




