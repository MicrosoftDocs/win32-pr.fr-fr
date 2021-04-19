---
description: Section critique qui protège l’état de blocage.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Membre CDynamicOutputPin :: m_BlockStateLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524006"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="cf053-103">CDynamicOutputPin :: m \_ BlockStateLock, membre</span><span class="sxs-lookup"><span data-stu-id="cf053-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="cf053-104">Section critique qui protège l’état de blocage.</span><span class="sxs-lookup"><span data-stu-id="cf053-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf053-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf053-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="cf053-106">Notes</span><span class="sxs-lookup"><span data-stu-id="cf053-106">Remarks</span></span>

<span data-ttu-id="cf053-107">Tenez cette section critique avant d’utiliser l’une des variables de membre suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf053-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="cf053-108">**CDynamicOutputPin :: m \_ BlockState**</span><span class="sxs-lookup"><span data-stu-id="cf053-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="cf053-109">**CDynamicOutputPin :: m \_ dwBlockCallerThreadID**</span><span class="sxs-lookup"><span data-stu-id="cf053-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="cf053-110">**CDynamicOutputPin :: m \_ dwNumOutstandingOutputPinUsers**</span><span class="sxs-lookup"><span data-stu-id="cf053-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="cf053-111">**CDynamicOutputPin :: m \_ hNotifyCallerPinBlockedEvent**</span><span class="sxs-lookup"><span data-stu-id="cf053-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="cf053-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf053-112">Requirements</span></span>



| <span data-ttu-id="cf053-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf053-113">Requirement</span></span> | <span data-ttu-id="cf053-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf053-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf053-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf053-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cf053-116"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf053-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf053-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cf053-117">Library</span></span><br/> | <dl> <span data-ttu-id="cf053-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cf053-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf053-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf053-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf053-120">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="cf053-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




