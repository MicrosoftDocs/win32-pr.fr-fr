---
description: Section critique qui verrouille les données partagées entre les threads.
ms.assetid: 87966d7d-6677-462f-93bc-fedda7f0bdcf
title: 'Membre CAMThread :: m_WorkerLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WorkerLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fce6c2ff2a7857f6cb69ce3bb92fe2b6f24bcbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545561"
---
# <a name="camthreadm_workerlock-member"></a><span data-ttu-id="da83c-103">CAMThread :: m \_ WorkerLock, membre</span><span class="sxs-lookup"><span data-stu-id="da83c-103">CAMThread::m\_WorkerLock member</span></span>

<span data-ttu-id="da83c-104">Section critique qui verrouille les données partagées entre les threads.</span><span class="sxs-lookup"><span data-stu-id="da83c-104">Critical section that locks data shared among threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="da83c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da83c-105">Syntax</span></span>


```C++
CCritSec m_WorkerLock;
```



## <a name="requirements"></a><span data-ttu-id="da83c-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da83c-106">Requirements</span></span>



| <span data-ttu-id="da83c-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da83c-107">Requirement</span></span> | <span data-ttu-id="da83c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="da83c-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da83c-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="da83c-109">Header</span></span><br/>  | <dl> <span data-ttu-id="da83c-110"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da83c-110"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="da83c-111">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da83c-111">Library</span></span><br/> | <dl> <span data-ttu-id="da83c-112"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="da83c-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da83c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da83c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da83c-114">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="da83c-114">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




