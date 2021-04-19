---
description: La méthode Close attend que le thread se termine, puis libère ses ressources.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Méthode CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525592"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="b8dff-103">CAMThread. Close, méthode</span><span class="sxs-lookup"><span data-stu-id="b8dff-103">CAMThread.Close method</span></span>

<span data-ttu-id="b8dff-104">La `Close` méthode attend que le thread se termine, puis libère ses ressources.</span><span class="sxs-lookup"><span data-stu-id="b8dff-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8dff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8dff-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="b8dff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8dff-106">Parameters</span></span>

<span data-ttu-id="b8dff-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b8dff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8dff-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8dff-108">Return value</span></span>

<span data-ttu-id="b8dff-109">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b8dff-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8dff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b8dff-110">Remarks</span></span>

<span data-ttu-id="b8dff-111">Avant d’appeler cette méthode, vous devez fournir un moyen de quitter le thread.</span><span class="sxs-lookup"><span data-stu-id="b8dff-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="b8dff-112">Par exemple, dans votre méthode [**CAMThread :: ThreadProc**](camthread-threadproc.md) , définissez une demande qui signale au thread de s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="b8dff-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="b8dff-113">Appelez ensuite la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) avec cette valeur.</span><span class="sxs-lookup"><span data-stu-id="b8dff-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="b8dff-114">La méthode du destructeur [**~ CAMThread**](camthread--camthread.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b8dff-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8dff-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8dff-115">Requirements</span></span>



| <span data-ttu-id="b8dff-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8dff-116">Requirement</span></span> | <span data-ttu-id="b8dff-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8dff-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dff-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8dff-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b8dff-119"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8dff-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b8dff-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8dff-120">Library</span></span><br/> | <dl> <span data-ttu-id="b8dff-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b8dff-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8dff-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8dff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8dff-123">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="b8dff-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




