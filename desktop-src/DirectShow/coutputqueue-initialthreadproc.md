---
description: 'La méthode InitialThreadProc appelle la méthode COutputQueue :: ThreadProc lorsque le thread est créé.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Iniméthode tialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543883"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="29781-103">COutputQueue.Iniméthode tialThreadProc</span><span class="sxs-lookup"><span data-stu-id="29781-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="29781-104">La `InitialThreadProc` méthode appelle la méthode [**COutputQueue :: ThreadProc**](coutputqueue-threadproc.md) lorsque le thread est créé.</span><span class="sxs-lookup"><span data-stu-id="29781-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="29781-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29781-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="29781-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29781-107">*va*</span><span class="sxs-lookup"><span data-stu-id="29781-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="29781-108">`this` dirigé.</span><span class="sxs-lookup"><span data-stu-id="29781-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29781-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29781-109">Return value</span></span>

<span data-ttu-id="29781-110">Retourne la valeur retournée par la méthode [**COutputQueue :: ThreadProc**](coutputqueue-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="29781-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="29781-111">Notes</span><span class="sxs-lookup"><span data-stu-id="29781-111">Remarks</span></span>

<span data-ttu-id="29781-112">Cette méthode est la procédure de thread pour le thread de travail de l’objet.</span><span class="sxs-lookup"><span data-stu-id="29781-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="29781-113">Le pointeur de l’objet `this` est le paramètre de thread.</span><span class="sxs-lookup"><span data-stu-id="29781-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="29781-114">La méthode déréférence ce pour appeler **ThreadProc**.</span><span class="sxs-lookup"><span data-stu-id="29781-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="29781-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29781-115">Requirements</span></span>



| <span data-ttu-id="29781-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29781-116">Requirement</span></span> | <span data-ttu-id="29781-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="29781-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29781-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="29781-118">Header</span></span><br/>  | <dl> <span data-ttu-id="29781-119"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29781-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29781-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29781-120">Library</span></span><br/> | <dl> <span data-ttu-id="29781-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="29781-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29781-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29781-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29781-123">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="29781-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




