---
description: La méthode InitialThreadProc appelle la procédure de thread principale.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Iniméthode tialThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529928"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="a9d66-103">CAMThread.Iniméthode tialThreadProc</span><span class="sxs-lookup"><span data-stu-id="a9d66-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="a9d66-104">La `InitialThreadProc` méthode appelle la procédure de thread principale.</span><span class="sxs-lookup"><span data-stu-id="a9d66-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9d66-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="a9d66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9d66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d66-107">*va*</span><span class="sxs-lookup"><span data-stu-id="a9d66-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d66-108">`this` dirigé.</span><span class="sxs-lookup"><span data-stu-id="a9d66-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d66-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9d66-109">Return value</span></span>

<span data-ttu-id="a9d66-110">Retourne la **valeur DWORD** retournée par [**CAMThread :: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="a9d66-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="a9d66-111">La classe dérivée définit cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a9d66-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d66-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a9d66-112">Remarks</span></span>

<span data-ttu-id="a9d66-113">La méthode [**CAMThread :: Create**](camthread-create.md) utilise cette méthode pour la procédure de thread lors de la création du thread.</span><span class="sxs-lookup"><span data-stu-id="a9d66-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="a9d66-114">Elle utilise le `this` pointeur comme argument de thread.</span><span class="sxs-lookup"><span data-stu-id="a9d66-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="a9d66-115">Cette méthode appelle la méthode [**CAMThread :: CoInitializeHelper**](camthread-coinitializehelper.md) , puis ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="a9d66-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d66-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9d66-116">Requirements</span></span>



| <span data-ttu-id="a9d66-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9d66-117">Requirement</span></span> | <span data-ttu-id="a9d66-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9d66-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d66-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9d66-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a9d66-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d66-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a9d66-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a9d66-121">Library</span></span><br/> | <dl> <span data-ttu-id="a9d66-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d66-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d66-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9d66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d66-124">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="a9d66-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




