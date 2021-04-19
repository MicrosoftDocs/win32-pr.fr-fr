---
description: Utilise la fonction Microsoft Win32 GetThreadPriority pour récupérer la priorité du thread de travail actuel.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Méthode CMsgThread. GetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542267"
---
# <a name="cmsgthreadgetthreadpriority-method"></a><span data-ttu-id="49c4b-103">Méthode CMsgThread. GetThreadPriority</span><span class="sxs-lookup"><span data-stu-id="49c4b-103">CMsgThread.GetThreadPriority method</span></span>

<span data-ttu-id="49c4b-104">Utilise la fonction Microsoft Win32 **GetThreadPriority** pour récupérer la priorité du thread de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="49c4b-104">Uses the Microsoft Win32 **GetThreadPriority** function to retrieve the priority of the current worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c4b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49c4b-105">Syntax</span></span>


```C++
int GetThreadPriority();
```



## <a name="parameters"></a><span data-ttu-id="49c4b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49c4b-106">Parameters</span></span>

<span data-ttu-id="49c4b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="49c4b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49c4b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49c4b-108">Return value</span></span>

<span data-ttu-id="49c4b-109">Retourne la priorité de thread sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="49c4b-109">Returns the thread priority as an integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c4b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49c4b-110">Requirements</span></span>



| <span data-ttu-id="49c4b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49c4b-111">Requirement</span></span> | <span data-ttu-id="49c4b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="49c4b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c4b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="49c4b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="49c4b-114"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49c4b-114"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49c4b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49c4b-115">Library</span></span><br/> | <dl> <span data-ttu-id="49c4b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49c4b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c4b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49c4b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c4b-118">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="49c4b-118">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




