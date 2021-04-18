---
description: La méthode ThreadProc est la procédure de thread.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: CAMThread. ThreadProc, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526366"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="187b2-103">CAMThread. ThreadProc, méthode</span><span class="sxs-lookup"><span data-stu-id="187b2-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="187b2-104">La `ThreadProc` méthode est la procédure de thread.</span><span class="sxs-lookup"><span data-stu-id="187b2-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="187b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="187b2-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="187b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="187b2-106">Parameters</span></span>

<span data-ttu-id="187b2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="187b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="187b2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="187b2-108">Return value</span></span>

<span data-ttu-id="187b2-109">Retourne une valeur **DWORD** dont la signification est définie par la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="187b2-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="187b2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="187b2-110">Remarks</span></span>

<span data-ttu-id="187b2-111">Il s’agit d’une méthode virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="187b2-111">This is a pure virtual method.</span></span> <span data-ttu-id="187b2-112">Implémentez cette méthode dans votre classe dérivée pour fournir une procédure de thread.</span><span class="sxs-lookup"><span data-stu-id="187b2-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="187b2-113">Quand la méthode [**CAMThread :: Create**](camthread-create.md) crée un thread, elle donne l’adresse de la méthode [**CAMThread :: InitialThreadProc**](camthread-initialthreadproc.md) , qui à son tour appelle votre méthode ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="187b2-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="187b2-114">En règle générale, votre méthode ThreadProc entrera dans une boucle qui récupère les requêtes (en appelant les méthodes [**CAMThread :: GetRequest**](camthread-getrequest.md) ou [**CAMThread :: CheckRequest**](camthread-checkrequest.md) ) et traite les données.</span><span class="sxs-lookup"><span data-stu-id="187b2-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="187b2-115">Lorsque cette méthode est retournée, le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="187b2-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="187b2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="187b2-116">Requirements</span></span>



| <span data-ttu-id="187b2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="187b2-117">Requirement</span></span> | <span data-ttu-id="187b2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="187b2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187b2-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="187b2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="187b2-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="187b2-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="187b2-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="187b2-121">Library</span></span><br/> | <dl> <span data-ttu-id="187b2-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="187b2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187b2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="187b2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187b2-124">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="187b2-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




