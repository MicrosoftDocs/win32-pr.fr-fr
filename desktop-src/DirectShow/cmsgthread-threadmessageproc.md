---
description: Traite les demandes. Il s’agit d’une fonction membre virtuelle pure.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Méthode CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526566"
---
# <a name="cmsgthreadthreadmessageproc-method"></a><span data-ttu-id="79966-104">Méthode CMsgThread. ThreadMessageProc</span><span class="sxs-lookup"><span data-stu-id="79966-104">CMsgThread.ThreadMessageProc method</span></span>

<span data-ttu-id="79966-105">Traite les demandes.</span><span class="sxs-lookup"><span data-stu-id="79966-105">Processes requests.</span></span> <span data-ttu-id="79966-106">Il s’agit d’une fonction membre virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="79966-106">This is a pure virtual member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="79966-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79966-107">Syntax</span></span>


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="79966-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79966-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79966-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="79966-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="79966-110">Code de la requête.</span><span class="sxs-lookup"><span data-stu-id="79966-110">Request code.</span></span>

</dd> <dt>

<span data-ttu-id="79966-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="79966-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="79966-112">Paramètre d’indicateur facultatif à demander.</span><span class="sxs-lookup"><span data-stu-id="79966-112">Optional flag parameter to request.</span></span>

</dd> <dt>

<span data-ttu-id="79966-113">*lpParam*</span><span class="sxs-lookup"><span data-stu-id="79966-113">*lpParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79966-114">Pointeur facultatif vers des données supplémentaires ou un bloc de données de retour.</span><span class="sxs-lookup"><span data-stu-id="79966-114">Optional pointer to extra data or a return data block.</span></span>

</dd> <dt>

<span data-ttu-id="79966-115">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="79966-115">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="79966-116">Pointeur facultatif vers un objet d’événement.</span><span class="sxs-lookup"><span data-stu-id="79966-116">Optional pointer to an event object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79966-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79966-117">Return value</span></span>

<span data-ttu-id="79966-118">Tout retour différent de zéro provoque la fermeture du thread.</span><span class="sxs-lookup"><span data-stu-id="79966-118">Any nonzero return causes the thread to exit.</span></span> <span data-ttu-id="79966-119">Retourne zéro sauf si une demande de sortie a été traitée récemment.</span><span class="sxs-lookup"><span data-stu-id="79966-119">Returns zero unless an exit request has been processed recently.</span></span>

## <a name="remarks"></a><span data-ttu-id="79966-120">Notes</span><span class="sxs-lookup"><span data-stu-id="79966-120">Remarks</span></span>

<span data-ttu-id="79966-121">Cette fonction virtuelle pure doit être substituée dans votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="79966-121">This pure virtual function must be overridden in your derived class.</span></span> <span data-ttu-id="79966-122">Elle est appelée une fois pour chaque demande en file d’attente par un appel à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="79966-122">It will be called once for each request queued by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function.</span></span>

<span data-ttu-id="79966-123">La fonction membre définit les quatre paramètres.</span><span class="sxs-lookup"><span data-stu-id="79966-123">The member function defines the four parameters.</span></span> <span data-ttu-id="79966-124">En général, utilisez le paramètre *uMsg* pour indiquer la demande, et les trois autres paramètres seront des paramètres supplémentaires facultatifs.</span><span class="sxs-lookup"><span data-stu-id="79966-124">Typically, use the *uMsg* parameter to indicate the request, and the other three parameters will be optional additional parameters.</span></span> <span data-ttu-id="79966-125">L’application appelante peut fournir un pointeur vers un objet [**CAMEvent**](camevent.md) dans le paramètre *pEvent* si votre application l’exige.</span><span class="sxs-lookup"><span data-stu-id="79966-125">The calling application can supply a pointer to a [**CAMEvent**](camevent.md) object in the *pEvent* parameter if your application requires it.</span></span> <span data-ttu-id="79966-126">Vous devez définir cet événement après avoir traité l’événement à l’aide d’une expression telle que :</span><span class="sxs-lookup"><span data-stu-id="79966-126">You must set this event after processing the event by using an expression such as:</span></span>


```C++
pEvent->SetEvent
```



<span data-ttu-id="79966-127">Un code de demande doit être mis de côté pour indiquer au thread de travail de se fermer.</span><span class="sxs-lookup"><span data-stu-id="79966-127">One request code must be set aside to tell the worker thread to exit.</span></span> <span data-ttu-id="79966-128">Une fois cette demande reçue, retournez 1 à partir de cette fonction membre.</span><span class="sxs-lookup"><span data-stu-id="79966-128">Upon receiving this request, return 1 from this member function.</span></span> <span data-ttu-id="79966-129">Retourne 0 si vous ne souhaitez pas que le thread de travail se termine.</span><span class="sxs-lookup"><span data-stu-id="79966-129">Return 0 if you do not want the worker thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="79966-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79966-130">Requirements</span></span>



| <span data-ttu-id="79966-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79966-131">Requirement</span></span> | <span data-ttu-id="79966-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="79966-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79966-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="79966-133">Header</span></span><br/>  | <dl> <span data-ttu-id="79966-134"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79966-134"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79966-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79966-135">Library</span></span><br/> | <dl> <span data-ttu-id="79966-136"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="79966-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79966-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79966-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79966-138">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="79966-138">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




