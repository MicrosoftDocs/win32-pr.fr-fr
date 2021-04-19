---
description: La méthode GetDueHandle récupère le descripteur d’événement à signaler.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Méthode CCmdQueue. GetDueHandle (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545341"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="debce-103">Méthode CCmdQueue. GetDueHandle</span><span class="sxs-lookup"><span data-stu-id="debce-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="debce-104">La `GetDueHandle` méthode récupère le handle d’événement à signaler.</span><span class="sxs-lookup"><span data-stu-id="debce-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="debce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="debce-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="debce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="debce-106">Parameters</span></span>

<span data-ttu-id="debce-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="debce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="debce-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="debce-108">Return value</span></span>

<span data-ttu-id="debce-109">Retourne le handle d’événement.</span><span class="sxs-lookup"><span data-stu-id="debce-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="debce-110">Notes</span><span class="sxs-lookup"><span data-stu-id="debce-110">Remarks</span></span>

<span data-ttu-id="debce-111">Retourne le descripteur d’événement chaque fois que des commandes différées sont dues pour l’exécution (quand [**CCmdQueue :: GetDueCommand**](ccmdqueue-getduecommand.md) n’est pas bloqué).</span><span class="sxs-lookup"><span data-stu-id="debce-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="debce-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="debce-112">Requirements</span></span>



| <span data-ttu-id="debce-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="debce-113">Requirement</span></span> | <span data-ttu-id="debce-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="debce-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="debce-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="debce-115">Header</span></span><br/>  | <dl> <span data-ttu-id="debce-116"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="debce-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="debce-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="debce-117">Library</span></span><br/> | <dl> <span data-ttu-id="debce-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="debce-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="debce-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="debce-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="debce-120">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="debce-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




