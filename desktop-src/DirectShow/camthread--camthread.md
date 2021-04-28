---
description: CAMThread. ~ CAMThread, destructeur, méthode de destructeur.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CAMThread. ~ CAMThread, destructeur (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096437"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="103f5-103">CAMThread. ~ CAMThread, destructeur</span><span class="sxs-lookup"><span data-stu-id="103f5-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="103f5-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="103f5-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="103f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="103f5-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="103f5-106">Notes </span><span class="sxs-lookup"><span data-stu-id="103f5-106">Remarks</span></span>

<span data-ttu-id="103f5-107">Le destructeur appelle la méthode [**CAMThread :: Close**](camthread-close.md) , qui attend que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="103f5-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="103f5-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="103f5-108">Requirements</span></span>



| <span data-ttu-id="103f5-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="103f5-109">Requirement</span></span> | <span data-ttu-id="103f5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="103f5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="103f5-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="103f5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="103f5-112"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="103f5-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="103f5-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="103f5-113">Library</span></span><br/> | <dl> <span data-ttu-id="103f5-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="103f5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103f5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="103f5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103f5-116">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="103f5-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




