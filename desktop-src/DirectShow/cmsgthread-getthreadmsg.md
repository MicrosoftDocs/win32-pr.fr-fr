---
description: Récupère un objet CMsg mis en file d’attente contenant une requête.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Méthode CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530320"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="ab917-103">Méthode CMsgThread. GetThreadMsg</span><span class="sxs-lookup"><span data-stu-id="ab917-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="ab917-104">Récupère un objet [**CMsg**](cmsg.md) mis en file d’attente contenant une requête.</span><span class="sxs-lookup"><span data-stu-id="ab917-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab917-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab917-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="ab917-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab917-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab917-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="ab917-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="ab917-108">Pointeur vers un objet [**CMsg**](cmsg.md) alloué.</span><span class="sxs-lookup"><span data-stu-id="ab917-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab917-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab917-109">Return value</span></span>

<span data-ttu-id="ab917-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ab917-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab917-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ab917-111">Remarks</span></span>

<span data-ttu-id="ab917-112">Cette fonction membre est appelée à partir de la fonction [**ThreadProc**](camthread-threadproc.md) privée du thread de travail pour récupérer la fonction membre suivante.</span><span class="sxs-lookup"><span data-stu-id="ab917-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="ab917-113">Le paramètre *MSG* doit pointer vers un objet [**CMsg**](cmsg.md) alloué qui sera rempli avec les paramètres de la requête suivante dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ab917-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="ab917-114">S’il n’y a aucune demande en file d’attente, cette fonction membre se bloque jusqu’à ce que la requête suivante soit mise en file d’attente (par un appel à la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).</span><span class="sxs-lookup"><span data-stu-id="ab917-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab917-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab917-115">Requirements</span></span>



| <span data-ttu-id="ab917-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab917-116">Requirement</span></span> | <span data-ttu-id="ab917-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab917-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab917-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab917-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ab917-119"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab917-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab917-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab917-120">Library</span></span><br/> | <dl> <span data-ttu-id="ab917-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab917-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab917-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab917-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab917-123">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="ab917-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




