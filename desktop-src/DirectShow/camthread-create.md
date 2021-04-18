---
description: La méthode Create crée le thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: CAMThread. Create, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533150"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="d4480-103">CAMThread. Create, méthode</span><span class="sxs-lookup"><span data-stu-id="d4480-103">CAMThread.Create method</span></span>

<span data-ttu-id="d4480-104">La `Create` méthode crée le thread.</span><span class="sxs-lookup"><span data-stu-id="d4480-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4480-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4480-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="d4480-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4480-106">Parameters</span></span>

<span data-ttu-id="d4480-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d4480-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4480-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4480-108">Return value</span></span>

<span data-ttu-id="d4480-109">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d4480-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4480-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d4480-110">Remarks</span></span>

<span data-ttu-id="d4480-111">Cette méthode crée le thread, à l’aide de la méthode [**CAMThread :: InitialThreadProc**](camthread-initialthreadproc.md) pour la procédure de thread et `this` pour l’argument de thread.</span><span class="sxs-lookup"><span data-stu-id="d4480-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="d4480-112">La méthode échoue si le thread existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d4480-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4480-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4480-113">Requirements</span></span>



| <span data-ttu-id="d4480-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4480-114">Requirement</span></span> | <span data-ttu-id="d4480-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4480-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4480-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4480-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d4480-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4480-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d4480-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4480-118">Library</span></span><br/> | <dl> <span data-ttu-id="d4480-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4480-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4480-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4480-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4480-121">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="d4480-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




