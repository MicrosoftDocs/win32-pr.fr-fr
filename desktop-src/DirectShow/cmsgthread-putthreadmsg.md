---
description: Met en file d’attente une demande d’exécution par le thread de travail.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Méthode CMsgThread. PutThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533176"
---
# <a name="cmsgthreadputthreadmsg-method"></a><span data-ttu-id="4439d-103">Méthode CMsgThread. PutThreadMsg</span><span class="sxs-lookup"><span data-stu-id="4439d-103">CMsgThread.PutThreadMsg method</span></span>

<span data-ttu-id="4439d-104">Met en file d’attente une demande d’exécution par le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="4439d-104">Queues a request for execution by the worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="4439d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4439d-105">Syntax</span></span>


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="4439d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4439d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4439d-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="4439d-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="4439d-108">Code de la requête.</span><span class="sxs-lookup"><span data-stu-id="4439d-108">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="4439d-109">*dwMsgFlags*</span><span class="sxs-lookup"><span data-stu-id="4439d-109">*dwMsgFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4439d-110">Paramètre flags facultatif.</span><span class="sxs-lookup"><span data-stu-id="4439d-110">Optional flags parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4439d-111">*lpMsgParam*</span><span class="sxs-lookup"><span data-stu-id="4439d-111">*lpMsgParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4439d-112">Pointeur facultatif vers un bloc de données contenant des paramètres ou des valeurs de retour supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4439d-112">Optional pointer to a data block containing additional parameters or return values.</span></span> <span data-ttu-id="4439d-113">Doit être statique ou alloué par segment de mémoire et non automatique.</span><span class="sxs-lookup"><span data-stu-id="4439d-113">Must be statically or heap-allocated and not automatic.</span></span>

</dd> <dt>

<span data-ttu-id="4439d-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="4439d-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="4439d-115">Pointeur facultatif vers un objet d’événement à signaler à l’achèvement.</span><span class="sxs-lookup"><span data-stu-id="4439d-115">Optional pointer to an event object to be signaled upon completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4439d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4439d-116">Return value</span></span>

<span data-ttu-id="4439d-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4439d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4439d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4439d-118">Remarks</span></span>

<span data-ttu-id="4439d-119">Cette fonction membre met en file d’attente une requête d’exécution par le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="4439d-119">This member function queues a request for execution by the worker thread.</span></span> <span data-ttu-id="4439d-120">Les paramètres de cette fonction membre seront mis en file d’attente (dans un objet [**CMsg**](cmsg.md) ) et passés à la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) du thread de travail.</span><span class="sxs-lookup"><span data-stu-id="4439d-120">The parameters of this member function will be queued (in a [**CMsg**](cmsg.md) object) and passed to the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function of the worker thread.</span></span> <span data-ttu-id="4439d-121">Cette fonction membre retourne immédiatement après la mise en file d’attente de la demande et n’attend pas que le thread exécute la demande.</span><span class="sxs-lookup"><span data-stu-id="4439d-121">This member function returns immediately after queuing the request and does not wait for the thread to fulfill the request.</span></span> <span data-ttu-id="4439d-122">La fonction membre **CMsgThread :: ThreadMessageProc** de la classe dérivée définit les quatre paramètres.</span><span class="sxs-lookup"><span data-stu-id="4439d-122">The **CMsgThread::ThreadMessageProc** member function of the derived class defines the four parameters.</span></span>

<span data-ttu-id="4439d-123">Cette fonction membre utilise une liste sécurisée multithread. par conséquent, plusieurs appels à cette fonction membre à partir de différents threads peuvent être effectués en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="4439d-123">This member function uses a multithread safe list, so multiple calls to this member function from different threads can be made safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="4439d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4439d-124">Requirements</span></span>



| <span data-ttu-id="4439d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4439d-125">Requirement</span></span> | <span data-ttu-id="4439d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4439d-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4439d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4439d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4439d-128"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4439d-128"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4439d-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4439d-129">Library</span></span><br/> | <dl> <span data-ttu-id="4439d-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4439d-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4439d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4439d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4439d-132">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="4439d-132">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




