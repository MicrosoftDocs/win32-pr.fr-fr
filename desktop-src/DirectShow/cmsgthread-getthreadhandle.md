---
description: Récupère le handle du thread dans l’objet CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Méthode CMsgThread. GetThreadHandle (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537529"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="48285-103">Méthode CMsgThread. GetThreadHandle</span><span class="sxs-lookup"><span data-stu-id="48285-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="48285-104">Récupère le handle du thread dans l’objet [**CMsgThread**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="48285-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="48285-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48285-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="48285-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48285-106">Parameters</span></span>

<span data-ttu-id="48285-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="48285-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48285-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48285-108">Return value</span></span>

<span data-ttu-id="48285-109">Retourne le handle de thread.</span><span class="sxs-lookup"><span data-stu-id="48285-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="48285-110">Notes</span><span class="sxs-lookup"><span data-stu-id="48285-110">Remarks</span></span>

<span data-ttu-id="48285-111">Le descripteur de thread peut être passé aux fonctions d’attente, telles que [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="48285-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="48285-112">Le handle de thread est signalé lorsque le thread s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="48285-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="48285-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48285-113">Requirements</span></span>



| <span data-ttu-id="48285-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48285-114">Requirement</span></span> | <span data-ttu-id="48285-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="48285-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48285-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="48285-116">Header</span></span><br/>  | <dl> <span data-ttu-id="48285-117"><dt>Msgthrd. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48285-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48285-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48285-118">Library</span></span><br/> | <dl> <span data-ttu-id="48285-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48285-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48285-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48285-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48285-121">**CMsgThread, classe**</span><span class="sxs-lookup"><span data-stu-id="48285-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

