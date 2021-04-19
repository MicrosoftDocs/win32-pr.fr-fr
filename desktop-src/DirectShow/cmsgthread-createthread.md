---
description: Crée un thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: CMsgThread. CreateThread, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539227"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="394ac-103">CMsgThread. CreateThread, méthode</span><span class="sxs-lookup"><span data-stu-id="394ac-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="394ac-104">Crée un thread.</span><span class="sxs-lookup"><span data-stu-id="394ac-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="394ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="394ac-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="394ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="394ac-106">Parameters</span></span>

<span data-ttu-id="394ac-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="394ac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="394ac-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="394ac-108">Return value</span></span>

<span data-ttu-id="394ac-109">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="394ac-109">Returns one of the following values.</span></span>



| <span data-ttu-id="394ac-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="394ac-110">Return code</span></span>                                                                              | <span data-ttu-id="394ac-111">Description</span><span class="sxs-lookup"><span data-stu-id="394ac-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="394ac-112"><dt>VRAI \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="394ac-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="394ac-113">Le thread a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="394ac-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="394ac-114"><dt>FALSe \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="394ac-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="394ac-115">Le thread n’a pas été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="394ac-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="394ac-116">Notes</span><span class="sxs-lookup"><span data-stu-id="394ac-116">Remarks</span></span>

<span data-ttu-id="394ac-117">Le thread se bloque jusqu’à ce qu’une demande soit mise en file d’attente (via la fonction membre [**CMsgThread ::P utthreadmsg**](cmsgthread-putthreadmsg.md) ), puis appelle la fonction membre [**CMsgThread :: ThreadMessageProc**](cmsgthread-threadmessageproc.md) avec chaque message.</span><span class="sxs-lookup"><span data-stu-id="394ac-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="394ac-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="394ac-118">Requirements</span></span>



| <span data-ttu-id="394ac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="394ac-119">Requirement</span></span> | <span data-ttu-id="394ac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="394ac-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394ac-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="394ac-121">Header</span></span><br/>  | <dl> <span data-ttu-id="394ac-122"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="394ac-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="394ac-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="394ac-123">Library</span></span><br/> | <dl> <span data-ttu-id="394ac-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="394ac-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="394ac-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="394ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394ac-126">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="394ac-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




