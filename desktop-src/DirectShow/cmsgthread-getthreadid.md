---
description: Récupère l’identificateur du thread.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Méthode CMsgThread. GetThreadID (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545505"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="e530b-103">Méthode CMsgThread. GetThreadID</span><span class="sxs-lookup"><span data-stu-id="e530b-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="e530b-104">Récupère l’identificateur du thread.</span><span class="sxs-lookup"><span data-stu-id="e530b-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e530b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e530b-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="e530b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e530b-106">Parameters</span></span>

<span data-ttu-id="e530b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e530b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e530b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e530b-108">Return value</span></span>

<span data-ttu-id="e530b-109">Retourne le membre de données privées de l' **\_ ThreadID m** .</span><span class="sxs-lookup"><span data-stu-id="e530b-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="e530b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e530b-110">Remarks</span></span>

<span data-ttu-id="e530b-111">Cette fonction retourne l’identificateur Microsoft Win32 pour le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="e530b-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="e530b-112">Vous pouvez appeler cette fonction membre sur le thread de travail ou un thread client.</span><span class="sxs-lookup"><span data-stu-id="e530b-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="e530b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e530b-113">Requirements</span></span>



| <span data-ttu-id="e530b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e530b-114">Requirement</span></span> | <span data-ttu-id="e530b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e530b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e530b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e530b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e530b-117"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e530b-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e530b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e530b-118">Library</span></span><br/> | <dl> <span data-ttu-id="e530b-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e530b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e530b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e530b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e530b-121">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="e530b-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




