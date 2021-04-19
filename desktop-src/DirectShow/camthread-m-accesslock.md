---
description: Section critique qui empêche l’accès du thread par d’autres threads.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Membre CAMThread :: m_AccessLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541297"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="f3b37-103">CAMThread :: m \_ AccessLock, membre</span><span class="sxs-lookup"><span data-stu-id="f3b37-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="f3b37-104">Section critique qui empêche l’accès du thread par d’autres threads.</span><span class="sxs-lookup"><span data-stu-id="f3b37-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3b37-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="f3b37-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f3b37-106">Remarks</span></span>

<span data-ttu-id="f3b37-107">Les méthodes [**CAMThread :: Create**](camthread-create.md) et [**CAMThread :: CallWorker**](camthread-callworker.md) contiennent ce verrou, pour sérialiser des opérations sur le thread.</span><span class="sxs-lookup"><span data-stu-id="f3b37-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b37-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3b37-108">Requirements</span></span>



| <span data-ttu-id="f3b37-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3b37-109">Requirement</span></span> | <span data-ttu-id="f3b37-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3b37-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b37-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3b37-111">Header</span></span><br/>  | <dl> <span data-ttu-id="f3b37-112"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3b37-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f3b37-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f3b37-113">Library</span></span><br/> | <dl> <span data-ttu-id="f3b37-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3b37-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b37-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3b37-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b37-116">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="f3b37-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




