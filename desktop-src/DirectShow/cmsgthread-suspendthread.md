---
description: Utilise la fonction Microsoft Win32 SuspendThread pour interrompre l’opération d’un thread en cours d’exécution.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: CMsgThread. SuspendThread, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526474"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="9766c-103">CMsgThread. SuspendThread, méthode</span><span class="sxs-lookup"><span data-stu-id="9766c-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="9766c-104">Utilise la fonction Microsoft Win32 **SuspendThread** pour interrompre l’opération d’un thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9766c-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="9766c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9766c-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="9766c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9766c-106">Parameters</span></span>

<span data-ttu-id="9766c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9766c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9766c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9766c-108">Return value</span></span>

<span data-ttu-id="9766c-109">Si la fonction membre est réussie, la valeur de retour est le nombre de suspensions précédent du thread.</span><span class="sxs-lookup"><span data-stu-id="9766c-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="9766c-110">Si la fonction membre échoue, la valeur de retour est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="9766c-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="9766c-111">Pour obtenir des informations d’erreur étendues, appelez la fonction Microsoft Win32 **GetLastError** .</span><span class="sxs-lookup"><span data-stu-id="9766c-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9766c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9766c-112">Remarks</span></span>

<span data-ttu-id="9766c-113">Le thread client appelle cette fonction membre pour interrompre l’opération du thread de travail.</span><span class="sxs-lookup"><span data-stu-id="9766c-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="9766c-114">Le thread de travail reste suspendu et ne s’exécute pas jusqu’à ce qu’un appel supplémentaire à la fonction membre [**CMsgThread :: ResumeThread**](cmsgthread-resumethread.md) soit effectué.</span><span class="sxs-lookup"><span data-stu-id="9766c-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="9766c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9766c-115">Requirements</span></span>



| <span data-ttu-id="9766c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9766c-116">Requirement</span></span> | <span data-ttu-id="9766c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9766c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9766c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="9766c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9766c-119"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9766c-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9766c-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9766c-120">Library</span></span><br/> | <dl> <span data-ttu-id="9766c-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9766c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9766c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9766c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9766c-123">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="9766c-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




