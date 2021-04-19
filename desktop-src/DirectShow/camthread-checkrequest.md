---
description: La méthode CheckRequest vérifie s’il existe une demande, sans blocage.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Méthode CAMThread. CheckRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528135"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="ebe8c-103">Méthode CAMThread. CheckRequest</span><span class="sxs-lookup"><span data-stu-id="ebe8c-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="ebe8c-104">La `CheckRequest` méthode vérifie s’il existe une demande, sans blocage.</span><span class="sxs-lookup"><span data-stu-id="ebe8c-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe8c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebe8c-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="ebe8c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebe8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe8c-107">*pParam*</span><span class="sxs-lookup"><span data-stu-id="ebe8c-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe8c-108">Pointeur vers une variable qui reçoit la valeur passée dans le dernier appel à la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="ebe8c-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe8c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebe8c-109">Return value</span></span>

<span data-ttu-id="ebe8c-110">Retourne la **valeur true** s’il y a une demande en attente, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ebe8c-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe8c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ebe8c-111">Remarks</span></span>

<span data-ttu-id="ebe8c-112">Cette méthode est une version sans blocage de la méthode [**CAMThread :: GetRequest**](camthread-getrequest.md) .</span><span class="sxs-lookup"><span data-stu-id="ebe8c-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="ebe8c-113">Si un autre thread attend un appel à CallWorker, cette méthode récupère le paramètre de requête et retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ebe8c-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="ebe8c-114">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="ebe8c-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="ebe8c-115">Si la méthode retourne la **valeur true**, appelez la méthode [**CAMThread :: reply**](camthread-reply.md) pour libérer le thread demandeur.</span><span class="sxs-lookup"><span data-stu-id="ebe8c-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe8c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe8c-116">Requirements</span></span>



| <span data-ttu-id="ebe8c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebe8c-117">Requirement</span></span> | <span data-ttu-id="ebe8c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebe8c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe8c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebe8c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ebe8c-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe8c-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ebe8c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ebe8c-121">Library</span></span><br/> | <dl> <span data-ttu-id="ebe8c-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe8c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe8c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe8c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe8c-124">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="ebe8c-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




