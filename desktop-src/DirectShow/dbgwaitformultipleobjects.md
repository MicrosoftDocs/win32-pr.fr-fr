---
description: Attend qu’un ou plusieurs des objets spécifiés soient signalés.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: DbgWaitForMultipleObjects, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526880"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="dcfce-103">DbgWaitForMultipleObjects fonction)</span><span class="sxs-lookup"><span data-stu-id="dcfce-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="dcfce-104">Attend qu’un ou plusieurs des objets spécifiés soient signalés.</span><span class="sxs-lookup"><span data-stu-id="dcfce-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="dcfce-105">Dans une version Debug, cette fonction déclenche une assertion si l’intervalle de délai d’attente expire avant que les objets ne soient signalés.</span><span class="sxs-lookup"><span data-stu-id="dcfce-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="dcfce-106">Pour définir l’intervalle de délai d’attente, appelez la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="dcfce-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="dcfce-107">Dans une version commerciale, cette fonction est équivalente à la fonction **WaitForMultipleObjects** avec un intervalle de délai d’attente infini.</span><span class="sxs-lookup"><span data-stu-id="dcfce-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcfce-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="dcfce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcfce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcfce-110">*nCount*</span><span class="sxs-lookup"><span data-stu-id="dcfce-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfce-111">Nombre d’objets.</span><span class="sxs-lookup"><span data-stu-id="dcfce-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="dcfce-112">*lpHandles*</span><span class="sxs-lookup"><span data-stu-id="dcfce-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfce-113">Tableau de handles aux objets, de taille *nCount*.</span><span class="sxs-lookup"><span data-stu-id="dcfce-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="dcfce-114">*bWaitAll*</span><span class="sxs-lookup"><span data-stu-id="dcfce-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="dcfce-115">Valeur booléenne qui spécifie s’il faut attendre tous les objets.</span><span class="sxs-lookup"><span data-stu-id="dcfce-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="dcfce-116">Si la **valeur est true**, la fonction attend que tous les objets soient signalés.</span><span class="sxs-lookup"><span data-stu-id="dcfce-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="dcfce-117">Sinon, elle attend qu’au moins un objet soit signalé.</span><span class="sxs-lookup"><span data-stu-id="dcfce-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dcfce-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcfce-118">Requirements</span></span>



| <span data-ttu-id="dcfce-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcfce-119">Requirement</span></span> | <span data-ttu-id="dcfce-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcfce-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfce-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcfce-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dcfce-122"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcfce-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcfce-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcfce-123">Library</span></span><br/> | <dl> <span data-ttu-id="dcfce-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dcfce-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcfce-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcfce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcfce-126">Fonctions de débogage d’attente</span><span class="sxs-lookup"><span data-stu-id="dcfce-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




