---
description: 'La méthode GetRequestHandle récupère un handle vers l’événement signalé par la méthode CAMThread :: CallWorker.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Méthode CAMThread. GetRequestHandle (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530338"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="c3563-103">Méthode CAMThread. GetRequestHandle</span><span class="sxs-lookup"><span data-stu-id="c3563-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="c3563-104">La `GetRequestHandle` méthode récupère un handle vers l’événement signalé par la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="c3563-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3563-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3563-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="c3563-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3563-106">Parameters</span></span>

<span data-ttu-id="c3563-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c3563-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3563-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3563-108">Return value</span></span>

<span data-ttu-id="c3563-109">Retourne un handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="c3563-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3563-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c3563-110">Remarks</span></span>

<span data-ttu-id="c3563-111">La classe CAMEvent conserve un événement de réinitialisation manuelle privé, qui est défini par CallWorker et réinitialisé par la méthode [**CAMThread :: reply**](camthread-reply.md) .</span><span class="sxs-lookup"><span data-stu-id="c3563-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="c3563-112">Si vous appelez une fonction telle que WaitForMultipleObjects, utilisez GetRequestHandle pour récupérer le handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="c3563-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3563-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3563-113">Requirements</span></span>



| <span data-ttu-id="c3563-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3563-114">Requirement</span></span> | <span data-ttu-id="c3563-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3563-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3563-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3563-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c3563-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3563-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c3563-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3563-118">Library</span></span><br/> | <dl> <span data-ttu-id="c3563-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c3563-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3563-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3563-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3563-121">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="c3563-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




