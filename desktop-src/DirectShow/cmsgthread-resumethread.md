---
description: 'Utilise la fonction Win32 ResumeThread de Microsoft pour poursuivre l’opération du thread de travail après un appel précédent à la fonction membre CMsgThread :: SuspendThread.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: CMsgThread. ResumeThread, méthode (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532014"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="456b0-103">CMsgThread. ResumeThread, méthode</span><span class="sxs-lookup"><span data-stu-id="456b0-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="456b0-104">Utilise la fonction Win32 **ResumeThread** de Microsoft pour poursuivre l’opération du thread de travail après un appel précédent à la fonction membre [**CMsgThread :: SuspendThread**](cmsgthread-suspendthread.md) .</span><span class="sxs-lookup"><span data-stu-id="456b0-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="456b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="456b0-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="456b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="456b0-106">Parameters</span></span>

<span data-ttu-id="456b0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="456b0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="456b0-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="456b0-108">Return value</span></span>

<span data-ttu-id="456b0-109">Si la fonction membre est réussie, la valeur de retour est le nombre de suspensions précédent du thread.</span><span class="sxs-lookup"><span data-stu-id="456b0-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="456b0-110">Si la fonction membre échoue, la valeur de retour est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="456b0-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="456b0-111">Pour obtenir des informations d’erreur étendues, appelez la fonction Microsoft Win32 **GetLastError** .</span><span class="sxs-lookup"><span data-stu-id="456b0-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="456b0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="456b0-112">Requirements</span></span>



| <span data-ttu-id="456b0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="456b0-113">Requirement</span></span> | <span data-ttu-id="456b0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="456b0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456b0-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="456b0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="456b0-116"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="456b0-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="456b0-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="456b0-117">Library</span></span><br/> | <dl> <span data-ttu-id="456b0-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="456b0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456b0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="456b0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456b0-120">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="456b0-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




