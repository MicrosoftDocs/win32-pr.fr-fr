---
description: La méthode IsQueued détermine si l’objet utilise un thread de travail pour fournir des exemples.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: Méthode COutputQueue. IsQueued (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540206"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="8cbd3-103">Méthode COutputQueue. IsQueued</span><span class="sxs-lookup"><span data-stu-id="8cbd3-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="8cbd3-104">La `IsQueued` méthode détermine si l’objet utilise un thread de travail pour fournir des exemples.</span><span class="sxs-lookup"><span data-stu-id="8cbd3-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cbd3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cbd3-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="8cbd3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cbd3-106">Parameters</span></span>

<span data-ttu-id="8cbd3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8cbd3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cbd3-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cbd3-108">Return value</span></span>

<span data-ttu-id="8cbd3-109">Retourne la **valeur true** si l’objet utilise un thread de travail, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8cbd3-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cbd3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cbd3-110">Requirements</span></span>



| <span data-ttu-id="8cbd3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cbd3-111">Requirement</span></span> | <span data-ttu-id="8cbd3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cbd3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbd3-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cbd3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="8cbd3-114"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cbd3-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8cbd3-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8cbd3-115">Library</span></span><br/> | <dl> <span data-ttu-id="8cbd3-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8cbd3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cbd3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cbd3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbd3-118">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="8cbd3-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




