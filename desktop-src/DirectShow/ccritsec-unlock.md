---
description: La méthode unlock Déverrouille l’objet section critique.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: CCritSec. Unlock, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545553"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="a841d-103">CCritSec. Unlock, méthode</span><span class="sxs-lookup"><span data-stu-id="a841d-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="a841d-104">La méthode **Unlock** déverrouille l’objet section critique.</span><span class="sxs-lookup"><span data-stu-id="a841d-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a841d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a841d-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="a841d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a841d-106">Parameters</span></span>

<span data-ttu-id="a841d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a841d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a841d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a841d-108">Return value</span></span>

<span data-ttu-id="a841d-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a841d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a841d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a841d-110">Remarks</span></span>

<span data-ttu-id="a841d-111">Cette méthode appelle la fonction [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="a841d-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="a841d-112">Appelez cette méthode une fois pour chaque appel à la méthode [**CCritSec :: Lock**](ccritsec-lock.md) .</span><span class="sxs-lookup"><span data-stu-id="a841d-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a841d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a841d-113">Requirements</span></span>



| <span data-ttu-id="a841d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a841d-114">Requirement</span></span> | <span data-ttu-id="a841d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a841d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a841d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a841d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a841d-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a841d-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a841d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a841d-118">Library</span></span><br/> | <dl> <span data-ttu-id="a841d-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a841d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a841d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a841d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a841d-121">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="a841d-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

