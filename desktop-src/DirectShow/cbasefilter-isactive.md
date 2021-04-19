---
description: La méthode IsActive détermine si le filtre est actuellement actif (en cours d’exécution ou en pause).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: CBaseFilter. IsActive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63cf2cd78bb61562c9b4d6a09de3d88c88d4c643
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545606"
---
# <a name="cbasefilterisactive-method"></a><span data-ttu-id="58549-103">CBaseFilter. IsActive, méthode</span><span class="sxs-lookup"><span data-stu-id="58549-103">CBaseFilter.IsActive method</span></span>

<span data-ttu-id="58549-104">La `IsActive` méthode détermine si le filtre est actuellement actif (en cours d’exécution ou en pause).</span><span class="sxs-lookup"><span data-stu-id="58549-104">The `IsActive` method determines whether the filter is currently active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="58549-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58549-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="58549-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58549-106">Parameters</span></span>

<span data-ttu-id="58549-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="58549-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58549-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58549-108">Return value</span></span>

<span data-ttu-id="58549-109">Retourne la **valeur true** si le filtre est suspendu ou en cours d’exécution, ou **false** s’il est arrêté.</span><span class="sxs-lookup"><span data-stu-id="58549-109">Returns **TRUE** if the filter is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="58549-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58549-110">Requirements</span></span>



| <span data-ttu-id="58549-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58549-111">Requirement</span></span> | <span data-ttu-id="58549-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="58549-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58549-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="58549-113">Header</span></span><br/>  | <dl> <span data-ttu-id="58549-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58549-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="58549-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58549-115">Library</span></span><br/> | <dl> <span data-ttu-id="58549-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="58549-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58549-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58549-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58549-118">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="58549-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




