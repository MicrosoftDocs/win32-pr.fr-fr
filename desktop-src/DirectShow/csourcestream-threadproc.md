---
description: 'La méthode ThreadProc est la procédure de thread pour le thread de travail. Cette méthode implémente la méthode CAMThread :: ThreadProc virtuelle pure.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Méthode CSourceStream. ThreadProc (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542251"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="6759f-104">CSourceStream. ThreadProc, méthode</span><span class="sxs-lookup"><span data-stu-id="6759f-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="6759f-105">La `ThreadProc` méthode est la procédure de thread pour le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="6759f-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="6759f-106">Cette méthode implémente la méthode [**CAMThread :: ThreadProc**](camthread-threadproc.md) virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="6759f-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6759f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6759f-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="6759f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6759f-108">Parameters</span></span>

<span data-ttu-id="6759f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6759f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6759f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6759f-110">Return value</span></span>

<span data-ttu-id="6759f-111">Retourne 0 si le thread s’est terminé correctement ou 1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6759f-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="6759f-112">Si la valeur de retour est 1, il est possible que les ressources du thread soient encore allouées.</span><span class="sxs-lookup"><span data-stu-id="6759f-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="6759f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6759f-113">Remarks</span></span>

<span data-ttu-id="6759f-114">Cette méthode attend indéfiniment les demandes de thread, en appelant la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="6759f-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="6759f-115">Si elle reçoit une demande [**CSourceStream :: Run**](csourcestream-run.md) ou [**CSourceStream ::P ause**](csourcestream-pause.md) , elle appelle la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="6759f-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="6759f-116">La méthode **DoBufferProcessingLoop** transmet les données jusqu’à ce qu’elles reçoivent une demande [**CSourceStream :: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="6759f-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="6759f-117">La procédure de thread s’arrête lorsqu’elle reçoit une demande [**CSourceStream :: Exit**](csourcestream-exit.md) .</span><span class="sxs-lookup"><span data-stu-id="6759f-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="6759f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6759f-118">Requirements</span></span>



| <span data-ttu-id="6759f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6759f-119">Requirement</span></span> | <span data-ttu-id="6759f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6759f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6759f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6759f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6759f-122"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6759f-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6759f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6759f-123">Library</span></span><br/> | <dl> <span data-ttu-id="6759f-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6759f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6759f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6759f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6759f-126">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="6759f-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




