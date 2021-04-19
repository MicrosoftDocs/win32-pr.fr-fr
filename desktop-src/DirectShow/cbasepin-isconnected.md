---
description: La méthode IsConnected détermine si le pin est connecté à un autre code confidentiel.
ms.assetid: d8b9b43b-6f8d-4d75-9688-f0cee3794a78
title: CBasePin. IsConnected, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b857e1ceff4844d66c55cf729a3d2b9771d48846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537883"
---
# <a name="cbasepinisconnected-method"></a><span data-ttu-id="cd59d-103">CBasePin. IsConnected, méthode</span><span class="sxs-lookup"><span data-stu-id="cd59d-103">CBasePin.IsConnected method</span></span>

<span data-ttu-id="cd59d-104">La `IsConnected` méthode détermine si le pin est connecté à un autre code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="cd59d-104">The `IsConnected` method determines whether the pin is connected to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd59d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd59d-105">Syntax</span></span>


```C++
BOOL IsConnected();
```



## <a name="parameters"></a><span data-ttu-id="cd59d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd59d-106">Parameters</span></span>

<span data-ttu-id="cd59d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cd59d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd59d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd59d-108">Return value</span></span>

<span data-ttu-id="cd59d-109">Retourne la **valeur true** si le code PIN est connecté.</span><span class="sxs-lookup"><span data-stu-id="cd59d-109">Returns **TRUE** if the pin is connected.</span></span> <span data-ttu-id="cd59d-110">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="cd59d-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd59d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd59d-111">Requirements</span></span>



| <span data-ttu-id="cd59d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd59d-112">Requirement</span></span> | <span data-ttu-id="cd59d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd59d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd59d-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd59d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="cd59d-115"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd59d-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd59d-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd59d-116">Library</span></span><br/> | <dl> <span data-ttu-id="cd59d-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cd59d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd59d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd59d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd59d-119">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="cd59d-119">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




