---
description: La méthode GetRequest attend la requête suivante.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Méthode CAMThread. GetRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544023"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="91c77-103">Méthode CAMThread. GetRequest</span><span class="sxs-lookup"><span data-stu-id="91c77-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="91c77-104">La `GetRequest` méthode attend la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="91c77-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91c77-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="91c77-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91c77-106">Parameters</span></span>

<span data-ttu-id="91c77-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="91c77-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91c77-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91c77-108">Return value</span></span>

<span data-ttu-id="91c77-109">Retourne une valeur définie par la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="91c77-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c77-110">Notes</span><span class="sxs-lookup"><span data-stu-id="91c77-110">Remarks</span></span>

<span data-ttu-id="91c77-111">Cette méthode bloque jusqu’à ce qu’un autre thread appelle la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="91c77-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="91c77-112">Elle retourne ensuite le paramètre qui a été passé à CallWorker.</span><span class="sxs-lookup"><span data-stu-id="91c77-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="91c77-113">Appelez la méthode [**CAMThread :: reply**](camthread-reply.md) pour libérer le thread demandeur.</span><span class="sxs-lookup"><span data-stu-id="91c77-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c77-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91c77-114">Requirements</span></span>



| <span data-ttu-id="91c77-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91c77-115">Requirement</span></span> | <span data-ttu-id="91c77-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91c77-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c77-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="91c77-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91c77-118"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91c77-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="91c77-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91c77-119">Library</span></span><br/> | <dl> <span data-ttu-id="91c77-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="91c77-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c77-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91c77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c77-122">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="91c77-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




