---
description: Identificateur de thread du thread propriétaire.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Membre CCritSec :: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540663"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="4082a-103">CCritSec :: m \_ currentOwner, membre</span><span class="sxs-lookup"><span data-stu-id="4082a-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="4082a-104">Identificateur de thread du thread propriétaire.</span><span class="sxs-lookup"><span data-stu-id="4082a-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="4082a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4082a-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="4082a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4082a-106">Remarks</span></span>

<span data-ttu-id="4082a-107">Cette variable membre est définie uniquement dans la version Debug de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="4082a-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="4082a-108">Les [fonctions de débogage de la section critique](critical-section-debugging-functions.md) utilisent ce membre.</span><span class="sxs-lookup"><span data-stu-id="4082a-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="4082a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4082a-109">Requirements</span></span>



| <span data-ttu-id="4082a-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4082a-110">Requirement</span></span> | <span data-ttu-id="4082a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4082a-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4082a-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="4082a-112">Header</span></span><br/>  | <dl> <span data-ttu-id="4082a-113"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4082a-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4082a-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4082a-114">Library</span></span><br/> | <dl> <span data-ttu-id="4082a-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4082a-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4082a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4082a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4082a-117">**CCritSec, classe**</span><span class="sxs-lookup"><span data-stu-id="4082a-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




