---
description: Méthode de destructeur.
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
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532668"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="1d396-103">CAMThread. ~ CAMThread, destructeur</span><span class="sxs-lookup"><span data-stu-id="1d396-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="1d396-104">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="1d396-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d396-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d396-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="1d396-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1d396-106">Remarks</span></span>

<span data-ttu-id="1d396-107">Le destructeur appelle la méthode [**CAMThread :: Close**](camthread-close.md) , qui attend que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="1d396-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d396-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d396-108">Requirements</span></span>



| <span data-ttu-id="1d396-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d396-109">Requirement</span></span> | <span data-ttu-id="1d396-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d396-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d396-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d396-111">Header</span></span><br/>  | <dl> <span data-ttu-id="1d396-112"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d396-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1d396-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d396-113">Library</span></span><br/> | <dl> <span data-ttu-id="1d396-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1d396-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d396-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d396-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d396-116">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="1d396-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




