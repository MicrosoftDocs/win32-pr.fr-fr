---
description: La méthode NotifyThread avertit le thread que la file d’attente contient des données.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: Méthode COutputQueue. NotifyThread (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530384"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="b57a3-103">Méthode COutputQueue. NotifyThread</span><span class="sxs-lookup"><span data-stu-id="b57a3-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="b57a3-104">La `NotifyThread` méthode avertit le thread que la file d’attente contient des données.</span><span class="sxs-lookup"><span data-stu-id="b57a3-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b57a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b57a3-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="b57a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b57a3-106">Parameters</span></span>

<span data-ttu-id="b57a3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b57a3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b57a3-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b57a3-108">Return value</span></span>

<span data-ttu-id="b57a3-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b57a3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b57a3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b57a3-110">Remarks</span></span>

<span data-ttu-id="b57a3-111">Maintenez la section critique avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b57a3-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57a3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b57a3-112">Requirements</span></span>



| <span data-ttu-id="b57a3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b57a3-113">Requirement</span></span> | <span data-ttu-id="b57a3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b57a3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b57a3-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="b57a3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b57a3-116"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b57a3-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b57a3-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b57a3-117">Library</span></span><br/> | <dl> <span data-ttu-id="b57a3-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b57a3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b57a3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b57a3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57a3-120">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="b57a3-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




